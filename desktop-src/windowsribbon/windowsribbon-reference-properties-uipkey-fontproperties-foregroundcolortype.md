---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica la \_ \_ Proprietà ForegroundColorType FontProperties di pkey dell'interfaccia utente \_ .
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399282"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>Interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColorType

Identifica la \_ \_ Proprietà ForegroundColorType FontProperties di pkey dell'interfaccia utente \_ .

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

L'interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColorType viene usata da un'applicazione, in combinazione con l' [interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), per eseguire query sulle impostazioni della raccolta **colori del testo** .

Il valore della proprietà è dall' [**enumerazione \_ SWATCHCOLORTYPE dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

Il valore predefinito è `UI_SWATCHCOLORTYPE_RGB`.

Nella tabella seguente vengono descritti i valori delle proprietà.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Non supportato da [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | L'applicazione deve eseguire una query sulla metrica di sistema appropriata per il valore di colore in genere il colore corrente del **testo** del tema Windows recuperato con GETSYSCOLOR (Color \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | L'applicazione deve eseguire una query sull' [interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) per il valore del colore. Il valore del colore dell' [interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) viene visualizzato sul pulsante **colore testo** e selezionato nella raccolta **colori testo** .<br/> |



 

L'interfaccia utente \_ pkey \_ FontProperties \_ ForegroundColorType viene passata al metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback quando viene selezionato un campione di colore in una raccolta **colori del testo** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> È consigliabile che l'applicazione imposti solo un valore di **colore del testo** iniziale e non imposti nuovamente questo valore quando il cursore viene riposizionato all'interno di un documento. L'ultima selezione deve essere mantenuta per evitare di dover selezionare di nuovo il colore desiderato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interfaccia utente \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controllo carattere](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

