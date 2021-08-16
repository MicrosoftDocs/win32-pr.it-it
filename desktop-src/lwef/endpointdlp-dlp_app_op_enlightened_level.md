---
description: Associa un'azione di prevenzione della perdita dei dati dell'endpoint a un livello di imposizione.
title: DLP_APP_OP_ENLIGHTENED_LEVEL struttura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e47fa7705701701af2fc0832c5ea27cfdc7d1e67948ec095f3c24837a93de18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610481"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL struttura

Associa un'azione di prevenzione della perdita dei dati dell'endpoint a un livello di imposizione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Members

<dl> <dt>

*Operazione* \[ Pollici\]
</dt> <dd>

Valore dell'enumerazione [DlpActionType](endpointdlp-dlpactiontype.md) che specifica il tipo di azione DLP dell'endpoint.

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[ Pollici\]
</dt> <dd>

Valore di [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) che specifica il livello di imposizione per il tipo di azione DLP dell'endpoint associato.

</dd> </dl>





## <a name="remarks"></a>Commenti

Passare una matrice di queste strutture in [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) per impostare la modalità di imposizione per un set di operazioni DLP dell'endpoint.

## <a name="requirements"></a>Requisiti



| Requisito          |    Valore                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, versione 1809 (10.0; Build 17763)           |

