---
description: Il messaggio della linea \_ PROXYREQUEST di TAPI invia una richiesta a un gestore della funzione proxy registrato.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Messaggio di LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327983"
---
# <a name="line_proxyrequest-message"></a>\_Messaggio linea PROXYREQUEST

Il messaggio della **linea \_ PROXYREQUEST** di TAPI invia una richiesta a un gestore della funzione proxy registrato.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo della linea in cui è stato modificato lo stato dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Puntatore a una struttura [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) contenente la richiesta che deve essere elaborata dall'applicazione del gestore proxy.

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

Il messaggio di **riga \_ PROXYREQUEST** viene inviato solo alla prima applicazione registrata per gestire le richieste proxy del tipo recapitato.

L'applicazione deve elaborare la richiesta contenuta nel buffer del proxy e chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per restituire i dati o recapitare i risultati. L'elaborazione della richiesta deve essere eseguita nel contesto della funzione di callback TAPI dell'applicazione solo se può essere eseguita immediatamente, senza attendere la risposta da nessun'altra entità. Se l'applicazione deve comunicare con altre entità, ad esempio un provider di servizi per gestire ACD basato su PBX o qualsiasi altro servizio di sistema che potrebbe causare il blocco, la richiesta deve essere accodata all'interno dell'applicazione e la funzione di callback è stata chiusa per evitare di ritardare la ricezione di altri messaggi TAPI dall'applicazione.

Nel momento in cui la **riga \_ PROXYREQUEST** viene recapitata al gestore del proxy, TAPI ha già restituito un risultato positivo della funzione *dwRequestID* nell'applicazione originale e ha sbloccato il thread chiamante per continuare l'esecuzione. L'applicazione è in attesa di un messaggio di [**\_ risposta di riga**](line-reply.md) , che viene generato automaticamente quando l'applicazione del gestore del proxy chiama [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).

L'applicazione non deve liberare la memoria a cui punta *lpProxyRequest*. TAPI libera la memoria durante l'esecuzione di [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse). L'applicazione può chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) esattamente una volta per ogni messaggio di **riga \_ PROXYREQUEST** .

Se l'applicazione riceve un messaggio di [**\_ chiusura riga**](line-close.md) mentre contiene richieste proxy in sospeso, deve chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per ogni richiesta in sospeso, passando un valore *dwResult* appropriato, ad esempio LINEERR \_ OPERATIONFAILED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_chiusura riga**](line-close.md)
</dt> <dt>

[**\_risposta riga**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




