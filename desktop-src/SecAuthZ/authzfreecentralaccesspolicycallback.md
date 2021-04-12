---
description: La funzione AuthzFreeCentralAccessPolicyCallback è una funzione definita dall'applicazione che libera la memoria allocata dalla funzione AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Funzione di callback AuthzFreeCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234338"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="1e5a7-103">Funzione di callback AuthzFreeCentralAccessPolicyCallback</span><span class="sxs-lookup"><span data-stu-id="1e5a7-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="1e5a7-104">La funzione *AuthzFreeCentralAccessPolicyCallback* è una funzione definita dall'applicazione che libera la memoria allocata dalla funzione [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) .</span><span class="sxs-lookup"><span data-stu-id="1e5a7-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="1e5a7-105">*AuthzFreeCentralAccessPolicyCallback* è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e5a7-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5a7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e5a7-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="1e5a7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e5a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e5a7-108">*pCentralAccessPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e5a7-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e5a7-109">Puntatore ai criteri di accesso centrale da liberare.</span><span class="sxs-lookup"><span data-stu-id="1e5a7-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e5a7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e5a7-110">Return value</span></span>

<span data-ttu-id="1e5a7-111">Se la funzione ha esito positivo, la funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="1e5a7-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="1e5a7-112">Se la funzione non è in grado di eseguire la valutazione, viene restituito **false**.</span><span class="sxs-lookup"><span data-stu-id="1e5a7-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="1e5a7-113">Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="1e5a7-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e5a7-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e5a7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5a7-115">**\_informazioni init \_ AUTHZ**</span><span class="sxs-lookup"><span data-stu-id="1e5a7-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="1e5a7-116">*AuthzGetCentralAccessPolicyCallback*</span><span class="sxs-lookup"><span data-stu-id="1e5a7-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
