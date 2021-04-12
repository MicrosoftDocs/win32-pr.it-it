---
description: Funzione definita dall'applicazione che gestisce le voci di controllo di accesso (ACE) di callback durante un controllo di accesso.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Funzione di callback AuthzAccessCheckCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234340"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="14b7c-103">Funzione di callback AuthzAccessCheckCallback</span><span class="sxs-lookup"><span data-stu-id="14b7c-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="14b7c-104">La funzione **AuthzAccessCheckCallback** è una funzione definita dall'applicazione che gestisce le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) di callback durante un controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="14b7c-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="14b7c-105">**AuthzAccessCheckCallback** è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14b7c-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="14b7c-106">L'applicazione registra questo callback chiamando [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span><span class="sxs-lookup"><span data-stu-id="14b7c-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="14b7c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14b7c-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="14b7c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14b7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b7c-109">*hAuthzClientContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b7c-110">Handle per un contesto client.</span><span class="sxs-lookup"><span data-stu-id="14b7c-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="14b7c-111">*velocità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b7c-112">Puntatore alla voce ACE da valutare per l'inclusione nella chiamata alla funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="14b7c-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="14b7c-113">*pArgs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14b7c-114">Dati passati nel parametro *DynamicGroupArgs* della chiamata a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) o [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span><span class="sxs-lookup"><span data-stu-id="14b7c-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="14b7c-115">*pbAceApplicable* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14b7c-116">Puntatore a una variabile booleana che riceve i risultati della valutazione della logica definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14b7c-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="14b7c-117">I risultati sono **true** se la logica determina che la voce ACE è applicabile e verrà inclusa nella chiamata a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); in caso contrario, i risultati sono **false**.</span><span class="sxs-lookup"><span data-stu-id="14b7c-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b7c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14b7c-118">Return value</span></span>

<span data-ttu-id="14b7c-119">Se la funzione ha esito positivo, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="14b7c-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="14b7c-120">Se la funzione non è in grado di eseguire la valutazione, viene restituito **false**.</span><span class="sxs-lookup"><span data-stu-id="14b7c-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="14b7c-121">Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="14b7c-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b7c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="14b7c-122">Remarks</span></span>

<span data-ttu-id="14b7c-123">Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. in caso contrario, il termine espressione condizionale che vi fa riferimento restituisce Unknown.</span><span class="sxs-lookup"><span data-stu-id="14b7c-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="14b7c-124">Per ulteriori informazioni, vedere il funzionamento di [AccessCheck](how-dacls-control-access-to-an-object.md) e panoramica dei [criteri di autorizzazione centralizzati](centralized-authorization-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="14b7c-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b7c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14b7c-125">Requirements</span></span>



| <span data-ttu-id="14b7c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b7c-126">Requirement</span></span> | <span data-ttu-id="14b7c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="14b7c-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="14b7c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b7c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="14b7c-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="14b7c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b7c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="14b7c-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14b7c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="14b7c-132">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="14b7c-132">Redistributable</span></span><br/>          | <span data-ttu-id="14b7c-133">Windows Server 2003 Administration Tools Pack in Windows XP</span><span class="sxs-lookup"><span data-stu-id="14b7c-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14b7c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14b7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b7c-135">Funzioni di controllo di accesso di base</span><span class="sxs-lookup"><span data-stu-id="14b7c-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="14b7c-136">Criteri di autorizzazione centralizzati</span><span class="sxs-lookup"><span data-stu-id="14b7c-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="14b7c-137">Funzionamento di AccessCheck</span><span class="sxs-lookup"><span data-stu-id="14b7c-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="14b7c-138">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="14b7c-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="14b7c-139">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="14b7c-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="14b7c-140">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="14b7c-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="14b7c-141">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="14b7c-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

