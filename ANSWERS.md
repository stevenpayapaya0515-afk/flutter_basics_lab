1. Your GitHub repository link (Step 3).
https://github.com/stevenpayapaya0515-afk/flutter_basics_lab.git

2. The last three build() called lines from Activity 2.
build() called: 1 glasses
build() called: 2 glasses
build() called: 3 glasses

3. Your observations from the experiments in Activities 2, 3 and 5.

Activity 2 – Water Tracker: I observed that when I clicked the add or remove button, the number of glasses and progress indicator changed. The setState() method updates the interface when the value changes. The Debug Console also showed that the build() method was called again when the widget rebuilt.

Activity 3 – Weather Dashboard: I observed that Row arranges widgets horizontally, while Column arranges them vertically. The Expanded widget helps the stat boxes share the available space. When I removed Expanded, the layout could become uneven or cause overflow.

Activity 5 – Settings Page: I observed that ThemeData can customize the overall appearance of the app. The light and dark modes changed the interface colors, while widgets such as Card, ListTile, and Chip helped organize and display the settings.


Review questions:
1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each from this lab.

A StatelessWidget does not store changing data that updates the UI, while a StatefulWidget can update the UI when its data changes. An example of a StatelessWidget is the ProfileCard in Activity 1, while the WaterTrackerPage in Activity 2 is a StatefulWidget.

2. Why is a StatefulWidget written as two classes? What does each class do?

A StatefulWidget uses two classes to separate the widget's structure from its changing data. The first class creates the widget, while the State class stores the data and updates the UI when the data changes.

3. In Activity 2, what happened when you changed _glasses outside setState()? Why?

When I changed `_glasses` outside `setState()`, the number did not update on the screen immediately. This happened because Flutter was not notified that the data had changed, so it did not rebuild the UI.

4. Looking at the Debug Console in Activity 2, when is build() called?

The `build()` method is called when Flutter creates the screen and whenever the widget needs to be rebuilt. In Activity 2, it is called again when I add or remove a glass or reset the tracker using `setState()`.

5. Explain the main axis and the cross axis of a Row and of a Column.

In a Row, the main axis is horizontal, while the cross axis is vertical. In a Column, the main axis is vertical, while the cross axis is horizontal. These axes determine how the widgets are arranged on the screen.

6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?

Without Expanded, a box no longer shares the available row space equally with the other boxes. Expanded helps distribute the available space among the widgets in a Row or Column.

7. Why do we use GridView.builder for the menu instead of a Column with many children?

GridView.builder arranges items in a grid and builds them as needed while scrolling. A Column arranges its children vertically.

8. How do Stack and Positioned create the Best seller badge in Activity 4?

Stack allows widgets to overlap. Positioned places a widget at a specified position inside the stack, such as the best-seller badge near the top-left corner of a menu card.

9. What is the difference between customizing with ThemeData and with a style on one widget? Give one example of each from Activity 5.

ThemeData sets the overall appearance of the app and its components. TextStyle controls the appearance of specific text, such as its size, weight, and color.

10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the change reach MaterialApp?

The _ThemeDemoAppState class stores the _isDark value. When the switch changes, the callback updates the value using setState(). The MaterialApp then uses ThemeMode.dark or ThemeMode.light based on that value.

