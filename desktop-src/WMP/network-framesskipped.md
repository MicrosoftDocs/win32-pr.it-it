---
title: Network.framesSkipped
description: La proprietà framesSkipped recupera il numero totale di fotogrammi ignorati durante la riproduzione.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Network.framesSkipped Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1031585feae5fa2c7fdd9f5fb64bf958e77b8029d502f3e99476024276a652cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901671"
---
# <a name="networkframesskipped"></a>Network.framesSkipped

La **proprietà framesSkipped** recupera il numero totale di fotogrammi ignorati durante la riproduzione.

## <a name="syntax"></a>Sintassi

*lettore*. *network*. **framesSkipped**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **framesSkipped** per visualizzare il numero totale di fotogrammi ignorati durante la riproduzione quando l'utente fa clic su un pulsante. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FS". **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





