---
description: Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e rimuove tutto il testo rimanente che non è ancora stato inserito.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: Metodo ITipAutocompleteClient::UserSelection (TipAutoComplete.h)
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
ms.openlocfilehash: 2dac765c3f1c3e709bb7066a1645c2d77783ea555bccd81f9d5809da802d7043
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843481"
---
# <a name="itipautocompleteclientuserselection-method"></a>Metodo ITipAutocompleteClient::UserSelection

Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e rimuove tutto il testo rimanente che non è ancora stato inserito.

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
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal provider per notificare al client che è stata effettuata una selezione dall'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete.h (richiede anche Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[Informazioni di riferimento sul pannello Input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




