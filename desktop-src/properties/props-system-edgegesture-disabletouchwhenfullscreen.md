---
description: Impedisce i comportamenti del movimento del bordo quando una finestra dell'applicazione è attiva e in modalità schermo intero (o una finestra di proprietà è attiva).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System.EdgeGesture.DisableTouchWhenFullscreen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13132ba30fd3f1e594ec54966dfe2268ce66d570b66ca6d34b1c63b03bfc0c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845121"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System.EdgeGesture.DisableTouchWhenFullscreen

Impedisce i comportamenti del movimento del bordo quando una finestra dell'applicazione è attiva e in modalità schermo intero (o una finestra di proprietà è attiva).

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

In Windows 8, le interazioni dell'utente con i bordi dell'interfaccia utente del sistema di visualizzazione dello schermo, ad esempio le barre dell'app, gli accessi e le app in esecuzione.

Per le applicazioni remote a schermo intero, questo comportamento dell'interfaccia utente nel computer locale potrebbe sostituire e interferire con l'interfaccia utente della sessione remota. Questa proprietà consente a un'applicazione di disabilitare l'interfaccia utente perimetrale nel computer locale.

Per disabilitare l'interfaccia utente perimetrale, impostare questa proprietà su VARIANT \_ TRUE. Il valore predefinito è VARIANT \_ FALSE.

Questa proprietà non ha alcun effetto sulle Windows Store.

L'esempio seguente illustra come impostare i comportamenti dell'interfaccia utente perimetrali.


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

[proprietàDescrizione](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
