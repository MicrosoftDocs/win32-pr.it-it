---
title: Evento Player.Error
description: L'evento Error si verifica quando è presente una condizione di errore.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Eventi di errore Windows Media Player
- Evento di errore Windows Media Player , classe Player
- Classe player Windows Media Player , evento Error
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a7e4642eef19b4edc4b1aa5bc75022a307d279d0d60482af0c7e2f0a9368c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134814"
---
# <a name="playererror-event"></a>Evento Player.Error

**L'evento Error** si verifica quando è presente una condizione di errore.

## <a name="syntax"></a>Sintassi


```JScript
Player.Error()
```



## <a name="parameters"></a>Parametri

Questo evento non ha parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene creato un gestore eventi per visualizzare il testo della descrizione del primo errore nella coda degli errori. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

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

[**ErrorItem.errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Error.item**](error-item.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





