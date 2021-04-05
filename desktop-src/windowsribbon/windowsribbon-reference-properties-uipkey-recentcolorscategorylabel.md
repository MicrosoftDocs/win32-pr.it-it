---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifica la proprietà RecentColorsCategoryLabel dell'interfaccia utente \_ pkey \_ .
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712031"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>Interfaccia utente \_ pkey \_ RecentColorsCategoryLabel

Identifica la proprietà RecentColorsCategoryLabel dell'interfaccia utente \_ pkey \_ .

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

L'interfaccia utente \_ pkey \_ RecentColorsCategoryLabel viene utilizzata da un'applicazione per eseguire una query sul valore dell'etichetta associata alla categoria **colori recenti** di un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

UI \_ pkey \_ RecentColorsCategoryLabel è valido solo per un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) `ThemeColors` in cui viene specificato come valore dell'attributo **ColorTemplate** (questo è l'unico modello che contiene le categorie con etichetta).

Lo screenshot seguente mostra un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![screenshot dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su ThemeColors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà selezione colori](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




