---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica la proprietà \_ FontProperties BackgroundColorType dell'interfaccia \_ \_ utente PKEY.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443822"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ BackgroundColorType

Identifica la proprietà \_ FontProperties BackgroundColorType dell'interfaccia \_ \_ utente PKEY.

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

UI PKEY FontProperties BackgroundColorType viene usato da un'applicazione, in combinazione con UI \_ \_ \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor,](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)per eseguire query nelle impostazioni della raccolta colori **evidenziazione** testo.

Il valore della proprietà deriva [**dall'enumerazione \_ SWATCHCOLORTYPE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) utente.

Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.

Nella tabella seguente vengono descritti i valori delle proprietà.



|   Proprietà                             |   Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | L'applicazione deve eseguire una query sulla metrica  di sistema appropriata per il valore del colore in genere il colore di sfondo corrente della finestra del tema di Windows recuperato con GetSysColor(COLOR \_ WINDOW).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Non supportato da [**FontControl.**](windowsribbon-element-fontcontrol.md)                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | L'applicazione deve eseguire una query [ \_ dell'interfaccia utente PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) per il valore del colore. Il valore del colore [dell'interfaccia utente \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) viene visualizzato nel pulsante **Colore** evidenziazione testo e selezionato nella raccolta colori **evidenziazione** testo.<br/> |



 

UI PKEY FontProperties BackgroundColorType viene passato al metodo \_ \_ di callback \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando viene selezionato un campione di colore in una raccolta colori di evidenziazione del testo [**FontControl.**](windowsribbon-element-fontcontrol.md)

> [!Note]  
> È consigliabile che l'applicazione  imposta solo un valore iniziale per il colore di evidenziazione testo e non lo riposiziona quando il cursore viene riposizionato all'interno di un documento. L'ultima selezione deve essere mantenuta per evitare la necessità di selezionare nuovamente il colore desiderato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_SWATCHCOLORTYPE DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

