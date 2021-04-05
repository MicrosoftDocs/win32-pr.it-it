---
title: Enumerazione BG_JOB_PRIORITY (Deliveryoptimization. h)
description: L'enumerazione BG_JOB_PRIORITY definisce i valori costanti che specificano il livello di priorità di un processo.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Enumerazione BG_JOB_PRIORITY
- Enumerazione BG_JOB_PRIORITY
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
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048229"
---
# <a name="bg_job_priority-enumeration"></a>Enumerazione BG_JOB_PRIORITY

L'enumerazione **BG_JOB_PRIORITY** definisce i valori costanti che specificano il livello di priorità di un processo.

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

Trasferisce il processo in primo piano. I trasferimenti in primo piano competono per la larghezza di banda di rete con altre applicazioni, che possono ostacolare l'esperienza di rete dell'utente. Questo è il livello di priorità più alto.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Trasferisce il processo in background. I trasferimenti in background utilizzano una piccola percentuale di larghezza di banda di rete.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

Il comportamento è lo stesso per tutti i processi non in primo piano. Per informazioni dettagliate, vedere i commenti in BG_JOB_PRIORITY_HIGH.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Il comportamento è lo stesso per tutti i processi non in primo piano. Per informazioni dettagliate, vedere i commenti in BG_JOB_PRIORITY_HIGH.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile eseguire contemporaneamente più trasferimenti in primo piano e in background.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob:: GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: sepriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





