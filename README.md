# Ayase


A high-performance Rust-based AI agent built using [rig](https://github.com/0xPlaygrounds/rig). Ayase powers an autonomous and engaging social media presence on [X](x.com).

Follow Ayase: [@Ayase_Arc](https://x.com/[Ayase_Arc])

## Overview

Ayase is an AI-driven social media agent that seamlessly interacts on platforms while maintaining a distinct personality and natural conversational flow. Designed with Rust for efficiency and reliability, it utilizes the rig framework for advanced AI functionality.

## Key Features

### Character-Driven Design
- Comprehensive personality traits for authentic interactions
- Adjustable writing styles and topic preferences
- Dynamic response generation based on character profiles

### Autonomous Engagement
- Creates relevant, original posts
- Responds intelligently to mentions and messages
- Smart filtering to prioritize meaningful interactions
- Ensures natural and fluid conversation flow

### Advanced Memory Management
- Persistent interaction history
- Context-aware responses
- Tracks relationships with other users

### Platform Integration
- Rate limiting and scheduling for seamless automation
- Natural posting patterns with random delays
- Full integration with Twitter API v2

### Modular and Scalable
- Decoupled core logic and integrations
- Extensible character trait system
- Pluggable provider framework
- Optimized memory usage for high performance

## Prerequisites

- Latest stable version of Rust
- API Keys:
  - Anthropic Claude API
  - Twitter API v2 credentials (OAuth 1.0a)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/chakaboommm/Saki
cd Saki
```

2. Create a `.env` file with the required credentials:
```env
ANTHROPIC_API_KEY=your_api_key
TWITTER_CONSUMER_KEY=your_key
TWITTER_CONSUMER_SECRET=your_secret
TWITTER_ACCESS_TOKEN=your_token
TWITTER_ACCESS_TOKEN_SECRET=your_token_secret
CHARACTER_NAME=your_character_name
```

3. Set up your character:
   - Create a new directory: `characters/{CHARACTER_NAME}/`
   - Add the character definition in `character.json`

## Character Configuration

Define characters in a structured JSON format:

```json
{
  "instructions": {
    "base": "Base character instructions",
    "suffix": "Additional instructions"
  },
  "adjectives": ["trait1", "trait2"],
  "bio": {
    "headline": "Character headline",
    "key_traits": ["trait1", "trait2"]
  },
  "lore": ["background1", "background2"],
  "styles": ["style1", "style2"],
  "topics": ["topic1", "topic2"],
  "post_style_examples": ["example1", "example2"]
}
```

## Usage

Run the agent:
```bash
cargo run
```

## Project Structure

```
Saki/
├── src/
│   ├── core/           # Core functionality
│   ├── characteristics/ # Character traits
│   ├── providers/      # External service integrations
│   └── memory/         # Persistence layer
├── characters/         # Character definitions
└── tests/             # Test suite
```

## Dependencies

- [rig](https://github.com/0xPlaygrounds/rig): AI agent framework
- `twitter-v2`: Twitter API client
- `tokio`: Async runtime
- `serde`: Serialization/deserialization
- `anyhow`: Error handling

## Acknowledgments

- Thanks to the [rig](https://github.com/0xPlaygrounds/rig) team for their AI framework.
- Gratitude to all contributors and maintainers.

## Support

For questions or support, please open an issue in this repository.
