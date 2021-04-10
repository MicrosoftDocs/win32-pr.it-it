---
description: Recupera il numero di modelli di certificato.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Metodo ISCrdEnr:: getCertTemplateCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884853"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="c7574-103">Metodo ISCrdEnr:: getCertTemplateCount</span><span class="sxs-lookup"><span data-stu-id="c7574-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="c7574-104">Il metodo **getCertTemplateCount** Recupera il numero di modelli di certificato.</span><span class="sxs-lookup"><span data-stu-id="c7574-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7574-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7574-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="c7574-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7574-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7574-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7574-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7574-108">Valore che determina se il modello è per i certificati utente o computer.</span><span class="sxs-lookup"><span data-stu-id="c7574-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="c7574-109">Se questo valore viene spaventato \_ \_ \_ \_ per la registrazione del modello di certificato utente (definito come 1), il conteggio restituito sarà per i modelli di certificato utente.</span><span class="sxs-lookup"><span data-stu-id="c7574-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="c7574-110">Se questo valore viene spaventato \_ , registrare \_ \_ \_ il modello di certificato del computer (definito come 2) il numero restituito sarà per i modelli di certificato del computer.</span><span class="sxs-lookup"><span data-stu-id="c7574-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="c7574-111">*pdwCertTemplateCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c7574-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7574-112">Puntatore a un oggetto **Long** che restituisce il numero di modelli di certificato.</span><span class="sxs-lookup"><span data-stu-id="c7574-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7574-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7574-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="c7574-114">C++</span><span class="sxs-lookup"><span data-stu-id="c7574-114">C++</span></span>

<span data-ttu-id="c7574-115">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7574-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="c7574-116">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="c7574-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c7574-117">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="c7574-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="c7574-118">VB</span><span class="sxs-lookup"><span data-stu-id="c7574-118">VB</span></span>

<span data-ttu-id="c7574-119">Valore **Long** che rappresenta il numero di modelli di certificato.</span><span class="sxs-lookup"><span data-stu-id="c7574-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7574-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7574-120">Requirements</span></span>



| <span data-ttu-id="c7574-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7574-121">Requirement</span></span> | <span data-ttu-id="c7574-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c7574-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7574-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7574-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7574-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c7574-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7574-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7574-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7574-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7574-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7574-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c7574-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7574-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7574-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7574-129">IID</span><span class="sxs-lookup"><span data-stu-id="c7574-129">IID</span></span><br/>                      | <span data-ttu-id="c7574-130">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="c7574-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c7574-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7574-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7574-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="c7574-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="c7574-133">**ISCrdEnr::enumCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="c7574-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




