---
description: Handle per l'oggetto Criteri locali.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050071"
---
# <a name="lsa_handle"></a><span data-ttu-id="2804b-103">\_handle LSA</span><span class="sxs-lookup"><span data-stu-id="2804b-103">LSA\_HANDLE</span></span>

<span data-ttu-id="2804b-104">Il tipo di dati dell' **\_ handle LSA** è un handle per l'oggetto [**criterio**](policy-object.md) locale.</span><span class="sxs-lookup"><span data-stu-id="2804b-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="2804b-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="2804b-105">Remarks</span></span>

<span data-ttu-id="2804b-106">Prima di poter usare l'API criteri locali, l'applicazione deve aprire un handle per un oggetto [**criteri**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="2804b-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="2804b-107">A tale scopo, chiamare [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span><span class="sxs-lookup"><span data-stu-id="2804b-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="2804b-108">Questa funzione restituisce un handle che l'applicazione può quindi specificare nelle successive chiamate di funzione dei criteri LSA.</span><span class="sxs-lookup"><span data-stu-id="2804b-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="2804b-109">A ogni handle è associato un set di autorizzazioni che determina le operazioni che l'applicazione può eseguire sull'oggetto [**criterio**](policy-object.md) utilizzando l'handle.</span><span class="sxs-lookup"><span data-stu-id="2804b-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="2804b-110">L'applicazione può aprire più di un handle per l'oggetto **criteri** alla volta.</span><span class="sxs-lookup"><span data-stu-id="2804b-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="2804b-111">Quando un handle non è più necessario, l'applicazione deve chiuderla chiamando [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span><span class="sxs-lookup"><span data-stu-id="2804b-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="2804b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2804b-112">Requirements</span></span>



| <span data-ttu-id="2804b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2804b-113">Requirement</span></span> | <span data-ttu-id="2804b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2804b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2804b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2804b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2804b-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2804b-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2804b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2804b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2804b-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2804b-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2804b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2804b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2804b-120"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2804b-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2804b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2804b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2804b-122">**LsaClose**</span><span class="sxs-lookup"><span data-stu-id="2804b-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="2804b-123">**LsaOpenPolicy**</span><span class="sxs-lookup"><span data-stu-id="2804b-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

