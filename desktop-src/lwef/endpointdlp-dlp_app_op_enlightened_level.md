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
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="fc556-103">DLP_APP_OP_ENLIGHTENED_LEVEL struttura</span><span class="sxs-lookup"><span data-stu-id="fc556-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="fc556-104">Associa un'azione di prevenzione della perdita dei dati (DLP) dell'endpoint a un livello di imposizione.</span><span class="sxs-lookup"><span data-stu-id="fc556-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc556-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc556-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="fc556-106">Members</span><span class="sxs-lookup"><span data-stu-id="fc556-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc556-107">*Operazione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fc556-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc556-108">Valore dell'enumerazione [DlpActionType](endpointdlp-dlpactiontype.md) che specifica il tipo di azione DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="fc556-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="fc556-109">*AppEnforcementLevel* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fc556-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc556-110">Valore di [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) che specifica il livello di imposizione per il tipo di azione DLP dell'endpoint associato.</span><span class="sxs-lookup"><span data-stu-id="fc556-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="fc556-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc556-111">Remarks</span></span>

<span data-ttu-id="fc556-112">Passare una matrice di queste strutture in [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) per impostare la modalità di imposizione per un set di operazioni DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="fc556-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc556-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc556-113">Requirements</span></span>



| <span data-ttu-id="fc556-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc556-114">Requirement</span></span>          |    <span data-ttu-id="fc556-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fc556-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc556-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc556-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc556-117">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="fc556-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

