---
title: MPTHREAT_TYPE enumerazione (MpClient.h)
description: Possibili tipi di minaccia.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE funzionalità dell'ambiente Windows legacy
- PMPTHREAT_TYPE puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: b858501603b67451db9b565609d0c263040d2186cf44d91646e6df6ce3871ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247142"
---
# <a name="mpthreat_type-enumeration"></a>Enumerazione MPTHREAT \_ TYPE

Possibili tipi di minaccia.

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

<span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**TIPO MPTHREAT \_ \_ NOTOBAD**
</dt> <dd>

Rilevata minaccia non valida nota tramite firma.

</dd> <dt>

<span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**COMPORTAMENTO DEL TIPO \_ \_ MPTHREAT**
</dt> <dd>

Rilevata minaccia sospetta tramite il monitoraggio del comportamento.

</dd> <dt>

<span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**TIPO MPTHREAT \_ \_ SCONOSCIUTO**
</dt> <dd>

Minacce sconosciute (non classificate).

</dd> <dt>

<span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**TIPO MPTHREAT \_ \_ KNOWNGOOD**
</dt> <dd>

Minaccia nota.

</dd> <dt>

<span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ TYPE \_ NIS**
</dt> <dd>

Rilevamento delle minacce NIS.

</dd> <dt>

<span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**TIPO MPTHREAT \_ \_ MAXVALUE**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





