---
description: Determina se il Pannello input penna è pronto per visualizzare l'elenco di completamento automatico.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: Metodo ITipAutocompleteClient::RequestShowUI (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 4288a506e14ae8096db9be051e3282bb2ebd62522988d75574f3e56070419fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449794"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>Metodo ITipAutocompleteClient::RequestShowUI

Determina se il Pannello input penna è pronto per visualizzare l'elenco di completamento automatico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWndACList* \[ Pollici\]
</dt> <dd>

Handle di finestra dell'interfaccia utente dell'elenco di completamento automatico.

</dd> <dt>

*pfAllowShowing* \[ Cambio\]
</dt> <dd>

**FALSE** se il client consiglia di non visualizzare l'interfaccia utente dell'elenco di completamento automatico. **TRUE** se il provider di completamento automatico può visualizzare l'interfaccia utente dell'elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal provider di completamento automatico quando sta per visualizzare l'interfaccia utente di completamento automatico. Se lo stato interno del client non consente al provider di visualizzare l'interfaccia utente, *pfAllowShowing* verrà impostato su **FALSE.** Ad esempio, quando il testo viene inviato al campo dall'interfaccia di scrittura manuale nel Pannello input penna del Tablet PC e l'utente avvia immediatamente l'input penna, il client consiglia di non visualizzare l'interfaccia utente di completamento automatico, per evitare di distrumentare l'input penna dell'utente, impostando *pfAllowShowing* su **FALSE.**

Chiamare **RequestShowUI** per impostare l'handle della finestra dell'elenco di completamento automatico popup prima di chiamare il metodo [**ITipAutocompleteClient::P referredRects**](itipautocompleteclient-preferredrects.md). In caso negativo, si verifica un **errore E \_ INVALIDARG** quando si **chiama PreferredRects**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete.h (richiede anche Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[**Metodo ITipAutocompleteClient::P referredRects**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Informazioni di riferimento sul pannello di input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




