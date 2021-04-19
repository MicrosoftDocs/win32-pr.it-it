---
description: Restituisce il numero di autorità di certificazione (CAs) disponibili per emettere un certificato in base al modello di certificato specificato.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Metodo ISCrdEnr:: getCACount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317718"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="ab940-103">Metodo ISCrdEnr:: getCACount</span><span class="sxs-lookup"><span data-stu-id="ab940-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="ab940-104">Il metodo **getCACount** restituisce il numero di [*autorità di certificazione*](../secgloss/c-gly.md) (CAS) disponibili per emettere un certificato in base al modello di certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="ab940-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab940-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab940-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="ab940-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab940-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab940-107">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab940-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab940-108">Stringa che rappresenta il nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="ab940-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="ab940-109">*pdwCACount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab940-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab940-110">Puntatore a un oggetto **Long** che restituisce il numero di autorità di certificazione disponibili che emetteranno un certificato per il modello di certificato specificato in *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="ab940-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab940-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab940-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="ab940-112">C++</span><span class="sxs-lookup"><span data-stu-id="ab940-112">C++</span></span>

<span data-ttu-id="ab940-113">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab940-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ab940-114">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="ab940-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ab940-115">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ab940-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="ab940-116">VB</span><span class="sxs-lookup"><span data-stu-id="ab940-116">VB</span></span>

<span data-ttu-id="ab940-117">Valore **Long** che rappresenta il numero di autorità di certificazione disponibili che emetteranno un certificato per il modello di certificato specificato in *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="ab940-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab940-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab940-118">Requirements</span></span>



| <span data-ttu-id="ab940-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab940-119">Requirement</span></span> | <span data-ttu-id="ab940-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ab940-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab940-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab940-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab940-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab940-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ab940-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab940-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab940-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab940-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab940-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ab940-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab940-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab940-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab940-127">IID</span><span class="sxs-lookup"><span data-stu-id="ab940-127">IID</span></span><br/>                      | <span data-ttu-id="ab940-128">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ab940-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ab940-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab940-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab940-130">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ab940-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ab940-131">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="ab940-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="ab940-132">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="ab940-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
