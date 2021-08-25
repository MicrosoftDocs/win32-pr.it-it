---
title: MPEXECUTION_STATUS enumerazione (MpClient.h)
description: Possibile stato di esecuzione delle minacce.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS di enumerazione Legacy Windows Environment Features
- PMPEXECUTION_STATUS puntatore di enumerazione Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4748b6d97e1b7ee05db8044837b89e2653a14fd1e6f87068a40107cdd9ee60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943911"
---
# <a name="mpexecution_status-enumeration"></a>Enumerazione MPEXECUTION \_ STATUS

Possibile stato di esecuzione delle minacce.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**STATO \_ DI ESECUZIONE MP \_ \_ SCONOSCIUTO**
</dt> <dd>

Lo stato di esecuzione non è noto.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**STATO \_ DI ESECUZIONE MP \_ \_ BLOCCATO**
</dt> <dd>

Bloccato dall'esecuzione tramite mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**STATO \_ DI ESECUZIONE MP \_ \_ CONSENTITO**
</dt> <dd>

Consentito per l'esecuzione tramite mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**STATO \_ DI ESECUZIONE MP IN \_ \_ ESECUZIONE**
</dt> <dd>

Minaccia in esecuzione.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**STATO \_ DI ESECUZIONE MP NON IN \_ \_ \_ ESECUZIONE**
</dt> <dd>

La minaccia non è in esecuzione ed è disponibile solo dal motore durante la correzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





