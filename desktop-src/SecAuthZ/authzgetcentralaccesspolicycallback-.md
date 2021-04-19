---
description: La funzione AuthzGetCentralAccessPolicyCallback è una funzione definita dall'applicazione che recupera i criteri di accesso centrale. AuthzGetCentralAccessPolicyCallback è un segnaposto per il nome della funzione definita dall'applicazione.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Funzione di callback AuthzGetCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319921"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="01a4d-104">Funzione di callback AuthzGetCentralAccessPolicyCallback</span><span class="sxs-lookup"><span data-stu-id="01a4d-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="01a4d-105">La funzione *AuthzGetCentralAccessPolicyCallback* è una funzione definita dall'applicazione che recupera i criteri di accesso centrale.</span><span class="sxs-lookup"><span data-stu-id="01a4d-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="01a4d-106">*AuthzGetCentralAccessPolicyCallback* è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="01a4d-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a4d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01a4d-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="01a4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01a4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a4d-109">*hAuthzClientContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a4d-110">Handle per il contesto client.</span><span class="sxs-lookup"><span data-stu-id="01a4d-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="01a4d-111">*capiti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01a4d-112">ID dei criteri di accesso centrale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="01a4d-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="01a4d-113">*pArgs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01a4d-114">Argomenti facoltativi passati alla funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) tramite il membro **OptionalArguments** della struttura della [**\_ \_ richiesta di accesso AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .</span><span class="sxs-lookup"><span data-stu-id="01a4d-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="01a4d-115">*pCentralAccessPolicyApplicable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01a4d-116">Puntatore a un valore booleano utilizzato dal gestore delle risorse per indicare se è necessario utilizzare un criterio di accesso centrale durante la valutazione dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="01a4d-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="01a4d-117">*ppCentralAccessPolicy* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01a4d-118">Puntatore ai criteri di accesso centrale da utilizzare per la valutazione dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="01a4d-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="01a4d-119">Se questo valore è **null**, viene applicato il limite predefinito.</span><span class="sxs-lookup"><span data-stu-id="01a4d-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a4d-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01a4d-120">Return value</span></span>

<span data-ttu-id="01a4d-121">Se la funzione ha esito positivo, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="01a4d-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="01a4d-122">Se la funzione non è in grado di eseguire la valutazione, viene restituito **false**.</span><span class="sxs-lookup"><span data-stu-id="01a4d-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="01a4d-123">Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="01a4d-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a4d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01a4d-124">Requirements</span></span>



| <span data-ttu-id="01a4d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a4d-125">Requirement</span></span> | <span data-ttu-id="01a4d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="01a4d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="01a4d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a4d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="01a4d-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="01a4d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a4d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="01a4d-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="01a4d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="01a4d-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="01a4d-131">Redistributable</span></span><br/>          | <span data-ttu-id="01a4d-132">Windows Server 2003 Administration Tools Pack in Windows XP</span><span class="sxs-lookup"><span data-stu-id="01a4d-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01a4d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01a4d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a4d-134">**\_richiesta di accesso AUTHZ \_**</span><span class="sxs-lookup"><span data-stu-id="01a4d-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="01a4d-135">**\_informazioni init \_ AUTHZ**</span><span class="sxs-lookup"><span data-stu-id="01a4d-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="01a4d-136">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="01a4d-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

