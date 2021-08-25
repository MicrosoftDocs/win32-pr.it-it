---
title: ErrorItem.errorDescription
description: La proprietà errorDescription recupera una descrizione dell'errore.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem.errorDescription Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5740adcef0b6eb86290ea392d0659abb0ccc3d51b0b0b1b3203105de67fb692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862791"
---
# <a name="erroritemerrordescription"></a>ErrorItem.errorDescription

La **proprietà errorDescription** recupera una descrizione dell'errore.

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="remarks"></a>Commenti

È necessario *impostare* Impostazioni . **enableErrorDialogs** su false se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene *utilizzato ErrorItem*. **errorDescription** in un gestore eventi per visualizzare il messaggio di errore all'utente. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





