---
description: Annulla la registrazione del provider associato.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: Metodo ITipAutocompleteClient::UnadviseProvider (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: d4f573e1dab88e8556dc8c6011173cd3a2284a87d9f98ac6d05cea13cef65ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712101"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>Metodo ITipAutocompleteClient::UnadviseProvider

Annulla la registrazione del provider associato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWndField* \[ Pollici\]
</dt> <dd>

Handle di finestra del campo che fornisce la funzionalità di completamento automatico.

</dd> <dt>

*pIACProvider* \[ Pollici\]
</dt> <dd>

Puntatore a interfaccia all'interfaccia del provider di completamento automatico di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

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

 

 




