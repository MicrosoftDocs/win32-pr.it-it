---
description: Funzione definita dall'applicazione che crea un elenco di identificatori di sicurezza (SID) che si applicano a un client. AuthzComputeGroupsCallback è un segnaposto per il nome della funzione definita dall'applicazione.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Funzione di callback AuthzComputeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760829"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="b97dc-104">Funzione di callback AuthzComputeGroupsCallback</span><span class="sxs-lookup"><span data-stu-id="b97dc-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="b97dc-105">La funzione **AuthzComputeGroupsCallback** è una funzione definita dall'applicazione che crea un elenco di [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che si applicano a un client.</span><span class="sxs-lookup"><span data-stu-id="b97dc-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="b97dc-106">**AuthzComputeGroupsCallback** è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b97dc-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97dc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b97dc-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="b97dc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b97dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b97dc-109">*hAuthzClientContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b97dc-110">Handle per un contesto client.</span><span class="sxs-lookup"><span data-stu-id="b97dc-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="b97dc-111">*Argomenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b97dc-112">Dati passati nel parametro *DynamicGroupArgs* di una chiamata alla funzione [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)o [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .</span><span class="sxs-lookup"><span data-stu-id="b97dc-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="b97dc-113">*pSidAttrArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b97dc-114">Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di strutture di [**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="b97dc-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="b97dc-115">Queste strutture rappresentano i gruppi ai quali appartiene il client.</span><span class="sxs-lookup"><span data-stu-id="b97dc-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="b97dc-116">*pSidCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b97dc-117">Numero di strutture in *pSidAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="b97dc-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="b97dc-118">*pRestrictedSidAttrArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b97dc-119">Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di strutture di [**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="b97dc-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="b97dc-120">Queste strutture rappresentano i gruppi da cui il client è limitato.</span><span class="sxs-lookup"><span data-stu-id="b97dc-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="b97dc-121">*pRestrictedSidCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b97dc-122">Numero di strutture in *pSidRestrictedAttrArray*.</span><span class="sxs-lookup"><span data-stu-id="b97dc-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b97dc-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b97dc-123">Return value</span></span>

<span data-ttu-id="b97dc-124">Se la funzione restituisce correttamente un elenco di SID, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="b97dc-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="b97dc-125">Se la funzione ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="b97dc-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b97dc-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b97dc-126">Remarks</span></span>

<span data-ttu-id="b97dc-127">Le applicazioni possono inoltre aggiungere SID al contesto client chiamando [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span><span class="sxs-lookup"><span data-stu-id="b97dc-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="b97dc-128">Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="b97dc-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="b97dc-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b97dc-129">Requirements</span></span>



| <span data-ttu-id="b97dc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b97dc-130">Requirement</span></span> | <span data-ttu-id="b97dc-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b97dc-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b97dc-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b97dc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b97dc-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b97dc-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b97dc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b97dc-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b97dc-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="b97dc-136">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b97dc-136">Redistributable</span></span><br/>          | <span data-ttu-id="b97dc-137">Windows Server 2003 Administration Tools Pack in Windows XP</span><span class="sxs-lookup"><span data-stu-id="b97dc-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b97dc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b97dc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97dc-139">Funzioni di controllo di accesso di base</span><span class="sxs-lookup"><span data-stu-id="b97dc-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="b97dc-140">**AuthzAddSidsToContext**</span><span class="sxs-lookup"><span data-stu-id="b97dc-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="b97dc-141">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="b97dc-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="b97dc-142">**AuthzInitializeContextFromAuthzContext**</span><span class="sxs-lookup"><span data-stu-id="b97dc-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="b97dc-143">**AuthzInitializeContextFromSid**</span><span class="sxs-lookup"><span data-stu-id="b97dc-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="b97dc-144">**AuthzInitializeContextFromToken**</span><span class="sxs-lookup"><span data-stu-id="b97dc-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="b97dc-145">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="b97dc-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="b97dc-146">**SID \_ e \_ attributi**</span><span class="sxs-lookup"><span data-stu-id="b97dc-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

