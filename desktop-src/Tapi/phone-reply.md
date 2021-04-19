---
description: Il messaggio di risposta del telefono TAPI \_ viene inviato a un'applicazione per segnalare i risultati della chiamata di funzione completata in modo asincrono.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Messaggio di PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324126"
---
# <a name="phone_reply-message"></a>\_Messaggio di risposta telefono

Il messaggio **di \_ risposta del telefono** TAPI viene inviato a un'applicazione per segnalare i risultati della chiamata di funzione completata in modo asincrono.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPhone* 
</dt> <dd>

Non utilizzato.

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

Le funzioni che operano in modo asincrono restituiscono un valore di identificatore di richiesta positivo all'applicazione. Questo identificatore di richiesta viene restituito con il messaggio di risposta per identificare la richiesta completata. L'altro parametro per il messaggio di **\_ risposta telefonica** contiene l'indicazione di esito positivo o negativo. Gli errori possibili sono gli stessi di quelli definiti dalla funzione corrispondente. Questo messaggio non può essere disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




