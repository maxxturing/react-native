# react-native

### Resource Links

- https://www.youtube.com/watch?v=OxIDLw0M-m0&list=PL4cUxeGkcC9ij8CfkAY2RAGb-tmkNwQHG
- https://www.youtube.com/watch?v=ur6I5m2nTvk&list=PL4cUxeGkcC9ixPU-QkScoRBVxtPPzVjrQ
  - https://github.com/iamshaunjp/react-native-tutorial
- https://github.com/hsavit1/Awesome-React-Native-Education
- https://expo.io/
- https://youtu.be/PuRIMFWVZ1M?t=259
- https://facebook.github.io/react-native/docs/getting-started
- https://facebook.github.io/react-native/docs/tutorial
- https://github.com/facebook/create-react-app

* React Native allows us to use the React library to create mobile apps (Android & iOS)
* It's best to understand core principles of React first
  - Functional components
  - State
  - Props
  - React hooks (useState hook) https://reactjs.org/docs/hooks-reference.html#usestate
* Works similar to React for web
  - Create an app by building a component tree
  - React Native takes components and compiles them into native code and widgets that work on Android and iOS
* Install node https://nodejs.org/en/download/
* Command Line Interface
  - Expo CLI
    - A wrapper that is better for beginners, allows for easy access to certain features
    - Less flexibility
  - React Native CLI
    - More fine-grain control, more complex
    - Can switch to RN CLI by ejecting project from Expo
* Install Expo CLI https://expo.io/learn
  ```sh
  npm install expo-cli --global
  ```
* Create your project
  ```sh
  expo init myproject
  ```
* Choose blank project
* Install with npm
* Move into directory
  ```sh
  cd myproject
  ```
* Open in Microsoft Visual Studio Code
  ```sh
  code .
  ```
