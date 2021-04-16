---
description: Enumera il nome dei provider del servizio di crittografia (CSP) disponibili.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Metodo ISCrdEnr:: enumCSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529994"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="153f0-103">Metodo ISCrdEnr:: enumCSPName</span><span class="sxs-lookup"><span data-stu-id="153f0-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="153f0-104">Il metodo **enumCSPName** enumera il nome dei [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) disponibili.</span><span class="sxs-lookup"><span data-stu-id="153f0-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="153f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="153f0-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="153f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="153f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153f0-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="153f0-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f0-108">Indice in base zero per la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="153f0-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="153f0-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="153f0-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="153f0-110">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="153f0-110">Reserved for future use.</span></span> <span data-ttu-id="153f0-111">Impostare questo valore su zero.</span><span class="sxs-lookup"><span data-stu-id="153f0-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="153f0-112">*pbstrCSPName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="153f0-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="153f0-113">Puntatore a una stringa che restituisce il nome del CSP enumerato.</span><span class="sxs-lookup"><span data-stu-id="153f0-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="153f0-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="153f0-115">C++</span><span class="sxs-lookup"><span data-stu-id="153f0-115">C++</span></span>

<span data-ttu-id="153f0-116">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="153f0-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="153f0-117">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="153f0-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="153f0-118">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="153f0-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="153f0-119">VB</span><span class="sxs-lookup"><span data-stu-id="153f0-119">VB</span></span>

<span data-ttu-id="153f0-120">Stringa che rappresenta il nome del CSP enumerato.</span><span class="sxs-lookup"><span data-stu-id="153f0-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="153f0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="153f0-121">Requirements</span></span>



| <span data-ttu-id="153f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="153f0-122">Requirement</span></span> | <span data-ttu-id="153f0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="153f0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="153f0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="153f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="153f0-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="153f0-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="153f0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="153f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="153f0-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="153f0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="153f0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="153f0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153f0-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153f0-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="153f0-130">IID</span><span class="sxs-lookup"><span data-stu-id="153f0-130">IID</span></span><br/>                      | <span data-ttu-id="153f0-131">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="153f0-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="153f0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="153f0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153f0-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="153f0-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="153f0-134">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="153f0-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="153f0-135">**ISCrdEnr:: NomeCSP**</span><span class="sxs-lookup"><span data-stu-id="153f0-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 
