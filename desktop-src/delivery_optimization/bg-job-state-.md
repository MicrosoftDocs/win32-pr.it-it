---
title: Enumerazione BG_JOB_STATE (Deliveryoptimization. h)
description: L'enumerazione BG_JOB_STATE definisce i valori costanti per i diversi Stati di un processo.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Enumerazione BG_JOB_STATE
- Enumerazione BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301091"
---
# <a name="bg_job_state-enumeration"></a>Enumerazione BG_JOB_STATE

L'enumerazione **BG_JOB_STATE** definisce i valori costanti per i diversi Stati di un processo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

Specifica che il processo è in coda e in attesa di esecuzione. Se un utente si disconnette durante il trasferimento del processo, il processo passa allo stato in coda.

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

Non supportata.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Specifica che il trasferimento dei dati per il processo è in corso.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Specifica che il processo è sospeso (in pausa). Per sospendere un processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) . Il processo resta sospeso fino a quando non viene chiamato il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md), [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md)o [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Specifica che si è verificato un errore irreversibile (il servizio non è in grado di trasferire il file). Se è possibile correggere l'errore, ad esempio un errore di accesso negato, chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) dopo che l'errore è stato risolto. Tuttavia, se non è possibile correggere l'errore, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) per annullare il processo oppure chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per accettare la parte di un processo di download che è stato trasferito correttamente.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Specifica che si è verificato un errore reversibile. I processi vengono ritentati nello stato di errore temporaneo in base alla configurazione di ripetizione dei tentativi interna. Lo stato del processo viene modificato in **BG_JOB_STATE_ERROR** se il processo non riesce a eseguire lo stato di avanzamento (vedere [**Metodo ibackgroundcopyjob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Specifica che il processo è stato elaborato correttamente. È necessario chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per confermare il completamento del processo e rendere i file disponibili per il client.

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Specifica che è stato chiamato il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per confermare che il processo è stato completato correttamente.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Specifica che è stato chiamato il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) per annullare il processo, ovvero rimuovere il processo dalla coda di trasferimento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





