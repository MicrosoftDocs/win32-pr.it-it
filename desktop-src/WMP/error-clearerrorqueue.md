---
title: Error. clearErrorQueue, metodo
description: Il metodo clearErrorQueue Cancella gli errori dalla coda degli errori. | Error. clearErrorQueue, metodo
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- Metodo clearErrorQueue Windows Media Player
- Metodo clearErrorQueue Windows Media Player, classe Error
- Classe Error Media Player Windows, metodo clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327293"
---
# <a name="errorclearerrorqueue-method"></a>Error. clearErrorQueue, metodo

Il metodo **clearErrorQueue** Cancella gli errori dalla coda degli errori.

## <a name="syntax"></a>Sintassi


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è utile per cancellare la coda degli errori dopo l'elaborazione di una serie di errori.

È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Error*. **clearErrorQueue** in un gestore eventi per svuotare la coda degli errori dopo la visualizzazione di tutte le descrizioni degli errori. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> </dl>

 

 





