---
description: Imposta o Recupera il nome del provider del servizio di crittografia (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Proprietà ISCrdEnr:: NomeCSP'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058182"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="52a4d-103">Proprietà ISCrdEnr:: NomeCSP</span><span class="sxs-lookup"><span data-stu-id="52a4d-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="52a4d-104">La proprietà **NomeCSP** imposta o Recupera il nome del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="52a4d-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="52a4d-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="52a4d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a4d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52a4d-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="52a4d-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="52a4d-107">Property value</span></span>

<span data-ttu-id="52a4d-108">Nome del CSP.</span><span class="sxs-lookup"><span data-stu-id="52a4d-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52a4d-109">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="52a4d-109">Error codes</span></span>

<span data-ttu-id="52a4d-110">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52a4d-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="52a4d-111">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="52a4d-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="52a4d-112">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="52a4d-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52a4d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="52a4d-113">Remarks</span></span>

<span data-ttu-id="52a4d-114">Impostare questa proprietà per specificare il nome del CSP da usare con il controllo di registrazione delle smart card.</span><span class="sxs-lookup"><span data-stu-id="52a4d-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="52a4d-115">Ottenere questa proprietà per recuperare il nome del CSP specificato.</span><span class="sxs-lookup"><span data-stu-id="52a4d-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="52a4d-116">Se non si specifica un valore per questa proprietà, per impostazione predefinita la proprietà **NomeCSP** viene impostata sul nome nell'elenco dei CSP disponibili.</span><span class="sxs-lookup"><span data-stu-id="52a4d-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="52a4d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52a4d-117">Requirements</span></span>



| <span data-ttu-id="52a4d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a4d-118">Requirement</span></span> | <span data-ttu-id="52a4d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="52a4d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52a4d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a4d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52a4d-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="52a4d-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="52a4d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52a4d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52a4d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52a4d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52a4d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="52a4d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52a4d-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52a4d-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="52a4d-126">IID</span><span class="sxs-lookup"><span data-stu-id="52a4d-126">IID</span></span><br/>                      | <span data-ttu-id="52a4d-127">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="52a4d-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="52a4d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52a4d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a4d-129">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="52a4d-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="52a4d-130">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="52a4d-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="52a4d-131">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="52a4d-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
