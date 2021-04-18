---
title: ErrorItem. errorDescription
description: La proprietà errorDescription recupera una descrizione dell'errore.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- Media Player Windows ErrorItem. errorDescription
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
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324740"
---
# <a name="erroritemerrordescription"></a>ErrorItem. errorDescription

La proprietà **errorDescription** recupera una descrizione dell'errore.

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *ErrorItem*. **errorDescription** in un gestore eventi per visualizzare il messaggio di errore all'utente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





