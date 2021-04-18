---
description: Specifica un certificato di firma (noto anche come certificato dell'agente di registrazione).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Metodo ISCrdEnr:: setSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319358"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="ee1bc-103">Metodo ISCrdEnr:: setSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="ee1bc-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="ee1bc-104">Il metodo **setSigningCertificate** specifica un certificato di firma (noto anche come *certificato dell'agente di registrazione*).</span><span class="sxs-lookup"><span data-stu-id="ee1bc-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="ee1bc-105">Prima di eseguire la registrazione per conto di utenti, è necessario selezionare o impostare un certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="ee1bc-106">La [*chiave privata*](../secgloss/p-gly.md) associata a questo certificato di firma viene usata per firmare una \# richiesta PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="ee1bc-107">PKCS \# 7, a sua volta, contiene la richiesta PKCS 10 dell'utente \# (che è firmata con la chiave privata dell'utente).</span><span class="sxs-lookup"><span data-stu-id="ee1bc-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee1bc-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="ee1bc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee1bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1bc-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee1bc-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1bc-111">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-111">Reserved for future use.</span></span> <span data-ttu-id="ee1bc-112">Impostare questo valore su zero.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ee1bc-113">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee1bc-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1bc-114">Nome del modello di certificato per il certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="ee1bc-115">Se è stato ottenuto un certificato EnrollmentAgent, è possibile usare il valore "EnrollmentAgent".</span><span class="sxs-lookup"><span data-stu-id="ee1bc-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1bc-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee1bc-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="ee1bc-117">VB</span><span class="sxs-lookup"><span data-stu-id="ee1bc-117">VB</span></span>

<span data-ttu-id="ee1bc-118">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ee1bc-119">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ee1bc-120">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ee1bc-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1bc-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee1bc-121">Remarks</span></span>

<span data-ttu-id="ee1bc-122">Prima di eseguire la registrazione per conto di un utente, è innanzitutto necessario ottenere un certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="ee1bc-123">È possibile ottenere un certificato di firma tramite lo snap-in MMC di gestione certificati.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="ee1bc-124">Il metodo **setSigningCertificate** non ottiene il certificato di firma ma informa il controllo di registrazione della smart card che in precedenza ha ottenuto il certificato di firma da usare.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="ee1bc-125">Il metodo **setSigningCertificate** Cerca nell'archivio "My" del chiamante il certificato di firma più recente corrispondente al modello di certificato specificato da *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="ee1bc-126">Un'alternativa a **setSigningCertificate** è **ISCrdEnr:: setSigningCertificate**.</span><span class="sxs-lookup"><span data-stu-id="ee1bc-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="ee1bc-127">Dopo aver impostato un certificato di firma, è possibile recuperarne il nome chiamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="ee1bc-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1bc-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee1bc-128">Requirements</span></span>



| <span data-ttu-id="ee1bc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1bc-129">Requirement</span></span> | <span data-ttu-id="ee1bc-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ee1bc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1bc-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee1bc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ee1bc-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ee1bc-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ee1bc-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee1bc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ee1bc-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee1bc-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee1bc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ee1bc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee1bc-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee1bc-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ee1bc-137">IID</span><span class="sxs-lookup"><span data-stu-id="ee1bc-137">IID</span></span><br/>                      | <span data-ttu-id="ee1bc-138">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ee1bc-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ee1bc-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee1bc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1bc-140">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ee1bc-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ee1bc-141">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="ee1bc-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
