---
title: BITS_JOB_TRANSFER_POLICY enumerazione (Deliveryoptimization.h)
description: L BITS_JOB_TRANSFER_POLICY enumere definisce i valori ID corrispondenti alle proprietà DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- BITS_JOB_TRANSFER_POLICY enumerazione
- BITS_JOB_TRANSFER_POLICY enumerazione
topic_type:
- apiref
api_name:
- BITS_JOB_TRANSFER_POLICY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 022d12b78416ce4ec84cf02ae8696f17bf5c315a207ae04f28a8980f6aaac073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544599"
---
# <a name="bits_job_transfer_policy-enumeration"></a>BITS_JOB_TRANSFER_POLICY enumerazione

L BITS_JOB_TRANSFER_POLICY enumere definisce i valori ID corrispondenti alle proprietà DO. 

## <a name="syntax"></a>Sintassi


```C++
typedef enum _BITS_JOB_TRANSFER_POLICY { 
  BITS_JOB_TRANSFER_POLICY_ALWAYS        = 0x800000ff,
  BITS_JOB_TRANSFER_POLICY_NOT_ROAMING   = 0x8000007f,
  BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE  = 0x8000006f,
  BITS_JOB_TRANSFER_POLICY_STANDARD      = 0x80000067,
  BITS_JOB_TRANSFER_POLICY_UNRESTRICTED  = 0x80000021
} BITS_JOB_TRANSFER_POLICY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_ALWAYS"></span><span id="bits_job_transfer_policy_always"></span>**BITS_JOB_TRANSFER_POLICY_ALWAYS**
</dt> <dd>

Specifica che il processo verrà trasferito quando la connettività è disponibile, indipendentemente dal costo.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NOT_ROAMING"></span><span id="bits_job_transfer_policy_not_roaming"></span>**BITS_JOB_TRANSFER_POLICY_NOT_ROAMING**
</dt> <dd>

Specifica che il processo verrà trasferito quando la connettività è disponibile, a meno che tale connettività non sia soggetta a supplementi mobili.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**
</dt> <dd>

Specifica che il processo verrà trasferito solo quando è disponibile la connettività che non è soggetta a un supplemento.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**
</dt> <dd>

Specifica che il processo verrà trasferito solo quando è disponibile la connettività, che non è soggetta a un supplemento né quasi esaurita.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**
</dt> <dd>

Specifica che il processo verrà trasferito solo quando è disponibile la connettività che non impone costi o limiti di traffico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



 

 





