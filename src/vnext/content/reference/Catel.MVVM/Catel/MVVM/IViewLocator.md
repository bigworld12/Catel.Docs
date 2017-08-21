

# IViewLocator

Name|Value
---|---
Assembly|Catel.MVVM
Namespace|Catel.MVVM
Available on|.NET Framework 4.5, .NET Framework 4.6, Portable Class Libraries, Unknown, Windows 10.0 (Universal Apps), Xamarin - Android, Xamarin - iOS

```
public interface IViewLocator : ILocator
```

**Base types**

[ILocator](/Catel.MVVM\Catel\MVVM\ILocator.md)


Resolver that will resolve view types based on the view model type. For example, if a view model with the type name`MyAssembly.ViewModels.PersonViewModel` is inserted, this could result in the view type`MyAssembly.Views.PersonView`.



## Methods

### Register(Type viewModelType, Type viewType)

Registers the specified view in the local cache. This cache will also be used by the Type) method.

#### Parameters

**viewModelType**
Type of the view model.

**viewType**
Type of the view.

#### Exceptions

**T:System.ArgumentNullException**
The viewModelType is`null`.



### ResolveView(Type viewModelType)

Resolves a view type by the view model and the registered NamingConventions.

#### Parameters

**viewModelType**
Type of the view model to resolve the view for.

#### Returns

The resolved view or`null` if the view could not be resolved.

#### Exceptions

**T:System.ArgumentNullException**
The viewModelType is`null`.

#### Remarks

Keep in mind that all results are cached. The cache itself is not automatically cleared when the NamingConventions are changed. If the NamingConventions are changed, the cache must be cleared manually.


