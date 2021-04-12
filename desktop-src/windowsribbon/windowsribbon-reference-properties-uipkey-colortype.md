---
title: UI_PKEY_ColorType
description: Identifica la proprietà ColorType dell'interfaccia utente \_ pkey \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338230"
---
# <a name="ui_pkey_colortype"></a>Interfaccia utente \_ pkey \_ ColorType

Identifica la proprietà ColorType dell'interfaccia utente \_ pkey \_ .

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ ColorType viene usata da un'applicazione per eseguire una query sull'impostazione del colore del controllo [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .

Il valore della proprietà è dall' [**enumerazione \_ SWATCHCOLORTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| interfaccia utente \_ SWATCHCOLORTYPE \_ nocolor   | L'applicazione deve considerare l'impostazione del colore come trasparente. Viene in genere usato in combinazione con l'impostazione colori **Nessun** colore.                                                   |
| interfaccia utente \_ SWATCHCOLORTYPE \_ automatica | L'applicazione deve eseguire una query su [GetSysColor (Color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor). Viene in genere usato in combinazione con l'impostazione colore **automatica** . |
| interfaccia utente \_ SWATCHCOLORTYPE \_ RGB       | L'applicazione deve eseguire una query sul [ \_ \_ colore pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-color.md) per l'impostazione del colore.                                                          |



 

L'interfaccia utente \_ pkey \_ ColorType viene passata al metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback quando viene selezionato un campione di colore in un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà selezione colori](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 