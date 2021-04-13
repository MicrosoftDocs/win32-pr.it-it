---
description: Recupera il numero di provider del servizio di crittografia (CSP).
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Proprietà ISCrdEnr:: CSPCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348516"
---
# <a name="iscrdenrcspcount-property"></a><span data-ttu-id="aa193-103">Proprietà ISCrdEnr:: CSPCount</span><span class="sxs-lookup"><span data-stu-id="aa193-103">ISCrdEnr::CSPCount property</span></span>

<span data-ttu-id="aa193-104">La proprietà **CSPCount** Recupera il numero di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="aa193-104">The **CSPCount** property retrieves the number of [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

<span data-ttu-id="aa193-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="aa193-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa193-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa193-106">Syntax</span></span>


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="aa193-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aa193-107">Property value</span></span>

<span data-ttu-id="aa193-108">Numero di CSP.</span><span class="sxs-lookup"><span data-stu-id="aa193-108">The number of CSPs.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa193-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="aa193-109">Error codes</span></span>

<span data-ttu-id="aa193-110">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aa193-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="aa193-111">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="aa193-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="aa193-112">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="aa193-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa193-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa193-113">Requirements</span></span>



| <span data-ttu-id="aa193-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa193-114">Requirement</span></span> | <span data-ttu-id="aa193-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aa193-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa193-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa193-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aa193-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="aa193-117">None supported</span></span><br/>                                                               |
| <span data-ttu-id="aa193-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa193-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aa193-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa193-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa193-120">DLL</span><span class="sxs-lookup"><span data-stu-id="aa193-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa193-121"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa193-121"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa193-122">IID</span><span class="sxs-lookup"><span data-stu-id="aa193-122">IID</span></span><br/>                      | <span data-ttu-id="aa193-123">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="aa193-123">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="aa193-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa193-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa193-125">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="aa193-125">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="aa193-126">**ISCrdEnr:: NomeCSP**</span><span class="sxs-lookup"><span data-stu-id="aa193-126">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> <dt>

[<span data-ttu-id="aa193-127">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="aa193-127">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
