---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la proprietà \_ FontProperties ForegroundColorType dell'interfaccia \_ \_ utente PKEY.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444352"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ PKEY \_ FontProperties \_ ForegroundColorType

Identifica la proprietà \_ FontProperties ForegroundColorType dell'interfaccia \_ \_ utente PKEY.

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Commenti

UI PKEY FontProperties ForegroundColorType viene usato da un'applicazione, insieme a \_ \_ UI \_ [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), per eseguire query **nelle impostazioni della** raccolta colori del testo.

Il valore della proprietà deriva [**dall'enumerazione \_ SWATCHCOLORTYPE dell'interfaccia**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) utente.

Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.

Nella tabella seguente vengono descritti i valori delle proprietà.



|     Valore                           |     Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Non supportato da [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | L'applicazione deve eseguire una query sulla metrica  di sistema appropriata per il valore del colore in genere il colore corrente del testo del tema di Windows recuperato con GetSysColor(COLOR \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | L'applicazione deve eseguire una query [ \_ PKEY \_ FontProperties \_ ForegroundColor dell'interfaccia](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) utente per il valore del colore. Il valore del colore [dell'interfaccia utente \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) viene visualizzato nel pulsante **Colore** testo e selezionato nella **raccolta colori** testo.<br/> |



 

Ui PKEY FontProperties ForegroundColorType viene passato al metodo \_ \_ di callback \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando viene selezionato un campione di colore in una raccolta colori [**FontControl**](windowsribbon-element-fontcontrol.md) Text.

> [!Note]  
> È altamente consigliabile che l'applicazione imposta solo un valore iniziale di colore testo e non ri-impostare questo valore quando il cursore viene riposizionato all'interno di un documento.  L'ultima selezione deve essere mantenuta per evitare la necessità di selezionare nuovamente il colore desiderato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_SWATCHCOLORTYPE DELL'INTERFACCIA UTENTE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controllo Carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

