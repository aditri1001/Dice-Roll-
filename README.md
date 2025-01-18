# Dice Roller App 🎲  

A simple and interactive dice roller app built using React Native. This app provides a fun way to roll a dice, accompanied by haptic feedback for an engaging user experience.  

---

## Features ✨
- Roll a dice with a single tap.
- Displays dice face based on the random number (1-6).
- Haptic feedback to enhance user interaction.
- Smooth animations and visually pleasing UI.

---

## Demo 📱
| Roll the dice and feel the excitement with dynamic visuals and haptic feedback!

![Dice Roller App Demo](demo.gif) *(You can include a screen recording of the app running)*

---

## Installation 🚀

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/dice-roller-app.git
   cd dice-roller-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Install required libraries for the app:
   ```bash
   npm install react-native-haptic-feedback
   ```

4. Link native dependencies (only required for older versions of React Native):
   ```bash
   npx react-native link react-native-haptic-feedback
   ```

5. Run the app:
   ```bash
   npx react-native run-android  # For Android
   npx react-native run-ios      # For iOS
   ```

---

## Dependencies 📦

The following dependencies are required for this project:

1. **React Native**: Core framework for building mobile apps.
   - [Official Website](https://reactnative.dev/)

2. **react-native-haptic-feedback**: Provides haptic feedback for enhancing user experience.
   - Installation:
     ```bash
     npm install react-native-haptic-feedback
     ```
   - [GitHub Repository](https://github.com/mkuczera/react-native-haptic-feedback)

---

## Code Overview 🛠️

### Dice Component
The `Dice` component takes an image source as a prop and renders the corresponding dice face.

```tsx
type DiceProps = PropsWithChildren<{
  imageUrl: ImageSourcePropType;
}>;
```

### Rolling the Dice
The `rollDiceOnTap` function generates a random number (1-6), maps it to the appropriate dice image, and triggers a haptic feedback event.

```tsx
const rollDiceOnTap = () => {
  let randomNumber = Math.floor(Math.random() * 6) + 1;
  // Logic for setting the dice image based on the random number
  ReactNativeHapticFeedback.trigger("notificationWarning", options);
};
```

---

## File Structure 📂

```
src/
├── assets/
│   ├── One.png
│   ├── Two.png
│   ├── Three.png
│   ├── Four.png
│   ├── Five.png
│   └── Six.png
├── components/
│   └── Dice.tsx
├── App.tsx
└── styles.ts
```

---

## Screenshots 📸
### Default State:
![Default State](https://github.com/user-attachments/assets/a6e1c383-a7f4-42df-956c-2d6ce99c89bc)


### After Dice Roll:
![After Dice Roll](https://github.com/user-attachments/assets/78984cc9-f61d-40da-9696-a092cf6c5874)


---

## Contributing 🤝
Contributions are welcome! Feel free to:
- Fork the repository
- Create a new branch
- Submit a pull request


---

## Acknowledgements 🙌
- [React Native](https://reactnative.dev/)
- [react-native-haptic-feedback](https://github.com/mkuczera/react-native-haptic-feedback)
