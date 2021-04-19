---
title: Evento Player. Error
description: L'evento di errore si verifica in presenza di una condizione di errore.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Media Player di eventi di errore di Windows
- Evento di errore Windows Media Player, classe Player
- Classe Player Windows Media Player, evento Error
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
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329301"
---
# <a name="playererror-event"></a>Evento Player. Error

L'evento di **errore** si verifica in presenza di una condizione di errore.

## <a name="syntax"></a>Sintassi


```JScript
Player.Error()
```



## <a name="parameters"></a>Parametri

Questo evento non contiene parametri.

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene creato un gestore eventi per visualizzare il testo della descrizione per il primo errore nella coda degli errori. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ErrorItem. errorDescription**](erroritem-errordescription.md)
</dt> <dt>

[**Errore. elemento**](error-item.md)
</dt> <dt>

[**Oggetto Player**](player-object.md)
</dt> </dl>

 

 





