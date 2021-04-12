---
title: UI_PKEY_ThemeColors
description: Identifica la proprietà ThemeColors dell'interfaccia utente \_ pkey \_ .
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337774"
---
# <a name="ui_pkey_themecolors"></a>Interfaccia utente \_ pkey \_ ThemeColors

Identifica la proprietà ThemeColors dell'interfaccia utente \_ pkey \_ .

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ ThemeColors viene usata da un'applicazione per eseguire una query sui valori dei campioni di colore di un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Ogni valore di [COLORREF](../gdi/colorref.md) corrisponde a un campione di colore in un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) in cui `ThemeColors` viene specificato come valore dell'attributo **ColorTemplate** .

Il valore della proprietà è una matrice di valori [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà selezione colori](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 