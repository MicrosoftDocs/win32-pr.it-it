---
description: Specifica il livello di imposizione di un'operazione DLP (Data Loss Prevention) dell'endpoint.
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
ms.openlocfilehash: 99bd06a41c88ff0b5a02b9b329877c015aea7dfb3fdbc58fea3c2e305829faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349351"
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

