# Contributing Weapon Concepts

This repository contains weapon concepts and rebalances for custom Team Fortress 2 classes. If you'd like to contribute a new weapon concept, please follow the guidelines below to add it to the `weapons.json` file.

## How to Add a New Weapon Concept

1. **Fork the repository** and create a new branch for your contribution.
2. **Add your weapon concept** to the `weapons.json` file following the format described below.
3. **Add an image** for your weapon to the `images/` folder (see Image Requirements).
4. **Test your changes** by ensuring the JSON is valid and the image displays correctly.
5. **Submit a pull request** with a description of your concept and reasoning.

## JSON Format

The `weapons.json` file is a JSON object containing a single array called `weapons`. Each weapon is an object with the following structure:

```json
{
  "weapons": [
    {
      "name": "Weapon Name",
      "class": "Class Name",
      "type": "Weapon Type",
      "image": "images/weapon-image.png",
      "stats": {
        "positive": ["Positive stat 1", "Positive stat 2"],
        "negative": ["Negative stat 1", "Negative stat 2"]
      },
      "changes": ["Change description 1", "Change description 2"],
      "reasoning": "Explanation for the concept and changes",
      "isConcept": true
    }
  ]
}
```

### Required Fields

- **name** (string): The name of the weapon concept.
- **class** (string): The class this weapon belongs to (e.g., "Flanker", "Soldier", "Arsonist", "Brute", "Mechanic", "Doctor", "Marksman").
- **type** (string): The weapon slot type ("Primary", "Secondary", "Melee", "Building").
- **image** (string): Path to the weapon's image file in the `images/` folder.
- **stats** (object): Contains two arrays:
  - **positive** (array of strings): List of positive stat changes.
  - **negative** (array of strings): List of negative stat changes.
- **isConcept** (boolean): Set to `true` for new concepts, `false` for rebalances.

### Optional Fields

- **changes** (array of strings): List of specific changes made to the weapon. Can be empty `[]` for new concepts.
- **reasoning** (string): Explanation of the concept's design, balance, or purpose. Can be empty `""` for new concepts.

## Examples

### New Weapon Concept
```json
{
  "name": "Example Weapon",
  "class": "Flanker",
  "type": "Primary",
  "image": "images/example-weapon.png",
  "stats": {
    "positive": ["+25% faster firing speed", "On hit: Apply bleed for 5 seconds"],
    "negative": ["-20% damage penalty", "-15% clip size"]
  },
  "changes": [],
  "reasoning": "This weapon concept aims to provide Flanker with a new aggressive playstyle option.",
  "isConcept": true
}
```

### Weapon Rebalance
```json
{
  "name": "Existing Weapon",
  "class": "Soldier",
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

- **Be specific**: Use percentages or exact values (e.g., "+25% faster firing speed" instead of "faster firing").
- **Use standard terminology**: Follow TF2 stat conventions (e.g., "mini-crits", "crits", "blast jumping").
- **Balance is key**: Ensure positive and negative stats create an interesting trade-off.
- **Keep it concise**: Each stat should be a short, clear description.

## Image Requirements

- **Format**: PNG preferred, but JPG/JPEG acceptable.
- **Size**: Aim for 256x256 pixels or similar square dimensions.
- **Naming**: Use lowercase with hyphens (e.g., `my-weapon-concept.png`).
- **Content**: Should clearly represent the weapon concept. Reference existing TF2 weapon art styles.

## Validation

Before submitting:
1. Ensure the JSON is valid (use a JSON validator).
2. Check that the image path matches the file in `images/`.
3. Verify that all required fields are present and correctly formatted.
4. Test that the weapon displays properly in the application.

## Need Help?

If you have questions about contributing or need clarification on the format, feel free to open an issue or contact the maintainers.