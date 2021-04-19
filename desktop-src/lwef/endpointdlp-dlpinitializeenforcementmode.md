---
description: Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.
title: Funzione DlpInitializeEnforcementMode (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495731"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="12e52-103">Funzione DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="12e52-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="12e52-104">Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="12e52-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12e52-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="12e52-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12e52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e52-107">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="12e52-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12e52-108">Valore **DWORD** che specifica il numero di operazioni incluse nella *matrice OperationEnforcement.*</span><span class="sxs-lookup"><span data-stu-id="12e52-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="12e52-109">*OperationEnforcement* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="12e52-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12e52-110">Matrice di strutture [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) che specificano il livello di imposizione per un'operazione DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="12e52-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="12e52-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12e52-111">Return value</span></span>

<span data-ttu-id="12e52-112">Restituisce un HRESULT che include, ma non solo, i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="12e52-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="12e52-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="12e52-113">HRESULT</span></span> | <span data-ttu-id="12e52-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12e52-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="12e52-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="12e52-115">S_OK</span></span> | <span data-ttu-id="12e52-116">La funzione è stata completata correttamente</span><span class="sxs-lookup"><span data-stu-id="12e52-116">The function completed successfully</span></span> |
| <span data-ttu-id="12e52-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="12e52-117">E_INVALIDARG</span></span> | <span data-ttu-id="12e52-118">Uno o più parametri della funzione non sono validi.</span><span class="sxs-lookup"><span data-stu-id="12e52-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="12e52-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="12e52-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="12e52-120">Allocazione di memoria per l'operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="12e52-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="12e52-121">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="12e52-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="12e52-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12e52-122">Requirements</span></span>



| <span data-ttu-id="12e52-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e52-123">Requirement</span></span>          |    <span data-ttu-id="12e52-124">Valore</span><span class="sxs-lookup"><span data-stu-id="12e52-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12e52-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12e52-125">Minimum supported client</span></span><br/> | <span data-ttu-id="12e52-126">Windows 10, versione 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="12e52-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="12e52-127">DLL</span><span class="sxs-lookup"><span data-stu-id="12e52-127">DLL</span></span><br/>                      | <span data-ttu-id="12e52-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="12e52-128">EndpointDlp.dll</span></span> |