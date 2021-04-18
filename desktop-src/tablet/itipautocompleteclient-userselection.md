---
description: Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e per rimuovere tutto il testo rimanente che non è ancora stato inserito.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'Metodo ITipAutocompleteClient:: UserSelection (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313451"
---
# <a name="itipautocompleteclientuserselection-method"></a>Metodo ITipAutocompleteClient:: UserSelection

Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e per rimuovere tutto il testo rimanente che non è ancora stato inserito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal provider per notificare al client che è stata effettuata una selezione da parte dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




