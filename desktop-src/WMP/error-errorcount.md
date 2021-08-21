---
title: Error.errorCount
description: La proprietà errorCount recupera il numero di errori nella coda degli errori.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Error.errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99275930155724f47b77de4f85905b92de9d7a7eb612ab713d725a16c1239d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339803"
---
# <a name="errorerrorcount"></a>Error.errorCount

La **proprietà errorCount** recupera il numero di errori nella coda degli errori.

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**).

## <a name="remarks"></a>Commenti

È necessario *impostare* Impostazioni . **enableErrorDialogs** su false se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *Error*. **errorCount** in un gestore eventi per avvisare l'utente dell'errore più recente nella coda degli errori. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> </dl>

 

 





