# Basic Blockchain

A simple blockchain implementation in Rust that demonstrates the core concepts of blockchain technology.

## Features

- Create and mine new blocks with proof-of-work
- Add transactions between addresses
- Adjustable mining difficulty
- Configurable mining rewards
- Merkle tree implementation for transaction validation
- SHA-256 hashing for blockchain security

## Prerequisites

- Rust (edition 2024)
- Cargo package manager

## Dependencies

This project uses the following crates:
- serde (1.0.219): For serialization and deserialization
- serde_derive (1.0.219): For derive macros
- serde_json (1.0.140): For JSON handling
- sha2 (0.10.8): For SHA-256 cryptographic hashing
- time (0.3.41): For time operations
- chrono (0.4): For timestamp creation

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/basic-blockchain.git
cd basic-blockchain
```

2. Build the project:
```bash
cargo build --release
```

3. Run the blockchain:
```bash
cargo run --release
```

## Usage

When you start the application, you'll be prompted to:
1. Enter a miner address (this will receive mining rewards)
2. Set the initial mining difficulty (higher = more computational effort required)

After initialization, you can:
- Create new transactions between addresses
- Mine new blocks
- Adjust the mining difficulty
- Change the mining reward
- Exit the application

## How It Works

### Blockchain Structure

The blockchain consists of:
- **Blocks**: Contains a header and transactions
- **Blockheader**: Contains metadata including timestamp, nonce, previous hash, merkle root, and difficulty
- **Transactions**: Records of value transfers between addresses

### Mining Process

Mining uses a proof-of-work system:
1. The miner receives pending transactions
2. A reward transaction is added
3. A merkle root is calculated from all transactions
4. The nonce is iteratively adjusted until a hash with the required number of leading zeros is found
5. Once a valid hash is found, the block is added to the chain

### Transaction Verification

Transactions are verified using a merkle tree, which allows efficient and secure verification of transaction inclusion.

## License

[MIT License](LICENSE)

---

# Blockchain de Base (French)

Une implémentation simple de blockchain en Rust démontrant les concepts fondamentaux de la technologie blockchain.

## Fonctionnalités

- Création et minage de nouveaux blocs avec preuve de travail
- Ajout de transactions entre adresses
- Difficulté de minage ajustable
- Récompenses de minage configurables
- Implémentation d'arbre de Merkle pour la validation des transactions
- Hachage SHA-256 pour la sécurité de la blockchain

## Prérequis

- Rust (édition 2024)
- Gestionnaire de paquets Cargo

## Dépendances

Ce projet utilise les crates suivants :
- serde (1.0.219) : Pour la sérialisation et la désérialisation
- serde_derive (1.0.219) : Pour les macros dérivées
- serde_json (1.0.140) : Pour la gestion du JSON
- sha2 (0.10.8) : Pour le hachage cryptographique SHA-256
- time (0.3.41) : Pour les opérations temporelles
- chrono (0.4) : Pour la création d'horodatages

## Installation

1. Clonez le dépôt :
```bash
git clone https://github.com/votrenomdutilisateur/basic-blockchain.git
cd basic-blockchain
```

2. Compilez le projet :
```bash
cargo build --release
```

3. Exécutez la blockchain :
```bash
cargo run --release
```

## Utilisation

Lorsque vous démarrez l'application, vous serez invité à :
1. Saisir une adresse de mineur (celle-ci recevra les récompenses de minage)
2. Définir la difficulté initiale de minage (plus élevée = plus d'effort de calcul requis)

Après l'initialisation, vous pouvez :
- Créer de nouvelles transactions entre adresses
- Miner de nouveaux blocs
- Ajuster la difficulté de minage
- Modifier la récompense de minage
- Quitter l'application

## Fonctionnement

### Structure de la Blockchain

La blockchain se compose de :
- **Blocs** : Contient un en-tête et des transactions
- **En-tête de bloc** : Contient des métadonnées, y compris l'horodatage, le nonce, le hachage précédent, la racine de Merkle et la difficulté
- **Transactions** : Enregistrements des transferts de valeur entre adresses

### Processus de Minage

Le minage utilise un système de preuve de travail :
1. Le mineur reçoit les transactions en attente
2. Une transaction de récompense est ajoutée
3. Une racine de Merkle est calculée à partir de toutes les transactions
4. Le nonce est ajusté de manière itérative jusqu'à ce qu'un hachage avec le nombre requis de zéros en tête soit trouvé
5. Une fois qu'un hachage valide est trouvé, le bloc est ajouté à la chaîne

### Vérification des Transactions

Les transactions sont vérifiées à l'aide d'un arbre de Merkle, qui permet une vérification efficace et sécurisée de l'inclusion des transactions.

## Licence

[Licence MIT](LICENSE)
