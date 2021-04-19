---
description: Enumera il nome delle autorità di certificazione (CAs) per un determinato nome del modello di certificato.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Metodo ISCrdEnr:: enumCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317720"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="02cf8-103">Metodo ISCrdEnr:: enumCAName</span><span class="sxs-lookup"><span data-stu-id="02cf8-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="02cf8-104">Il metodo **enumCAName** enumera il nome dell'autorità di [*certificazione*](../secgloss/c-gly.md) (CAS) per un determinato nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="02cf8-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cf8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02cf8-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="02cf8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02cf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02cf8-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02cf8-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02cf8-108">Indice in base zero per la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="02cf8-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="02cf8-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02cf8-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02cf8-110">Valore che determina se il nome fa riferimento al nome della CA o al nome del computer della CA.</span><span class="sxs-lookup"><span data-stu-id="02cf8-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="02cf8-111">Se questo valore viene spaventato \_ , registrare il \_ nome del computer della CA \_ \_ (definito come 0x01), il nome si riferisce al nome del computer della CA.</span><span class="sxs-lookup"><span data-stu-id="02cf8-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="02cf8-112">In caso contrario, il nome si riferisce al nome della CA.</span><span class="sxs-lookup"><span data-stu-id="02cf8-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="02cf8-113">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02cf8-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02cf8-114">Nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="02cf8-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="02cf8-115">*pbstrCAName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="02cf8-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02cf8-116">Puntatore a una stringa che restituisce il nome dell'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="02cf8-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02cf8-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02cf8-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="02cf8-118">C++</span><span class="sxs-lookup"><span data-stu-id="02cf8-118">C++</span></span>

<span data-ttu-id="02cf8-119">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02cf8-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="02cf8-120">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="02cf8-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="02cf8-121">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="02cf8-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="02cf8-122">VB</span><span class="sxs-lookup"><span data-stu-id="02cf8-122">VB</span></span>

<span data-ttu-id="02cf8-123">Stringa che rappresenta il nome dell'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="02cf8-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="02cf8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02cf8-124">Requirements</span></span>



| <span data-ttu-id="02cf8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="02cf8-125">Requirement</span></span> | <span data-ttu-id="02cf8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="02cf8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02cf8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02cf8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02cf8-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02cf8-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="02cf8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02cf8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02cf8-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02cf8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02cf8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="02cf8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02cf8-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02cf8-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="02cf8-133">IID</span><span class="sxs-lookup"><span data-stu-id="02cf8-133">IID</span></span><br/>                      | <span data-ttu-id="02cf8-134">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="02cf8-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="02cf8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02cf8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cf8-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="02cf8-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="02cf8-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="02cf8-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="02cf8-138">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="02cf8-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="02cf8-139">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="02cf8-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
