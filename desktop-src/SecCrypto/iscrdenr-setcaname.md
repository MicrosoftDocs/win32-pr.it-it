---
description: Specifica il nome dell'autorità di certificazione (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Metodo ISCrdEnr:: setCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316659"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="129d5-103">Metodo ISCrdEnr:: setCAName</span><span class="sxs-lookup"><span data-stu-id="129d5-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="129d5-104">Il metodo **setCAName** specifica il nome dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="129d5-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="129d5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="129d5-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="129d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="129d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129d5-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="129d5-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="129d5-108">Valore che specifica se il nome fa riferimento al nome della CA o al nome del computer della CA.</span><span class="sxs-lookup"><span data-stu-id="129d5-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="129d5-109">Se questo valore viene spaventato \_ , registrare il \_ nome del computer della CA \_ \_ (definito come 0x01), il nome si riferisce al nome del computer della CA.</span><span class="sxs-lookup"><span data-stu-id="129d5-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="129d5-110">In caso contrario, il nome fa riferimento al nome della CA.</span><span class="sxs-lookup"><span data-stu-id="129d5-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="129d5-111">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="129d5-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="129d5-112">Nome del modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="129d5-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="129d5-113">*bstrCAName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="129d5-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="129d5-114">Nome della CA da usare con il modello di certificato specificato da *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="129d5-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129d5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="129d5-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="129d5-116">VB</span><span class="sxs-lookup"><span data-stu-id="129d5-116">VB</span></span>

<span data-ttu-id="129d5-117">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="129d5-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="129d5-118">Un valore di S \_ OK indica che la chiamata ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="129d5-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="129d5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="129d5-119">Remarks</span></span>

<span data-ttu-id="129d5-120">Utilizzare questo metodo per specificare una CA per un modello di certificato.</span><span class="sxs-lookup"><span data-stu-id="129d5-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="129d5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="129d5-121">Requirements</span></span>



| <span data-ttu-id="129d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="129d5-122">Requirement</span></span> | <span data-ttu-id="129d5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="129d5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="129d5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="129d5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="129d5-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="129d5-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="129d5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="129d5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="129d5-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="129d5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="129d5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="129d5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="129d5-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="129d5-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="129d5-130">IID</span><span class="sxs-lookup"><span data-stu-id="129d5-130">IID</span></span><br/>                      | <span data-ttu-id="129d5-131">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="129d5-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="129d5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="129d5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="129d5-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="129d5-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="129d5-134">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="129d5-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="129d5-135">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="129d5-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
