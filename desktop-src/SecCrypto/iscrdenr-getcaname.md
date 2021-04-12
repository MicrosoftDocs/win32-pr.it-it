---
description: Recupera il nome dell'autorità di certificazione (CA) specificata per un modello di certificato specificato.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Metodo ISCrdEnr:: getCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233501"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="69824-103">Metodo ISCrdEnr:: getCAName</span><span class="sxs-lookup"><span data-stu-id="69824-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="69824-104">Il metodo **getCAName** Recupera il nome dell'autorità di [*certificazione*](../secgloss/c-gly.md) (CA) specificata per un modello di certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="69824-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="69824-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69824-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="69824-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69824-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69824-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69824-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69824-108">Valore che determina se il nome fa riferimento al nome della CA o al nome del computer della CA.</span><span class="sxs-lookup"><span data-stu-id="69824-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="69824-109">Se questo valore viene spaventato \_ registrare il \_ nome del computer della CA \_ \_ (definito come 0x01), il nome si riferisce al nome del computer della CA. in caso contrario, il nome fa riferimento al nome della CA.</span><span class="sxs-lookup"><span data-stu-id="69824-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="69824-110">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69824-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69824-111">Nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="69824-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="69824-112">*pbstrCAName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69824-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69824-113">Puntatore a una stringa che restituisce il nome dell'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="69824-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69824-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69824-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="69824-115">C++</span><span class="sxs-lookup"><span data-stu-id="69824-115">C++</span></span>

<span data-ttu-id="69824-116">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69824-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="69824-117">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="69824-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="69824-118">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="69824-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="69824-119">VB</span><span class="sxs-lookup"><span data-stu-id="69824-119">VB</span></span>

<span data-ttu-id="69824-120">Stringa che rappresenta il nome dell'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="69824-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="69824-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="69824-121">Remarks</span></span>

<span data-ttu-id="69824-122">Il nome dell'autorità di certificazione predefinito è il primo nome nell'elenco di autorità di certificazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="69824-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="69824-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69824-123">Requirements</span></span>



| <span data-ttu-id="69824-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="69824-124">Requirement</span></span> | <span data-ttu-id="69824-125">Valore</span><span class="sxs-lookup"><span data-stu-id="69824-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69824-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69824-126">Minimum supported client</span></span><br/> | <span data-ttu-id="69824-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69824-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="69824-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69824-128">Minimum supported server</span></span><br/> | <span data-ttu-id="69824-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69824-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69824-130">DLL</span><span class="sxs-lookup"><span data-stu-id="69824-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69824-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69824-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="69824-132">IID</span><span class="sxs-lookup"><span data-stu-id="69824-132">IID</span></span><br/>                      | <span data-ttu-id="69824-133">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="69824-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="69824-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69824-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69824-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="69824-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="69824-136">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="69824-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="69824-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="69824-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="69824-138">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="69824-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
