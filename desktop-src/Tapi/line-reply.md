---
description: Il messaggio di risposta della linea TAPI \_ viene inviato per segnalare i risultati delle chiamate di funzione completate in modo asincrono.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Messaggio di LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332918"
---
# <a name="line_reply-message"></a>Messaggio di risposta di riga \_

Il messaggio **di \_ risposta della linea** TAPI viene inviato per segnalare i risultati delle chiamate di funzione completate in modo asincrono.


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

Restituisce l'istanza di callback dell'applicazione.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificatore della richiesta per cui si tratta della risposta.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Indicazione di esito positivo o negativo. L'applicazione deve eseguire il cast di questo parametro in un valore LONG. Zero indica esito positivo; un numero negativo indica un errore.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le funzioni che operano in modo asincrono restituiscono un valore di identificatore di richiesta positivo all'applicazione. Questo identificatore di richiesta viene restituito con il messaggio di risposta per identificare la richiesta completata. L'altro parametro per il messaggio di **\_ risposta di riga** contiene l'indicazione di esito positivo o negativo. Gli errori possibili sono gli stessi di quelli definiti dalla funzione corrispondente. Questo messaggio non può essere disabilitato.

In alcuni casi, un'applicazione potrebbe non essere in grado di ricevere il messaggio di **\_ risposta di riga** corrispondente a una chiamata a una funzione asincrona. Questo errore si verifica se l'handle di chiamata corrispondente viene deallocato prima che il messaggio sia stato ricevuto.

> [!Note]  
> Quando un'applicazione richiama qualsiasi operazione asincrona che scrive i dati nella memoria dell'applicazione, l'applicazione deve mantenuta la memoria disponibile per la scrittura fino a quando non viene ricevuta una **\_ risposta di riga** o un messaggio [**\_ GATHERDIGITS**](line-gatherdigits.md) .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> </dl>

 

 