* Get started (opens tab in browser with expo's debug tools)
  ```sh
  npm start
  ```
* Download expo client on phone and use QR code to preview app https://play.google.com/store/apps/details?id=host.exp.exponent
* Install Android Studio https://developer.android.com/studio
  - Click Configure and select AVD Manager
  - Select your phone
  - Download Pie (API level 28)
  - Click Next
  - Click Finish
  - Click Play button icon
* Project files overview
  - .expo - expo configuration/settings
  - .expo-shared - expo configuration/settings
  - assets - images
  - node_modules - dependencies
  - .gitignore - which files not to track for version control
  - App.js - kickstarts the app
  - app.json - information about project
  - babel.config.js - configuring how babel (compiler) works
  - package-lock.json - track dependencies
  - package.json - track dependencies
* Components
  - View
  - Text
  - Constants
    - Styles (aren't inherited, apart from Text within Text)
* React Hooks
  - Give us a way to use special functions in the React library
* State
  - useState hook
    - Use a state within a functional component
    - import from the React library
    - const [name, setName] = useState("shaun");
  -
* Button
  - Import Button from react native
  - Set a clickHandler for name/age change
    - `<Button title="Update Name" onPress={clickHandler} />`
    - `const clickHandler = () => { setName(); };`
* TextInput
  - multiline prop (multiple lines in input)
  - placeholder prop
    - `placeholder="e.g. John Smith"`
  - onChangeText prop
    - `onChangeText={val => setName(val)}`
    - `const [name, setName] = useState();`
    - `onChangeText={val => setAge(val)}`
    - `const [age, setAge] = useState();`
  - keyboardType
    - `keyboardType="numeric"`
* Lists
  - List
  - ```sh
    {people.map(item => {
          return (
            <View ket={item.key}>
              <Text>{item.name}</Text>
            </View>
          );
        })}
    ```
  - ```sh
      const [people, setPeople] = useState([
        { name: "maxxwell", id: "1" },
        { name: "jack", id: "2" },
        { name: "mia", id: "3" },
        { name: "nico", id: "4" },
        { name: "luke", id: "5" },
        { name: "hentie", id: "6" },
        { name: "cyril", id: "7" },
        { name: "pravin", id: "8" },
        { name: "fouzan", id: "9" },
        { name: "pete", id: "10" },
        { name: "kazuya", id: "11" }
      ]);
    ```
  - ScrollView component
  - FlatList Component
    - Renders as scrolling
    - Doesn't require specifying key property
    - keyExtractor
      - Use different property for id
    - numColumns
  - TouchableOpacity component
    - Makes it touchable
    - ```sh
      renderItem={({ item }) => (
          <TouchableOpacity onPress={() => pressHandler(item.id)}>
            <Text style={styles.item}>{item.name}</Text>
          </TouchableOpacity>
        )}
      />
      ```
      ```sh
      const pressHandler = id => {
        console.log(id);
        setPeople(prevPeople => {
          return prevPeople.filter(person => person.id != id);
        });
      };
      ```
* Todo App
  - ```sh
    export default function TodoItem({ item, pressHandler }) {
      return (
        <TouchableOpacity onPress={() => pressHandler(item.key)}>
          <Text style={styles.item}>{item.text}</Text>
        </TouchableOpacity>
      );
    }
    ```
* Flexbox
  - flexDirection: 'row'
  - justifyConten: 'space-around'
  - alignItems
    - flex-start
    - flex-end
    - center
  - flex
* Icons
  - Import
    ```sh
    import { MaterialIcons } from "@expo/vector-icons";
    ```
* Custom Fonts

  - https://docs.expo.io/versions/latest/guides/using-custom-fonts/
  - ```sh
    export default class App extends React.Component {
      componentDidMount() {
        Font.loadAsync({
          "open-sans-bold": require("./assets/fonts/OpenSans-Bold.ttf")
        });
      }

      // ...
    }
    ```

  - ```sh
    const getFonts = () =>
      Font.loadAsync({
        "nunito-regular": require("./assets/fonts/Nunito-Regular.ttf"),
        "nunito-bold": require("./assets/fonts/Nunito-Bold.ttf")
      });

    export default function App() {
      const [fontsLoaded, setFontsLoaded] = useState(false);

      if (fontsLoaded) {
        return <Home />;
      } else {
        return (
          <AppLoading startAsync={getFonts} onFinish={() => setFontsLoaded(true)} />
        );
      }
    }
    ```

  - ```sh
      const styles = StyleSheet.create({
        titleText: {
          fontFamily: "nunito-bold",
          fontSize: 18
        }
      });
    ```

    ```

    ```

* Navigation
  - Difference types of Stack
    - Stack navigation
    -
  - https://reactnavigation.org/
    - https://reactnavigation.org/docs/en/getting-started.html
      - npm install react-navigation
      - expo install react-native-gesture-handler react-native-reanimated react-native-screens react-native-safe-area-context @react-native-community/masked-view
  - npm install react-navigation-stack
  - routes/homeStack.js
    - `navigation.navigate("ReviewDetails");`
    - `navigation.push("ReviewDetails");`
  - ```sh
        export default function Home({ navigation }) {
      const pressHandler = () => {
        navigation.navigate("ReviewDetails");
        // navigation.push("ReviewDetails");
      };
    ```
  - ```sh
      export default function ReviewDetails({ navigation }) {
    const pressHandler = () => {
      navigation.goBack();
    };
    ```
  - navigationOptions
    - ```sh
      const HomeStack = createStackNavigator(screens, {
        defaultNavigationOptions: {
          headerTintColor: "white",
          headerStyle: {
            backgroundColor: "#1E67FC",
            height: 150
          }
        }
      });
      ```
  - Drawer navigation
    - npm install react-navigation-drawer
* Cards
* Modals
* Formik
  - npm install formik
  - npm install yup
* yup - form validation / errors
* Dev tools
  - https://www.npmjs.com/package/react-devtools
  - ```sh
    REACT_DEBUGGER="unset ELECTRON_RUN_AS_NODE && open -g 'rndebugger://set-debugger-loc?port=19001' ||" npm start
    ```
