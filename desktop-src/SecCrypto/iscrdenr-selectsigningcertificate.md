---
description: Consente di visualizzare una finestra di dialogo Seleziona certificato, in cui è possibile selezionare un certificato di firma (noto anche come certificato agente di registrazione).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Metodo ISCrdEnr:: selectSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884850"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="ed991-103">Metodo ISCrdEnr:: selectSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="ed991-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="ed991-104">Il metodo **selectSigningCertificate** Visualizza una finestra di dialogo **Seleziona certificato** , che consente di selezionare un certificato di firma (noto anche come *certificato agente di registrazione*).</span><span class="sxs-lookup"><span data-stu-id="ed991-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="ed991-105">Prima di eseguire la registrazione per conto di utenti, è necessario selezionare un certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="ed991-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="ed991-106">La [*chiave privata*](../secgloss/p-gly.md) associata a questo certificato di firma viene usata per firmare una \# richiesta PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="ed991-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="ed991-107">PKCS \# 7, a sua volta, contiene la richiesta PKCS 10 dell'utente \# (che è firmata con la chiave privata dell'utente).</span><span class="sxs-lookup"><span data-stu-id="ed991-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed991-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed991-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="ed991-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed991-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed991-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed991-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed991-111">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="ed991-111">Reserved for future use.</span></span> <span data-ttu-id="ed991-112">Impostare questo valore su zero.</span><span class="sxs-lookup"><span data-stu-id="ed991-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ed991-113">*bstrCertTemplateName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed991-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed991-114">Stringa che rappresenta il nome del modello di certificato per il certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="ed991-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="ed991-115">Se è stato ottenuto un certificato EnrollmentAgent, è possibile usare il valore "EnrollmentAgent".</span><span class="sxs-lookup"><span data-stu-id="ed991-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed991-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed991-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="ed991-117">VB</span><span class="sxs-lookup"><span data-stu-id="ed991-117">VB</span></span>

<span data-ttu-id="ed991-118">Se il metodo ha esito positivo, il metodo restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ed991-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="ed991-119">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="ed991-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ed991-120">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ed991-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed991-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed991-121">Remarks</span></span>

<span data-ttu-id="ed991-122">Prima di eseguire la registrazione per conto di un utente, è innanzitutto necessario ottenere un certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="ed991-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="ed991-123">È possibile ottenere un certificato di firma tramite lo snap-in MMC di gestione certificati.</span><span class="sxs-lookup"><span data-stu-id="ed991-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="ed991-124">Il metodo **selectSigningCertificate** non ottiene il certificato di firma ma Visualizza una finestra di dialogo dei certificati di firma ottenuti in precedenza, consentendo di scegliere il certificato che verrà usato per firmare le richieste di registrazione per conto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ed991-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="ed991-125">Un'alternativa a **selectSigningCertificate** è [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="ed991-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="ed991-126">Dopo aver selezionato un certificato di firma, è possibile recuperarne il nome chiamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="ed991-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed991-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed991-127">Requirements</span></span>



| <span data-ttu-id="ed991-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed991-128">Requirement</span></span> | <span data-ttu-id="ed991-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed991-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed991-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed991-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed991-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ed991-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ed991-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed991-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed991-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed991-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed991-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ed991-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed991-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed991-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ed991-136">IID</span><span class="sxs-lookup"><span data-stu-id="ed991-136">IID</span></span><br/>                      | <span data-ttu-id="ed991-137">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ed991-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ed991-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed991-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed991-139">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ed991-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ed991-140">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="ed991-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
