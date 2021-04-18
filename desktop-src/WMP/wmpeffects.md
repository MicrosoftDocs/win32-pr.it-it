---
title: WMPEFFECTS
description: Si tratta di effetti predefiniti con i seguenti valori predefiniti.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- Media Player Windows WMPEFFECTS
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db3e35143242c5ca7888ffc50feb006f586e68d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329677"
---
# <a name="wmpeffects"></a>WMPEFFECTS

Si tratta di **effetti** predefiniti con i seguenti valori predefiniti.

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a>Commenti

Verrà creato un elemento **Effects** che eseguirà l'istruzione nei set di impostazioni di visualizzazione quando l'utente fa clic sul controllo. Si estenderanno anche le visualizzazioni quando il lettore viene ridimensionato.

Il set di impostazioni di visualizzazione iniziale visualizzato è quello selezionato nel menu **Visualizza** in **visualizzazioni**. Se si modifica la selezione in questo menu, il set di impostazioni visualizzato da questo elemento verrà modificato automaticamente quando il lettore è in modalità Skin. Il menu **Visualizza** viene visualizzato nella modalità completa del lettore o quando l'attributo **View. barra** del titolo è impostato su true in un'interfaccia personalizzata.

È possibile eseguire l'override di tutte le proprietà di questo elemento **Effects** specificandone le proprietà in modo esplicito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 7,0 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> </dl>

 

 





