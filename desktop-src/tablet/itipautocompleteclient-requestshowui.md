---
description: Determina se il pannello di input è pronto per visualizzare l'elenco di completamento automatico.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Metodo ITipAutocompleteClient:: RequestShowUI (TipAutoComplete. h)'
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
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231911"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>Metodo ITipAutocompleteClient:: RequestShowUI

Determina se il pannello di input è pronto per visualizzare l'elenco di completamento automatico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWndACList* \[ in\]
</dt> <dd>

Handle di finestra dell'interfaccia utente dell'elenco di completamento automatico.

</dd> <dt>

*pfAllowShowing* \[ out\]
</dt> <dd>

**False** se il client consiglia di non visualizzare l'interfaccia utente dell'elenco di completamento automatico. **True** se il provider di completamento automatico può visualizzare l'interfaccia utente dell'elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal provider di completamento automatico quando sta per visualizzare l'interfaccia utente di completamento automatico. Se lo stato interno del client non consente al provider di visualizzare l'interfaccia utente, *pfAllowShowing* verrà impostato su **false**. Ad esempio, quando il testo viene inviato al campo dall'interfaccia della grafia nel Pannello input penna di Tablet PC e l'utente avvia immediatamente Inking, il client consiglia di non visualizzare l'interfaccia utente di completamento automatico, in modo da evitare la distruzione dell'Inking dell'utente, impostando *pfAllowShowing* su **false**.

Chiamare **RequestShowUI** per impostare l'handle della finestra elenco di completamento automatico popup prima di chiamare il [**metodo ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md). In caso contrario, viene generato un errore **E \_ INVALIDARG** quando si chiama **PreferredRects**.

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

[**ITipAutocompleteClient::P metodo referredRects**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




