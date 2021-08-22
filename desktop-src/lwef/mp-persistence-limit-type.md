---
title: MP_PERSISTENCE_LIMIT_TYPE enumerazione (MpClient.h)
description: Tipo di limite di persistenza.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE funzionalità dell'ambiente Windows legacy
- PMP_PERSISTENCE_LIMIT_TYPE puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: c2a56d4962467abe0ad338af257aca2581e612c100468fbdf2853aa4d71290ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609001"
---
# <a name="mp_persistence_limit_type-enumeration"></a>Enumerazione \_ MP PERSISTENCE LIMIT \_ \_ TYPE

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

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP \_ PERSISTENCE \_ UNKNOWN**
</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP \_ PERSISTENCE \_ NO \_ LIMIT**
</dt> <dd>

Nessun limite.

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**DURATA \_ PERSISTENZA \_ MP**
</dt> <dd>

Durata.

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP \_ PERSISTENCE \_ VDM \_ VERSION**
</dt> <dd>

Versione VDM.

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**\_TIMESTAMP DI PERSISTENZA \_ MP**
</dt> <dd>

Timestamp.

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP \_ PERSISTENCE \_ FORCED**
</dt> <dd>

Costretto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





