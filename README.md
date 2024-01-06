# ViewModifierKit

<p>
    <img src="https://img.shields.io/badge/iOS-13.0+-blue.svg" />
    <img src="https://img.shields.io/badge/macOS-10.15-gold.svg" />
    <img src="https://img.shields.io/badge/Swift-5.0-ff69b4.svg" />
</p>

----

> This package contains all the code to be able to add padding to any
SwiftUI view. The modifiers have an argument called `howMuch` if left
out then the modifier defaults to 10

----

## Features

### Padding Modifiers
-   bottomPadding
-   topPadding
-   allPadding
-   trailingPadding
-   leadingPadding
-   horizontalPadding
-   verticalPadding

#### Examples

```swift
var body: some View {
    Text("Bottom padding applied")
        .bottomPadding(howMuch: 5)

    Text("Top padding applied")
        .topPadding(howMuch: 5)
        
    Text("Generic padding applied")
        .allPadding(howMuch: 5)
        
    Text("Trailing padding applied")
        .trailingPadding(howMuch: 5)
        
    Text("Leading padding applied")
        .leadingPadding(howMuch: 5)
        
    Text("Horizontal padding applied")
        .horizontalPadding(howMuch: 5)
        
    Text("Vertical padding applied")
        .verticalPadding(howMuch: 5)
}
```

### Text View Modifiers
```
textViewModifier(for: , weight: , color: )
```

<ul>
<li>Font: Any Swift Font, Ex: .title</li>
<li>Weight: Any font weight, Ex: .bold</li>
<li>Color: Any SwiftUI Color, Ex: .primary</li>
</ul>

#### Example

```swift
var body: some View {
    Text("Bottom padding applied")
        .textViewModifier(for: .body, weight: .semibold, color: .primary)
}
```

### Image View Modifiers
```
imageViewModifier(color: , scale: )
```
<ul>
<li>Color: Any SwiftUI Color, Ex: .blue</li>
<li>Scale: Any Image.Scale, Ex: .fit</li>
</ul>

```
imageViewModifier(width: , height: , color: , ratio: , alignment: )
```
<ul>
<li>Width: CGFloat, Ex: 50</li>
<li>Height: CGFloat, Ex: 50</li>
<li>Color: Any SwiftUI Color, Ex: .blue</li>
</ul>

<ul>
<li>Ratio: Default value = .fit</li>
<li>Alignment: Default value = .center</li>
</ul>

```
imageViewModifier(width: , height: , color: , radius: , ratio: , alignment: )
```
<ul>
<li>Width: CGFloat, Ex: 50</li>
<li>Height: CGFloat, Ex: 50</li>
<li>Color: Any SwiftUI Color, Ex: .blue</li>
<li>Radius: CGFloat, Ex: 5.0e</li>
<li>Ratio: Default value = .fit</li>
<li>Alignment: Default value = .center</li>
</ul>

```
imageViewModifier(renderMode: .hierarchical, width: 50, height: 50, color: .orange, ratio: .fill, alignment: .center, radius: 5.0)
```
<ul>
<li>RenderMode: SymbolRenderingMode, Ex: .hierarchical</li>
<li>Width: CGFloat, Ex: 50</li>
<li>Height: CGFloat, Ex: 50</li>
<li>Color: Any SwiftUI Color, Ex: .blue</li>
<li>Ratio: Default value = .fit</li>
<li>Alignment: Default value = .center</li>
<li>Radius: CGFloat, Ex: 5.0e</li>
</ul>

#### Examples

```swift
VStack {
	Image(systemName: "globe")
		.imageViewModifier(color: .blue, scale: .medium)

	Image(systemName: "globe")
		.imageViewModifier(width: 50, height: 50, color: .red)

	Image(systemName: "globe")
		.imageViewModifier(width: 50, height: 50, color: .red, ratio: .fit, alignment: .center)

	Image(systemName: "square")
		.imageViewModifier(width: 50, height: 50, color: .yellow, radius: 5.0)

	Image(systemName: "square")
		.imageViewModifier(width: 50, height: 50, color: .orange, radius: 5.0, ratio: .fit, alignment: .center)

	Image(systemName: "square.text.square")
		.imageViewModifier(renderMode: .hierarchical, width: 50, height: 50, color: .blue)

	Image(systemName: "square.text.square")
		.imageViewModifier(renderMode: .hierarchical, width: 50, height: 50, color: .orange, ratio: .fill, alignment: .center, radius: 5.0)
}
```

## Installation

The code is packaged as a framework. You can install manually (by copying the files in the `Sources` directory) or using Swift Package Manager (**preferred**)

### Dependency For Another Swift Package
To install using Swift Package Manager, add this to the `dependencies` section of your `Package.swift` file:
`.package(url: "https://github.com/tazmancoder/ViewModifierKit.git", .upToNextMinor(from: "1.0.0"))`

### Xcode project
To install this into your Xcode project, follow the instructions below:

1. Goto your project folder, tap Package Dependencies, under Packages click the plus button
2. Enter this in searchbar - `https://github.com/tazmancoder/ViewModifierKit.git`. 
3. Set `Dependency Rule` to `Up to Next Major Version`
4. Tap `Add Package` button.

Thats it this package will then be installed and ready to use.

> Note: The package requires iOS v13.0+ or macOS v10.15+




