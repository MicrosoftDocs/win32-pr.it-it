---
title: Enumerazione BITS_JOB_TRANSFER_POLICY (Deliveryoptimization. h)
description: L'enumerazione BITS_JOB_TRANSFER_POLICY definisce i valori ID corrispondenti alle proprietà DO.
ms.assetid: 4811ADBF-F097-4340-BFF2-52CC9556ACF6
keywords:
- Enumerazione BITS_JOB_TRANSFER_POLICY
- Enumerazione BITS_JOB_TRANSFER_POLICY
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
ms.openlocfilehash: 455752375b76e574923ccdd96d1d05fc9142c16c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119350"
---
# <a name="bits_job_transfer_policy-enumeration"></a>Enumerazione BITS_JOB_TRANSFER_POLICY

L'enumerazione **BITS_JOB_TRANSFER_POLICY** definisce i valori ID corrispondenti alle proprietà do.

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

Specifica che il processo verrà trasferito quando è disponibile la connettività, a meno che la connettività non sia soggetta a sovrapprezzi in roaming.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE"></span><span id="bits_job_transfer_policy_no_surcharge"></span>**BITS_JOB_TRANSFER_POLICY_NO_SURCHARGE**
</dt> <dd>

Specifica che il processo verrà trasferito solo quando è disponibile la connettività, che non è soggetta a un supplemento.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_STANDARD"></span><span id="bits_job_transfer_policy_standard"></span>**BITS_JOB_TRANSFER_POLICY_STANDARD**
</dt> <dd>

Specifica che il processo verrà trasferito solo quando è disponibile la connettività, che non è soggetta a un sovrapprezzo né a un esaurimento.

</dd> <dt>

<span id="BITS_JOB_TRANSFER_POLICY_UNRESTRICTED"></span><span id="bits_job_transfer_policy_unrestricted"></span>**BITS_JOB_TRANSFER_POLICY_UNRESTRICTED**
</dt> <dd>

Specifica che il processo verrà trasferito solo quando è disponibile la connettività che non impone costi o limiti di traffico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





