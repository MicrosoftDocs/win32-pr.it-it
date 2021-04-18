---
description: Il messaggio della linea TAPI \_ CALLINFO viene inviato quando vengono modificate le informazioni relative alla chiamata specificata. L'applicazione può richiamare lineGetCallInfo per determinare le informazioni sulla chiamata corrente.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Messaggio di LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328052"
---
# <a name="line_callinfo-message"></a>\_Messaggio linea CALLINFO

Il messaggio della **linea TAPI \_ CALLINFO** viene inviato quando vengono modificate le informazioni relative alla chiamata specificata. L'applicazione può richiamare [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) per determinare le informazioni sulla chiamata corrente.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Elemento delle informazioni sulla chiamata modificato. Può essere una o più delle [**\_ costanti LINECALLINFOSTATE**](linecallinfostate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Un messaggio di **riga \_ CALLINFO** con indicazione *NumOwnersIncr*, *NumOwnersDecr* e/o *NumMonitorsChanged* viene inviato ad applicazioni che dispongono già di un handle per la chiamata. Questo può essere il risultato di un'altra applicazione che modifica la proprietà o il monitoraggio a una chiamata con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)e [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).

Questi messaggi di **riga \_ CALLINFO** non vengono inviati quando viene fornita una notifica di una nuova chiamata in un messaggio di [**\_ CALLSTATE riga**](line-callstate.md) , perché le informazioni sulla chiamata riflettono già il numero corretto di proprietari e monitoraggi al momento dell'invio dei messaggi di riga \_ CALLSTATE. **Riga \_ di** I messaggi CALLINFO vengono eliminati anche nel caso in cui una chiamata viene offerta da TAPI per monitorare il \_ meccanismo sconosciuto di LINECALLSTATE.

> [!Note]  
> L'applicazione che causa una modifica al numero di proprietari o monitoraggi (ad esempio, richiamando [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) o [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) non riceve un messaggio che indica che la modifica è stata eseguita.

 

Non viene inviato alcun messaggio di **riga \_ CALLINFO** per una chiamata dopo che la chiamata è entrata nello stato di *inattività* . In particolare, le modifiche apportate al numero di proprietari e monitoraggi non vengono segnalate come le applicazioni deallocano gli handle per la chiamata inattiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




