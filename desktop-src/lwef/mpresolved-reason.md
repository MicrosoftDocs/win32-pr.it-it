---
title: MPRESOLVED_REASON enumerazione (MpClient.h)
description: Possibili motivi della risoluzione di un errore di correzione.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON funzionalità dell'Windows legacy
- PMPRESOLVED_REASON puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: a365ef55d9fe2d76e619f3c772cc1df2e6c5e1c8c33721f24dc844d064b33398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975981"
---
# <a name="mpresolved_reason-enumeration"></a>Enumerazione MPRESOLVED \_ REASON

Possibili motivi della risoluzione di un errore di correzione.

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

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MOTIVO MPRESOLVED \_ \_ UNKNOWN**
</dt> <dd>

In uno stato di errore.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED \_ REASON \_ FULL \_ SCAN**
</dt> <dd>

È stata eseguita un'analisi completa.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**TIMEOUT DEL MOTIVO MPRESOLVED \_ \_ \_**
</dt> <dd>

È passato tempo sufficiente. Il valore predefinito è una settimana.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





