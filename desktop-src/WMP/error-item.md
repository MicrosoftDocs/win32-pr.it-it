---
title: Error. Item (metodo)
description: Il metodo Item recupera un oggetto ErrorItem dalla coda degli errori.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe Error
- Classe Error Media Player Windows, metodo Item
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324575"
---
# <a name="erroritem-method"></a>Error. Item (metodo)

Il metodo **Item** recupera un oggetto **ErrorItem** dalla coda degli errori.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dell'oggetto **ErrorItem** da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **ErrorItem** .

## <a name="remarks"></a>Commenti

Windows Media Player può generare un certo numero di errori in risposta a una condizione di errore. Questo metodo consente il recupero di un errore specifico nella coda usando un numero di indice. I numeri di indice per la coda degli errori iniziano con zero.

È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio JScript riportato di seguito viene utilizzato l' *errore*. oggetto **Item** in un gestore eventi per avvertire l'utente dell'errore più recente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

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
</dt> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





