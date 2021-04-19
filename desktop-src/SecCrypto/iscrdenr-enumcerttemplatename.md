---
description: Enumera i nomi dei modelli di certificato.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Metodo ISCrdEnr:: enumCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317719"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="3223d-103">Metodo ISCrdEnr:: enumCertTemplateName</span><span class="sxs-lookup"><span data-stu-id="3223d-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="3223d-104">Il metodo **enumCertTemplateName** enumera i nomi dei modelli di certificato.</span><span class="sxs-lookup"><span data-stu-id="3223d-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="3223d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3223d-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="3223d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3223d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3223d-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3223d-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3223d-108">Indice in base zero per la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="3223d-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="3223d-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3223d-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3223d-110">Valore che determina se il modello di certificato enumerato si applica ai certificati utente o computer.</span><span class="sxs-lookup"><span data-stu-id="3223d-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="3223d-111">Se questo valore viene spaventato \_ \_ \_ \_ per la registrazione del modello di certificato utente (definito come 1), l'enumerazione si applica ai modelli di certificato utente.</span><span class="sxs-lookup"><span data-stu-id="3223d-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="3223d-112">Se questo valore viene spaventato \_ , registrare \_ \_ \_ il modello del certificato del computer (definito come 2), l'enumerazione si applica ai modelli di certificato del computer.</span><span class="sxs-lookup"><span data-stu-id="3223d-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="3223d-113">*pbstrCertTemplateName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3223d-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3223d-114">Puntatore a una stringa che restituisce il nome del modello di certificato enumerato.</span><span class="sxs-lookup"><span data-stu-id="3223d-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3223d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3223d-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="3223d-116">C++</span><span class="sxs-lookup"><span data-stu-id="3223d-116">C++</span></span>

<span data-ttu-id="3223d-117">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3223d-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="3223d-118">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="3223d-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="3223d-119">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="3223d-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="3223d-120">VB</span><span class="sxs-lookup"><span data-stu-id="3223d-120">VB</span></span>

<span data-ttu-id="3223d-121">Stringa che contiene il nome del modello di certificato enumerato.</span><span class="sxs-lookup"><span data-stu-id="3223d-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="3223d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3223d-122">Requirements</span></span>



| <span data-ttu-id="3223d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3223d-123">Requirement</span></span> | <span data-ttu-id="3223d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3223d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3223d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3223d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3223d-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3223d-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3223d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3223d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3223d-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3223d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3223d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3223d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3223d-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3223d-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="3223d-131">IID</span><span class="sxs-lookup"><span data-stu-id="3223d-131">IID</span></span><br/>                      | <span data-ttu-id="3223d-132">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="3223d-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3223d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3223d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3223d-134">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="3223d-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="3223d-135">**ISCrdEnr::getCertTemplateCount**</span><span class="sxs-lookup"><span data-stu-id="3223d-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="3223d-136">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="3223d-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="3223d-137">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="3223d-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




