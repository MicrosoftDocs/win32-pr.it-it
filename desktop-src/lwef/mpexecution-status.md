---
title: Enumerazione MPEXECUTION_STATUS (MpClient. h)
description: Stato di esecuzione della minaccia possibile.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPEXECUTION_STATUS
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPEXECUTION_STATUS
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
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873597"
---
# <a name="mpexecution_status-enumeration"></a>\_Enumerazione stato MPEXECUTION

Stato di esecuzione della minaccia possibile.

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

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**\_stato di esecuzione MP \_ \_ sconosciuto**
</dt> <dd>

Lo stato di esecuzione non è noto.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**\_stato di esecuzione MP \_ \_ bloccato**
</dt> <dd>

Bloccato dall'esecuzione con mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**\_stato esecuzione \_ MP \_ consentito**
</dt> <dd>

Consentito per l'esecuzione con mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_stato esecuzione MP in \_ \_ esecuzione**
</dt> <dd>

È in corso l'esecuzione della minaccia.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**\_stato esecuzione \_ MP \_ non in \_ esecuzione**
</dt> <dd>

La minaccia non è in esecuzione ed è disponibile solo dal motore durante la correzione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





