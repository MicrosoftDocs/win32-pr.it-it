---
description: Funzione definita dall'applicazione che libera la memoria allocata dalla funzione AuthzComputeGroupsCallback. AuthzFreeGroupsCallback è un segnaposto per il nome della funzione definita dall'applicazione.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Funzione di callback AuthzFreeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760826"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="e1093-104">Funzione di callback AuthzFreeGroupsCallback</span><span class="sxs-lookup"><span data-stu-id="e1093-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="e1093-105">La funzione **AuthzFreeGroupsCallback** è una funzione definita dall'applicazione che libera la memoria allocata dalla funzione [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) .</span><span class="sxs-lookup"><span data-stu-id="e1093-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="e1093-106">**AuthzFreeGroupsCallback** è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e1093-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1093-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1093-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="e1093-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1093-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1093-109">*pSidAttrArray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1093-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1093-110">Puntatore alla memoria allocata da [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span><span class="sxs-lookup"><span data-stu-id="e1093-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1093-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1093-111">Return value</span></span>

<span data-ttu-id="e1093-112">Questa funzione di callback non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e1093-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1093-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1093-113">Remarks</span></span>

<span data-ttu-id="e1093-114">Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="e1093-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1093-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1093-115">Requirements</span></span>



| <span data-ttu-id="e1093-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1093-116">Requirement</span></span> | <span data-ttu-id="e1093-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e1093-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="e1093-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1093-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1093-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1093-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e1093-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1093-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1093-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1093-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="e1093-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e1093-122">Redistributable</span></span><br/>          | <span data-ttu-id="e1093-123">Windows Server 2003 Administration Tools Pack in Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1093-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1093-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1093-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1093-125">Funzioni di controllo di accesso di base</span><span class="sxs-lookup"><span data-stu-id="e1093-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="e1093-126">**AuthzComputeGroupsCallback**</span><span class="sxs-lookup"><span data-stu-id="e1093-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




