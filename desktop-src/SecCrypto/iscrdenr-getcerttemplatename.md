---
description: Recupera il nome del modello di certificato.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Metodo ISCrdEnr:: getCertTemplateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233499"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="ac827-103">Metodo ISCrdEnr:: getCertTemplateName</span><span class="sxs-lookup"><span data-stu-id="ac827-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="ac827-104">Il metodo **getCertTemplateName** Recupera il nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="ac827-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac827-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac827-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="ac827-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac827-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac827-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac827-108">Valore che determina se viene restituito il nome reale o il nome visualizzato del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="ac827-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="ac827-109">Se *dwFlags* presenta il valore SCard \_ Registra \_ il \_ \_ nome visualizzato del modello \_ di certificato, viene recuperato il nome visualizzato del modello di certificato; in caso contrario, viene visualizzato il nome effettivo del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="ac827-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="ac827-110">*pbstrCertTemplateName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac827-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac827-111">Puntatore a una stringa che restituisce il nome del modello di certificato che verrà usato nella [*richiesta di certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ac827-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac827-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac827-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="ac827-113">C++</span><span class="sxs-lookup"><span data-stu-id="ac827-113">C++</span></span>

<span data-ttu-id="ac827-114">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac827-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ac827-115">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="ac827-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ac827-116">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ac827-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="ac827-117">VB</span><span class="sxs-lookup"><span data-stu-id="ac827-117">VB</span></span>

<span data-ttu-id="ac827-118">Stringa che rappresenta il nome del modello di certificato che verrà utilizzato nella [*richiesta di certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ac827-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac827-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac827-119">Remarks</span></span>

<span data-ttu-id="ac827-120">Se non si imposta il nome del modello di certificato chiamando [**ISCrdEnr:: setCertTemplateName**](iscrdenr-setcerttemplatename.md), il nome predefinito è il primo nome nell'elenco dei modelli di certificato disponibili.</span><span class="sxs-lookup"><span data-stu-id="ac827-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac827-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac827-121">Requirements</span></span>



| <span data-ttu-id="ac827-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac827-122">Requirement</span></span> | <span data-ttu-id="ac827-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ac827-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac827-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac827-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ac827-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ac827-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ac827-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac827-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ac827-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac827-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac827-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ac827-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac827-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac827-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ac827-130">IID</span><span class="sxs-lookup"><span data-stu-id="ac827-130">IID</span></span><br/>                      | <span data-ttu-id="ac827-131">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ac827-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ac827-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac827-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac827-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ac827-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ac827-134">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="ac827-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
