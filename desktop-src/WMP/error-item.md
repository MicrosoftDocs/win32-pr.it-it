---
title: Metodo Error.item
description: Il metodo item recupera un oggetto ErrorItem dalla coda degli errori.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- Metodo item Windows Media Player
- Metodo item Windows Media Player , classe Error
- Classe Error Windows Media Player , metodo item
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
ms.openlocfilehash: 5e9fbd9f402a659af27db42c34cb0c58e2097270b73eb0eeff382544979dc0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339696"
---
# <a name="erroritem-method"></a>Metodo Error.item

Il **metodo item** recupera un oggetto **ErrorItem** dalla coda degli errori.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice dell'oggetto **ErrorItem** da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto ErrorItem.**

## <a name="remarks"></a>Commenti

Windows Media Player possibile generare una serie di errori in risposta a una condizione di errore. Questo metodo consente il recupero di un errore specifico nella coda usando un numero di indice. I numeri di indice per la coda degli errori iniziano con zero.

È necessario *impostare* Impostazioni . **enableErrorDialogs** su false se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene utilizzato *l'errore*. **Oggetto item** in un gestore eventi per avvisare l'utente dell'errore più recente. **L'oggetto** Player è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





