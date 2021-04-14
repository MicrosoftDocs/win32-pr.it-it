---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la \_ \_ Proprietà BackgroundColorType FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473267"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>Interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColorType

Identifica la \_ \_ Proprietà BackgroundColorType FontProperties di pkey dell'interfaccia utente \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Commenti

L'interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColorType viene utilizzata da un'applicazione, insieme all' [interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), per eseguire query sulle impostazioni della raccolta **colori di evidenziazione del testo** .

Il valore della proprietà è dall' [**enumerazione \_ SWATCHCOLORTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.

Nella tabella seguente vengono descritti i valori delle proprietà.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | L'applicazione deve eseguire una query sulla metrica di sistema appropriata per il valore del colore in genere il **colore di sfondo della finestra** del tema Windows corrente che viene recuperato con GetSysColor (finestra dei colori \_ ).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Non supportato da [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | L'applicazione deve eseguire una query sull' [interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) per il valore del colore. Il valore del colore dell' [interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) viene visualizzato sul pulsante **colore di evidenziazione del testo** e selezionato nella raccolta colori di **evidenziazione del testo** .<br/> |



 

L'interfaccia utente \_ pkey \_ FontProperties \_ BackgroundColorType viene passata al metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback quando viene selezionato un campione di colore in una raccolta **colori di evidenziazione del testo** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> È consigliabile che l'applicazione imposti solo un valore di **colore di evidenziazione del testo** iniziale e non imposti nuovamente questo valore quando il cursore viene riposizionato all'interno di un documento. L'ultima selezione deve essere mantenuta per evitare di dover selezionare di nuovo il colore desiderato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

