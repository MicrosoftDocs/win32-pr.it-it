---
description: Il messaggio TAPI LINE \_ PROXYREQUEST recapita una richiesta a un gestore di funzioni proxy registrato.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31986420cd21178cca8e6f0a1006e743c3250e726b4a1bf79513f6d57e380a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003159"
---
# <a name="line_proxyrequest-message"></a>MESSAGGIO \_ LINE PROXYREQUEST

Il messaggio TAPI **LINE \_ PROXYREQUEST** recapita una richiesta a un gestore di funzioni proxy registrato.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo line in cui è stato modificato lo stato dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Puntatore a [**una struttura LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) contenente la richiesta che deve essere elaborata dall'applicazione del gestore proxy.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Riservato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio LINE \_ PROXYREQUEST** viene inviato solo alla prima applicazione registrata per gestire le richieste proxy del tipo recapitato.

L'applicazione deve elaborare la richiesta contenuta nel buffer del proxy e chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per restituire i dati o recapitare i risultati. L'elaborazione della richiesta deve essere eseguita nel contesto della funzione di callback TAPI dell'applicazione solo se può essere eseguita immediatamente, senza attendere la risposta da qualsiasi altra entità. Se l'applicazione deve comunicare con altre entità (ad esempio, un provider di servizi per gestire acD basato su UNANIS o qualsiasi altro servizio di sistema che potrebbe causare il blocco), la richiesta deve essere accodata all'interno dell'applicazione e la funzione di callback è stata chiusa per evitare di ritardare la ricezione di altri messaggi TAPI da parte dell'applicazione.

Quando LINE **\_ PROXYREQUEST** viene recapitato al gestore proxy, TAPI ha già restituito un risultato positivo della funzione *dwRequestID* all'applicazione originale e ha sbloccato il thread chiamante per continuare l'esecuzione. L'applicazione è in attesa di un [**messaggio LINE \_ REPLY,**](line-reply.md) che viene generato automaticamente quando l'applicazione del gestore proxy chiama [**lineProxyResponse.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)

L'applicazione non deve liberare la memoria a cui punta *lpProxyRequest*. TAPI libera la memoria durante l'esecuzione di [**lineProxyResponse.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) L'applicazione può chiamare [**lineProxyResponse esattamente**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) una volta per ogni **messaggio LINE \_ PROXYREQUEST.**

Se l'applicazione riceve un messaggio [**LINE \_ CLOSE**](line-close.md) mentre contiene richieste proxy in sospeso, deve chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per ogni richiesta in sospeso, passando un valore *dwResult* appropriato (ad esempio LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHIUSURA \_ RIGA**](line-close.md)
</dt> <dt>

[**LINE \_ REPLY**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




