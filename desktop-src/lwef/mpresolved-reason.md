---
title: Enumerazione MPRESOLVED_REASON (MpClient. h)
description: Possibili motivi per la risoluzione di un errore di correzione.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPRESOLVED_REASON
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPRESOLVED_REASON
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048529"
---
# <a name="mpresolved_reason-enumeration"></a>\_Enumerazione MPRESOLVED Reason

Possibili motivi per la risoluzione di un errore di correzione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED \_ motivo \_ sconosciuto**
</dt> <dd>

In uno stato di errore.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED \_ motivo \_ dell' \_ analisi completa**
</dt> <dd>

È stata eseguita un'analisi completa.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**\_timeout del motivo MPRESOLVED \_ \_**
</dt> <dd>

Tempo sufficiente. Il valore predefinito è una settimana.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





