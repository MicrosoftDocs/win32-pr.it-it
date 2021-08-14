---
title: UI_PKEY_ThemeColors
description: Identifica la proprietà \_ PKEY \_ ThemeColors dell'interfaccia utente.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5c4582561e3c86ba19b2821cf600d0a1da614cfc9fc7144b935665c8af7f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437796"
---
# <a name="ui_pkey_themecolors"></a>\_ThemeColors PKEY \_ dell'interfaccia utente

Identifica la proprietà \_ PKEY \_ ThemeColors dell'interfaccia utente.

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

L'interfaccia utente PKEY ThemeColors viene usata da un'applicazione per eseguire query nei valori dei campioni \_ di colore di un controllo \_ [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

Ogni [valore COLORREF](../gdi/colorref.md) corrisponde a un campione di colore in [**un controllo DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) dove è specificato come `ThemeColors` valore **dell'attributo ColorTemplate.**

Il valore della proprietà è una matrice di [valori COLORREF.](../gdi/colorref.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Selezione colori proprietà](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 