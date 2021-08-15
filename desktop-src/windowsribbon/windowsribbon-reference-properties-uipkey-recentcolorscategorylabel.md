---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifica la proprietà \_ \_ RecentColorsCategoryLabel dell'interfaccia utente PKEY.
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f3a7a513afb50f01ee3a03c3a3240a2eae7a6ed7b6b8228c4a49e7343e052e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031476"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ PKEY \_ RecentColorsCategoryLabel

Identifica la proprietà \_ \_ RecentColorsCategoryLabel dell'interfaccia utente PKEY.

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Commenti

L'interfaccia utente PKEY RecentColorsCategoryLabel viene usata da un'applicazione per eseguire una query sul valore dell'etichetta associata alla categoria \_ \_ Colori **recenti** di un [**controllo DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

UI PKEY RecentColorsCategoryLabel è valida solo per \_ \_ un controllo [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) in cui è specificato come valore dell'attributo `ThemeColors` **ColorTemplate** (questo è l'unico modello che contiene categorie etichettate).

Lo screenshot seguente mostra un `ThemeColors` [**controllo DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

![Screenshot dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su themecolors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Selezione colori proprietà](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




