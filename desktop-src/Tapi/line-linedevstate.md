---
description: Il messaggio TAPI LINE \_ LINEDEVSTATE viene inviato quando lo stato di un dispositivo linea è stato modificato. L'applicazione può richiamare lineGetLineDevStatus per determinare il nuovo stato della riga.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: LINE_LINEDEVSTATE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261e7527354b84801437e48ffc13ba4dbad60ced0cca61be65eb96ce6417bb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682389"
---
# <a name="line_linedevstate-message"></a>Line \_ LINEDEVSTATE message

Il messaggio TAPI **LINE \_ LINEDEVSTATE** viene inviato quando lo stato di un dispositivo line è stato modificato. L'applicazione può richiamare [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) per determinare il nuovo stato della riga.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per il dispositivo di linea. Questo parametro è **NULL quando** *dwParam1* è LINEDEVSTATE \_ REINIT.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga. Se il *parametro dwParam1* è LINEDEVSTATE \_ REINIT, *il parametro dwCallbackInstance* non è valido e viene impostato su zero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Elemento di stato del dispositivo linea che è stato modificato. Il parametro può essere una o più costanti [**LINEDEVSTATE. \_**](linedevstate--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

L'interpretazione di questo parametro dipende dal valore *di dwParam1*. Se *dwParam1* è LINEDEVSTATE \_ RINGING, *dwParam2* contiene la modalità anello con cui l'opzione indica alla riga di eseguire il ring. Le modalità anello valide sono numeri nell'intervallo da uno a **dwNumRingModes,** dove **dwNumRingModes** è una funzionalità del dispositivo linea.

Se *dwParam1* è LINEDEVSTATE REINIT e il messaggio è stato emesso da TAPI come risultato della conversione di un nuovo messaggio API in un messaggio \_ REINIT, *dwParam2* contiene il *parametro dwMsg* del messaggio originale,ad esempio [**LINE \_ CREATE**](line-create.md) o \_ LINE LINEDEVSTATE. Se *dwParam2* è zero, significa che il messaggio REINIT è un messaggio REINIT "reale" che richiede all'applicazione di chiamare [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) al più presto.

</dd> <dt>

*dwParam3* 
</dt> <dd>

L'interpretazione di questo parametro dipende dal valore *di dwParam1*. Se *dwParam1 è* LINEDEVSTATE \_ RINGING, *dwParam3* contiene il numero di anelli per questo evento circolare. Il conteggio degli anelli inizia da zero.

Se *dwParam1* è LINEDEVSTATE REINIT e il messaggio è stato inviato da TAPI come risultato della conversione di un nuovo messaggio API in un messaggio \_ REINIT, *dwParam3* contiene il *parametro dwParam1* del messaggio originale (ad esempio, LINEDEVSTATE TRANSLATECHANGE o un altro valore \_ LINEDEVSTATE, se \_ *dwParam2* è LINE \_ LINEDEVSTATE o [**\_**](line-create.md)il nuovo identificatore di dispositivo, se *dwParam2* è LINE CREATE ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'invio **del \_ messaggio LINE LINEDEVSTATE** può essere controllato [**con lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Un'applicazione può indicare le modifiche all'elemento di stato per cui vuole ricevere una notifica. Per impostazione predefinita, tutti i report sullo stato sono disabilitati ad eccezione di LINEDEVSTATE \_ REINIT, che non può essere disabilitato. Questo messaggio viene inviato a tutte le applicazioni che hanno un handle alla riga, incluse quelle che hanno chiamato [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con il parametro *dwPrivileges* impostato su LINECALLPRIVILEGE \_ NONE, LINECALLPRIVILEGE \_ OWNER, LINECALLPRIVILEGE MONITOR o combinazioni \_ consentite.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ CREATE**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




