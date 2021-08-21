---
title: BG_JOB_PRIORITY enumerazione (Deliveryoptimization.h)
description: L BG_JOB_PRIORITY enumere dei criteri definisce i valori costanti che specificano il livello di priorità di un processo.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY enumerazione
- BG_JOB_PRIORITY enumerazione
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddeb3ea128f173d53c71467d4098c1b777beea48f7b1304922f7468d55fc3b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810951"
---
# <a name="bg_job_priority-enumeration"></a>BG_JOB_PRIORITY enumerazione

L BG_JOB_PRIORITY enumere dei criteri definisce i valori costanti che specificano il livello di priorità di un processo. 

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Trasferisce il processo in primo piano. I trasferimenti in primo piano si concorreranno per la larghezza di banda di rete con altre applicazioni, che possono compromettere l'esperienza di rete dell'utente. Si tratta del livello di priorità più alto.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Trasferisce il processo in background. I trasferimenti in background usano una piccola percentuale di larghezza di banda di rete.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

Il comportamento di DO è lo stesso per tutti i processi non in primo piano. Per informazioni dettagliate, BG_JOB_PRIORITY_HIGH commenti in .

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Il comportamento di DO è lo stesso per tutti i processi non in primo piano. Per informazioni dettagliate, BG_JOB_PRIORITY_HIGH commenti in .

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile eseguire contemporaneamente più trasferimenti in primo piano e in background.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob::GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**IBackgroundCopyJob::SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





