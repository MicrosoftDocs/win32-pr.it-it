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
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495788"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL struttura

Associa un'azione di prevenzione della perdita dei dati (DLP) dell'endpoint a un livello di imposizione.

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

