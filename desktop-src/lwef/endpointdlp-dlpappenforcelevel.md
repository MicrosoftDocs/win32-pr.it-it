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
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="d345f-103">Enumerazione DlpAppEnforceLevel</span><span class="sxs-lookup"><span data-stu-id="d345f-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="d345f-104">Specifica il livello di imposizione di un'operazione DLP (Data Loss Prevention) dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="d345f-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d345f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d345f-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="d345f-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d345f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d345f-107">*DlpAppEnforceLevelNone* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d345f-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d345f-108">Nessuna imposizione da parte dell'app.</span><span class="sxs-lookup"><span data-stu-id="d345f-108">No enforcement by the app.</span></span> <span data-ttu-id="d345f-109">Il sistema DLP imposirà l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d345f-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="d345f-110">*DlpAppEnforceLevelNotify* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d345f-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d345f-111">L'app Tne userà le API DLP per notificare al sistema DLP l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d345f-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="d345f-112">Il sistema DLP imposirà l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d345f-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="d345f-113">*DlpAppEnforceLevelPrevent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d345f-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d345f-114">Non supportato nella versione corrente.</span><span class="sxs-lookup"><span data-stu-id="d345f-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="d345f-115">*DlpAppEnforceLevelFull* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d345f-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d345f-116">Non supportato nella versione corrente.</span><span class="sxs-lookup"><span data-stu-id="d345f-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="d345f-117">*DlpAppEnforceLevelCount* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d345f-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d345f-118">Valore massimo dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="d345f-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="d345f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d345f-119">Remarks</span></span>

<span data-ttu-id="d345f-120">I valori di questa enumerazione vengono usati dalla [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) struttura .</span><span class="sxs-lookup"><span data-stu-id="d345f-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="d345f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d345f-121">Requirements</span></span>



| <span data-ttu-id="d345f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d345f-122">Requirement</span></span>          |    <span data-ttu-id="d345f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d345f-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d345f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d345f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d345f-125">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="d345f-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

