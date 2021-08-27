---
description: Il messaggio TAPI LINE \_ REQUEST viene inviato per segnalare l'arrivo di una nuova richiesta da un'altra applicazione.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: LINE_REQUEST messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cd49b14aafabfdd4d7ab37c5f2beec1487a08a53385ae8a1439b7443d49cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126231"
---
# <a name="line_request-message"></a>MESSAGGIO LINE \_ REQUEST

Il messaggio TAPI **LINE \_ REQUEST viene** inviato per segnalare l'arrivo di una nuova richiesta da un'altra applicazione.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di registrazione dell'applicazione specificata [**nella rigaRegisterRequestRecipient.**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)

</dd> <dt>

*dwParam1* 
</dt> <dd>

Modalità di richiesta della richiesta appena in sospeso. Questo parametro usa le [**costanti LINEREQUESTMODE \_**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Le condizioni per questo parametro sono, se *dwParam1* è impostato su LINEREQUESTMODE \_ DROP, *dwParam2 contiene* il *valore hWnd* dell'applicazione che richiede l'eliminazione. In caso *contrario, dwParam2* non viene usato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam1* è impostato su LINEREQUESTMODE DROP, la parola di ordine più basso \_ di *dwParam3* contiene *wRequestID* come specificato dall'applicazione che ha richiesto l'eliminazione. In caso *contrario, dwParam3* non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio LINE \_ REQUEST** viene inviato all'applicazione con priorità più alta registrata per la modalità di richiesta corrispondente. Questo messaggio indica l'arrivo di una richiesta di telefonia assistita della modalità di richiesta specificata. Se *dwParam1* è LINEREQUESTMODE MAKECALL, l'applicazione può richiamare lineGetRequest usando la modalità di richiesta \_ corrispondente per ricevere la richiesta. [](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) Se *dwParam1* è LINEREQUESTMODE DROP, il messaggio contiene tutti i dati necessari al destinatario della richiesta \_ per eseguire la richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




