---
title: Rete. framesSkipped
description: La proprietà framesSkipped Recupera il numero totale di frame ignorati durante la riproduzione.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Media Player di Windows Network. framesSkipped
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
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329440"
---
# <a name="networkframesskipped"></a>Rete. framesSkipped

La proprietà **framesSkipped** Recupera il numero totale di frame ignorati durante la riproduzione.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **framesSkipped**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **framesSkipped** per visualizzare il numero totale di frame ignorati durante la riproduzione quando l'utente fa clic su un pulsante. Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FS". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto di rete**](network-object.md)
</dt> </dl>

 

 





