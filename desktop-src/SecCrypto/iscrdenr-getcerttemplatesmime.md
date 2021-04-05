---
description: Usato per determinare se un modello di certificato contiene l' \_ \_ utilizzo della \_ chiave di protezione della posta elettronica szOID PKIX KP \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Metodo ISCrdEnr:: getCertTemplateSMIME'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884042"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="bd684-103">Metodo ISCrdEnr:: getCertTemplateSMIME</span><span class="sxs-lookup"><span data-stu-id="bd684-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="bd684-104">Il metodo **getCertTemplateSMIME** viene usato per determinare se un modello di certificato contiene l' \_ utilizzo della chiave di protezione della posta elettronica di szOID PKIX \_ KP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bd684-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="bd684-105">Se questo utilizzo della chiave fa parte del modello di certificato, il modello di certificato supporta le operazioni [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).</span><span class="sxs-lookup"><span data-stu-id="bd684-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd684-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd684-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="bd684-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd684-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd684-108">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd684-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd684-109">Nome del certificato sottoposto a query per l'utilizzo della chiave S/MIME.</span><span class="sxs-lookup"><span data-stu-id="bd684-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="bd684-110">*pdwCertTemplateSMIME* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd684-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd684-111">Puntatore a un valore **DWORD** che restituisce un valore di uno se *bstrCertTemplateName* supporta S/MIME. in caso contrario, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="bd684-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd684-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd684-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="bd684-113">C++</span><span class="sxs-lookup"><span data-stu-id="bd684-113">C++</span></span>

<span data-ttu-id="bd684-114">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bd684-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="bd684-115">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="bd684-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="bd684-116">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="bd684-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="bd684-117">VB</span><span class="sxs-lookup"><span data-stu-id="bd684-117">VB</span></span>

<span data-ttu-id="bd684-118">Valore **Long** di uno se *bstrCertTemplateName* supporta S/MIME; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="bd684-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd684-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd684-119">Remarks</span></span>

<span data-ttu-id="bd684-120">La costante per szOID \_ PKIX \_ KP \_ email \_ Protection è definita in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="bd684-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd684-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd684-121">Requirements</span></span>



| <span data-ttu-id="bd684-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd684-122">Requirement</span></span> | <span data-ttu-id="bd684-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bd684-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd684-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd684-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bd684-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bd684-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="bd684-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd684-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bd684-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd684-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd684-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bd684-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd684-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd684-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd684-130">IID</span><span class="sxs-lookup"><span data-stu-id="bd684-130">IID</span></span><br/>                      | <span data-ttu-id="bd684-131">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="bd684-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bd684-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd684-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd684-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="bd684-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="bd684-134">[**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd684-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
