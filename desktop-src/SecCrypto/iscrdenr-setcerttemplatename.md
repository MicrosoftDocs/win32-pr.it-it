---
description: Specifica il nome del modello di certificato.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Metodo ISCrdEnr:: setCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312802"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="074d3-103">Metodo ISCrdEnr:: setCertTemplateName</span><span class="sxs-lookup"><span data-stu-id="074d3-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="074d3-104">Il metodo **setCertTemplateName** specifica il nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="074d3-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="074d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="074d3-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="074d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="074d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074d3-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="074d3-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074d3-108">Valore che determina se è in corso l'impostazione del nome reale o del nome visualizzato del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="074d3-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="074d3-109">Se *dwFlags* presenta il valore SCard \_ Registra \_ il \_ \_ nome visualizzato \_ del modello di certificato, viene impostato il nome visualizzato del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="074d3-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="074d3-110">In caso contrario, viene impostato il nome reale del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="074d3-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="074d3-111">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="074d3-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="074d3-112">Nome del modello di certificato che verrà usato nella richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="074d3-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074d3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="074d3-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="074d3-114">VB</span><span class="sxs-lookup"><span data-stu-id="074d3-114">VB</span></span>

<span data-ttu-id="074d3-115">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="074d3-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="074d3-116">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="074d3-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="074d3-117">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="074d3-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="074d3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="074d3-118">Remarks</span></span>

<span data-ttu-id="074d3-119">Se non si imposta il nome del modello di certificato chiamando **ISCrdEnr:: setCertTemplateName**, il nome predefinito è il primo nome nell'elenco dei modelli di certificato disponibili.</span><span class="sxs-lookup"><span data-stu-id="074d3-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="074d3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="074d3-120">Requirements</span></span>



| <span data-ttu-id="074d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="074d3-121">Requirement</span></span> | <span data-ttu-id="074d3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="074d3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="074d3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="074d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="074d3-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="074d3-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="074d3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="074d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="074d3-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="074d3-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="074d3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="074d3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="074d3-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074d3-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="074d3-129">IID</span><span class="sxs-lookup"><span data-stu-id="074d3-129">IID</span></span><br/>                      | <span data-ttu-id="074d3-130">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="074d3-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="074d3-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="074d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074d3-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="074d3-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="074d3-133">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="074d3-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




