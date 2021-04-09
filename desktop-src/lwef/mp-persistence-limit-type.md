---
title: Enumerazione MP_PERSISTENCE_LIMIT_TYPE (MpClient. h)
description: Tipo di limite di persistenza.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_PERSISTENCE_LIMIT_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_PERSISTENCE_LIMIT_TYPE
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048676"
---
# <a name="mp_persistence_limit_type-enumeration"></a>\_Enumerazione del \_ tipo di limite di PERSISTEnza MP \_

Tipo di limite di persistenza.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**\_persistenza MP \_ sconosciuta**
</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**\_ \_ Nessun limite di PERSISTEnza MP \_**
</dt> <dd>

Nessun limite.

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**\_durata di persistenza MP \_**
</dt> <dd>

Durata.

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_versione di \_ VDM PERSISTEnza MP \_**
</dt> <dd>

Versione di VDM.

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**\_timestamp di persistenza MP \_**
</dt> <dd>

Timestamp.

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**\_persistenza MP \_ forzata**
</dt> <dd>

Forzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





