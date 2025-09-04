# Contributing to Typical Colors 2

We welcome contributions from the community! Whether you're suggesting weapon rebalances, proposing new concepts, or improving documentation, your input helps make TC2 better.

## How to Contribute

### 1. Fork the Repository
- Visit the [GitHub repository](https://github.com/examplia/balance)
- Click the "Fork" button to create your own copy

### 2. Create a Branch
```bash
git checkout -b your-feature-branch
```

### 3. Add Your Contribution
Follow the guidelines below based on what you're contributing.

### 4. Test Your Changes
- Ensure JSON is valid
- Verify images display correctly
- Test the website functionality

### 5. Submit a Pull Request
- Push your changes to your fork
- Create a pull request with a clear description
- Wait for review and feedback

## Adding Weapon Concepts

### JSON Format

Add your weapon to the `weapons.json` file using this structure:

```json
{
  "name": "Your Weapon Name",
  "class": "Class Name",
  "type": "Weapon Type",
  "image": "images/your-weapon-image.png",
  "stats": {
    "positive": ["Positive stat 1", "Positive stat 2"],
    "negative": ["Negative stat 1", "Negative stat 2"]
  },
  "changes": ["Change description 1", "Change description 2"],
  "reasoning": "Explanation for the concept and changes",
  "isConcept": true
}
```

### Required Fields

- **name** (string): The weapon's name
- **class** (string): Class this weapon belongs to
  - Flanker, Trooper, Arsonist, Brute, Mechanic, Doctor, Marksman, Annihilator, Agent
- **type** (string): Weapon slot - "Primary", "Secondary", "Melee", "Building"
- **image** (string): Path to weapon image in `images/` folder
- **stats** (object): Positive and negative stat changes
- **isConcept** (boolean): `true` for new concepts, `false` for rebalances

### Optional Fields

- **changes** (array): Specific changes made (can be empty for concepts)
- **reasoning** (string): Design explanation (can be empty for concepts)

### Examples

#### New Weapon Concept
```json
{
  "name": "Plasma Blaster",
  "class": "Flanker",
  "type": "Primary",
  "image": "images/plasma-blaster.png",
  "stats": {
    "positive": ["+25% faster firing speed", "On hit: Apply plasma burn"],
    "negative": ["-20% damage penalty", "-15% clip size"]
  },
  "changes": [],
  "reasoning": "A high-tech weapon concept for Flanker focusing on sustained damage.",
  "isConcept": true
}
```

#### Weapon Rebalance
```json
{
  "name": "Existing Weapon",
  "class": "Trooper",
  "type": "Primary",
  "image": "images/existing-weapon.png",
  "stats": {
    "positive": ["+10% damage bonus"],
    "negative": ["-5% slower firing speed"]
  },
  "changes": ["Increased damage bonus from 5% to 10%", "Added firing speed penalty"],
  "reasoning": "Balancing the weapon to reduce its power while maintaining viability.",
  "isConcept": false
}
```

## Guidelines for Stats

### Be Specific
- ✅ "+25% faster firing speed"
- ❌ "Faster firing"

### Use Standard Terminology
- Follow TF2 conventions: "mini-crits", "crits", "blast jumping"

### Balance is Key
Ensure positive and negative stats create interesting trade-offs.

### Keep it Concise
Each stat should be a short, clear description.

## Image Requirements

### Format
- PNG preferred, JPG/JPEG acceptable

### Size
- Aim for 256x256 pixels or similar square dimensions

### Naming
- Use lowercase with hyphens: `my-weapon-concept.png`

### Content
- Clearly represent the weapon concept
- Reference existing TF2 weapon art styles

## Validation Checklist

Before submitting:
- [ ] JSON is valid (use a JSON validator)
- [ ] Image path matches file in `images/`
- [ ] All required fields present and correctly formatted
- [ ] Weapon displays properly in the application
- [ ] Stats are balanced and follow guidelines
- [ ] Reasoning is clear and well-explained

## Need Help?

### Contact Us
- **@snazzygold** - The idea guy
- **@oxxywozz** - The website wizard

### Join Our Discord
[![Join Discord](https://img.shields.io/badge/Discord-Join%20Community-7289DA?style=for-the-badge&logo=discord)](https://discord.gg/9TDY9P2cmG)

## Code of Conduct

- Be respectful and constructive in feedback
- Focus on balance and gameplay improvement
- Respect the community's vision for TC2
- Keep discussions civil and on-topic

## Recognition

Contributors will be credited in the changelog and may be mentioned in future updates. Your ideas help shape the future of Typical Colors 2!

---

*Happy contributing! Keep it casual, keep it fun, keep it balanced!* 🎮