---
title: Rete. bufferingTime
description: La proprietà bufferingTime specifica o recupera la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima che inizi la riproduzione.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Media Player di Windows Network. bufferingTime
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326111"
---
# <a name="networkbufferingtime"></a>Rete. bufferingTime

La proprietà **bufferingTime** specifica o recupera la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima che inizi la riproduzione.

## <a name="syntax"></a>Sintassi

*Player*. *rete*. **bufferingTime**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Long**) compreso tra 0 e 60.000 e il valore predefinito è 5.000.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *rete*. **bufferingTime** per specificare il numero di secondi allocati per il buffering dei dati in ingresso. Le informazioni vengono recuperate da un elemento INPUT di testo HTML creato con ID = "bufText". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

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

 

 





