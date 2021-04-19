---
description: Il messaggio di richiesta della linea TAPI \_ viene inviato per segnalare l'arrivo di una nuova richiesta da un'altra applicazione.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Messaggio di LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326625"
---
# <a name="line_request-message"></a>Messaggio di richiesta di riga \_

Il messaggio **di \_ richiesta della linea** TAPI viene inviato per segnalare l'arrivo di una nuova richiesta da un'altra applicazione.


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

Istanza di registrazione dell'applicazione specificata in [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).

</dd> <dt>

*dwParam1* 
</dt> <dd>

Modalità di richiesta della richiesta appena in sospeso. Questo parametro usa le [**\_ costanti LINEREQUESTMODE**](linerequestmode--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Le condizioni per questo parametro sono, se *dwParam1* è impostato su LINEREQUESTMODE \_ Drop, *dwParam2* contiene l' *HWND* dell'applicazione che richiede l'eliminazione. In caso contrario, *dwParam2* è inutilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam1* è impostato su LINEREQUESTMODE \_ Drop, la parola di ordine inferiore di *dwParam3* contiene il *wRequestID* come specificato dall'applicazione che ha richiesto l'eliminazione. In caso contrario, *dwParam3* è inutilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **\_ richiesta di riga** viene inviato all'applicazione con priorità più elevata registrata per la modalità di richiesta corrispondente. Questo messaggio indica l'arrivo di una richiesta di telefonia assistita della modalità di richiesta specificata. Se *dwParam1* è LINEREQUESTMODE \_ MAKECALL, l'applicazione può richiamare [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) usando la modalità di richiesta corrispondente per ricevere la richiesta. Se *dwParam1* è LINEREQUESTMODE \_ Drop, il messaggio contiene tutti i dati necessari al destinatario della richiesta per eseguire la richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[**tapiRequestMakeCall**](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




