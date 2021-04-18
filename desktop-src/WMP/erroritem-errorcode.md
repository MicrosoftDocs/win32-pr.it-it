---
title: ErrorItem. errorCode
description: La proprietà errorCode Recupera il codice di errore corrente.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- Media Player Windows ErrorItem. errorCode
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324744"
---
# <a name="erroritemerrorcode"></a>ErrorItem. errorCode

La proprietà **ErrorCode** Recupera il codice di errore corrente.

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**).

## <a name="remarks"></a>Commenti

È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *ErrorItem*. **ErrorCode** in un gestore eventi per visualizzare il codice di errore all'utente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> </dl>

 

 





