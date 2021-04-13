---
title: Enumerazione MPTHREAT_TYPE (MpClient. h)
description: Tipi di minacce possibili.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_TYPE
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400498"
---
# <a name="mpthreat_type-enumeration"></a>\_Enumerazione del tipo MPTHREAT

Tipi di minacce possibili.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ tipo \_ KNOWNBAD**
</dt> <dd>

È stata rilevata una cattiva minaccia nota tramite firma.

</dd> <dt>

<span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_comportamento del tipo MPTHREAT \_**
</dt> <dd>

Minaccia sospetta rilevata tramite il monitoraggio del comportamento.

</dd> <dt>

<span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**\_tipo MPTHREAT \_ sconosciuto**
</dt> <dd>

Minacce sconosciute (non classificate).

</dd> <dt>

<span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ tipo \_ KNOWNGOOD**
</dt> <dd>

Una minaccia nota.

</dd> <dt>

<span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT di \_ tipo \_ NIS**
</dt> <dd>

Rilevamento delle minacce NIS.

</dd> <dt>

<span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT di \_ tipo \_ MaxValue**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





