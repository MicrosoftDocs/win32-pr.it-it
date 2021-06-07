---
title: UI_PKEY_ColorType
description: Identifica la proprietà \_ PKEY \_ ColorType dell'interfaccia utente.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443892"
---
# <a name="ui_pkey_colortype"></a>Tipo \_ di colore PKEY \_ dell'interfaccia utente

Identifica la proprietà \_ PKEY \_ ColorType dell'interfaccia utente.

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

Ui PKEY ColorType viene usato da un'applicazione per eseguire query sull'impostazione del \_ colore del controllo \_ [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

Il valore della proprietà deriva [**dall'enumerazione \_ SWATCHCOLORTYPE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) utente.



|    Proprietà                            |    Descrizione                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ SWATCHCOLORTYPE \_ NOCOLOR   | L'applicazione deve considerare l'impostazione del colore trasparente. Usato in genere insieme **all'impostazione Nessun colore.**                                                   |
| UI \_ SWATCHCOLORTYPE \_ AUTOMATIC | L'applicazione deve eseguire una query [su GetSysColor(COLOR \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor). In genere usato in combinazione con **l'impostazione Del** colore automatico. |
| RGB \_ SWATCHCOLORTYPE \_ dell'interfaccia utente       | L'applicazione deve eseguire una query [sul \_ colore PKEY \_ dell'interfaccia](windowsribbon-reference-properties-uipkey-color.md) utente per l'impostazione del colore.                                                          |



 

Ui PKEY ColorType viene passato al metodo \_ \_ di callback [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando viene selezionato un campione di colore in [**un controllo DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Selezione colori proprietà](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 