---
title: Network.bufferingTime
description: La proprietà bufferingTime specifica o recupera la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima dell'inizio della riproduzione.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network.bufferingTime Windows Media Player
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
ms.openlocfilehash: afe4a68a7ad1ae8a1444f1e2f31ad09461e05d221e8fceae52960bd5927aac0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901731"
---
# <a name="networkbufferingtime"></a>Network.bufferingTime

La **proprietà bufferingTime** specifica o recupera la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima dell'inizio della riproduzione.

## <a name="syntax"></a>Sintassi

*lettore*. *rete*. **bufferingTime**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero **di** lettura/scrittura (**long**) compreso tra zero e 60.000 con un valore predefinito di 5.000.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la rete*. **bufferingTime per** specificare il numero di secondi allocati per il buffering dei dati in ingresso. Le informazioni vengono recuperate da un elemento HTML TEXT INPUT creato con ID = "bufText". **L'oggetto Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Di rete**](network-object.md)
</dt> </dl>

 

 





