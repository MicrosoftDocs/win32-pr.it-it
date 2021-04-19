---
description: Specifica il livello di imposizione di un'operazione dlp (Data Loss Prevention) dell'endpoint.
title: Enumerazione DlpAppEnforceLevel (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495772"
---
# <a name="dlpappenforcelevel-enumeration"></a>Enumerazione DlpAppEnforceLevel

Specifica il livello di imposizione di un'operazione DLP (Data Loss Prevention) dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>Costanti

<dl> <dt>

*DlpAppEnforceLevelNone* \[ Pollici\]
</dt> <dd>

Nessuna imposizione da parte dell'app. Il sistema DLP imposirà l'operazione.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[ Pollici\]
</dt> <dd>

L'app Tne userà le API DLP per notificare al sistema DLP l'operazione. Il sistema DLP imposirà l'operazione.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[ Pollici\]
</dt> <dd>

Non supportato nella versione corrente.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[ Pollici\]
</dt> <dd>

Non supportato nella versione corrente.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[ Pollici\]
</dt> <dd>

Valore massimo dell'enumerazione.

</dd> </dl>



## <a name="remarks"></a>Commenti

I valori di questa enumerazione vengono usati dalla [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) struttura .


## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |

