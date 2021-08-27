---
description: Il messaggio TAPI LINE \_ REPLY viene inviato per segnalare i risultati delle chiamate di funzione completate in modo asincrono.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: LINE_REPLY messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febe10c822a469465984b715c7b6f23d150f1f068730d4e92190b05ce50cd535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126241"
---
# <a name="line_reply-message"></a>LINE \_ REPLY message

Il messaggio TAPI **LINE \_ REPLY** viene inviato per segnalare i risultati delle chiamate di funzione completate in modo asincrono.


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

Indicazione di esito positivo o di errore. L'applicazione deve eseguire il cast di questo parametro in long. Zero indica l'esito positivo. un numero negativo indica un errore.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Le funzioni che operano in modo asincrono restituiscono all'applicazione un valore di identificatore di richiesta positivo. Questo identificatore di richiesta viene restituito con il messaggio di risposta per identificare la richiesta completata. L'altro parametro per il **messaggio LINE \_ REPLY** contiene l'indicazione di esito positivo o negativo. Gli errori possibili sono gli stessi definiti dalla funzione corrispondente. Questo messaggio non può essere disabilitato.

In alcuni casi, un'applicazione potrebbe non riuscire a ricevere il messaggio **LINE \_ REPLY** corrispondente a una chiamata a una funzione asincrona. Questo errore si verifica se l'handle di chiamata corrispondente viene deallocato prima della ricezione del messaggio.

> [!Note]  
> Quando un'applicazione richiama un'operazione asincrona che scrive nuovamente i dati nella memoria dell'applicazione, l'applicazione deve mantenere tale memoria disponibile per la scrittura fino a quando non viene ricevuto un messaggio **LINE \_ REPLY** o [**LINE \_ GATHERDIGITS.**](line-gatherdigits.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> </dl>

 

 




