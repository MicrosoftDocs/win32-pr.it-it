---
title: WMPEFFECTS
description: Si tratta di un effects predefinito con i valori predefiniti seguenti.
ms.assetid: ebee17e3-96b0-4748-b69f-4ff41d0bc386
keywords:
- WMPEFFECTS Windows Media Player
topic_type:
- apiref
api_name:
- WMPEFFECTS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e84f33833e9d69c39cb50ff81bd6c97ff8f79d1e2f881f82d6e4d293e78d87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761271"
---
# <a name="wmpeffects"></a>WMPEFFECTS

Si tratta di un **effects predefinito** con i valori predefiniti seguenti.

``` syntax
horizontalAlignment="stretch"
verticalAlignment="stretch"
height="200"
width="250"
tabStop="false"
onclick="next();"
```

## <a name="remarks"></a>Commenti

Verrà creato un elemento **EFFECTS che** consente di scorrere i set di impostazioni di visualizzazione quando l'utente fa clic sul controllo. Estenderà anche le visualizzazioni quando il lettore viene ridimensionato.

Il set di impostazioni di visualizzazione iniziale visualizzato è quello selezionato nel menu **Visualizza** in **Visualizzazioni.** La modifica della selezione in questo menu modificherà automaticamente il set di impostazioni visualizzato da questo elemento quando il lettore è in modalità interfaccia. Il menu **Visualizza** viene visualizzato nella modalità completa del lettore o quando l'attributo **VIEW.titleBar** è impostato su true in un'interfaccia.

È possibile eseguire **l'override** di tutte le proprietà di questo elemento EFFECTS specificandole in modo esplicito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 7.0 o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> </dl>

 

 





