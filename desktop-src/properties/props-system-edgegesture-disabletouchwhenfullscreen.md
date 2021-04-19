---
description: Impedisce comportamenti dei movimenti di bordo quando una finestra dell'applicazione è attiva e in modalità schermo intero (oppure è attiva una finestra di proprietà).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. EdgeGesture. DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317993"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System. EdgeGesture. DisableTouchWhenFullscreen

Impedisce comportamenti dei movimenti di bordo quando una finestra dell'applicazione è attiva e in modalità schermo intero (oppure è attiva una finestra di proprietà).

> [!Note]  
> In modalità schermo intero, le dimensioni della finestra dell'applicazione corrispondono alla risoluzione dello schermo.

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Commenti

In Windows 8 le interazioni utente con i bordi dello schermo visualizzano l'interfaccia utente del sistema, ad esempio le barre dell'app, gli accessi e le app in esecuzione.

Per le applicazioni remote a schermo intero, questo comportamento dell'interfaccia utente nel computer locale potrebbe sostituire e interferire con l'interfaccia utente della sessione remota. Questa proprietà consente a un'applicazione di disabilitare l'interfaccia utente perimetrale nel computer locale.

Per disabilitare l'interfaccia utente di Edge, impostare questa proprietà su VARIANT \_ true. Il valore predefinito è VARIANT \_ false.

Questa proprietà non ha alcun effetto sulle app di Windows Store.

Nell'esempio seguente viene illustrato come impostare i comportamenti dell'interfaccia utente di Edge.


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
