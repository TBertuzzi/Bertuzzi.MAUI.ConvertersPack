# XBertuzzi.MAUI.ConvertersPack

Package with multiple converters for MAUI.
 
###### This is the component, works on iOS, Android and UWP.

**NuGet**

|Name|Info|
| ------------------- | :------------------: |
|Xamarin.Forms.ConvertersPack|[![NuGet](https://buildstats.info/nuget/Bertuzzi.MAUI.ConvertersPack)](https://www.nuget.org/packages/Bertuzzi.MAUI.ConvertersPack/)|

**Platform Support**

Bertuzzi.MAUI.ConvertersPack is a MAUI library.

## Setup / Usage

Does not require additional configuration. Just install the package in the shared project and use.

You just need to add the reference in your xaml file.

```csharp
    xmlns:converterPack="clr-namespace:Bertuzzi.MAUI.ConvertersPack;assembly=Bertuzzi.MAUI.ConvertersPack"
```

```csharp
     <ContentPage.Resources>
        <ResourceDictionary>
         <converterPack:CurrencyConverter x:Key="CurrencyConverter" />
         <converterPack:UpperTextConverter x:Key="UpperTextConverter" />
        <converterPack:LowerTextConverter x:Key="LowerTextConverter" />
        </ResourceDictionary>
    </ContentPage.Resources>
    
    <StackLayout>

         <Label Text="Enter your name"></Label>
        
         <Entry Placeholder="Your name" Text="{Binding Name}"></Entry>
        
         <Label Text="{Binding Name, Converter={StaticResource UpperTextConverter}}"></Label>
        
         <Label Text="{Binding Name, Converter={StaticResource LowerTextConverter}}"></Label>
        
         <Label Text="Enter your balance"></Label>
        
         <Entry Placeholder="Money" 
              Keyboard="Numeric" 
              Text="{Binding Money, Converter={StaticResource CurrencyConverter}}"></Entry>
        
    </StackLayout>

```

**Available Converters**

* **CurrencyConverter** : Converts your entry to a money field.
* **DecimalConverter** : Decimal Converter.
* **EqualsConverter** : Compare if two fields are the equals.
* **HasDataConverter** : Returns whether an object or a list has data.
* **HexToColorConverter** : Converts hexadecimal to color.
* **ImageFromByteArrayConverter** : Converts an array of bytes to Image.
* **ImageFromFileConverter** : Converts an image from a local repository to Image.
* **InvertedBooleanConverter** : Invert the value of a boolean.
* **ItemTappedEventArgsConverter** : Converts a selected item to an object. Ideal for Listview.
* **LowerTextConverter** : Converts your text to lowercase.
* **NullToBooleanConverter** : Checks the value if it is null and returns true or false.
* **UpperTextConverter** : Converts your text to uppercase.


The complete example can be downloaded here: <https://github.com/TBertuzzi/Xamarin.Forms.ConvertersPack/tree/master/MAUIConvertersPack>
