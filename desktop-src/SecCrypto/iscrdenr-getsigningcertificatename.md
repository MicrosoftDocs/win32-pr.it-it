---
description: Recupera il nome dell'oggetto dal certificato di firma.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Metodo ISCrdEnr:: getSigningCertificateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401745"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="fff30-103">Metodo ISCrdEnr:: getSigningCertificateName</span><span class="sxs-lookup"><span data-stu-id="fff30-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="fff30-104">Il metodo **getSigningCertificateName** Recupera il nome dell'oggetto dal certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="fff30-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="fff30-105">Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="fff30-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="fff30-106">Questo metodo chiama la [](../secgloss/c-gly.md) funzione CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="fff30-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="fff30-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fff30-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="fff30-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fff30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff30-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fff30-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff30-110">Valore che determina se il certificato viene visualizzato in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="fff30-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="fff30-111">Se questo valore viene spaventato \_ \_ , nessun certificato di \_ visualizzazione \_ (definito come 0x01), il certificato di firma non viene visualizzato; qualsiasi altro valore genera il certificato di firma visualizzato nella finestra di dialogo **certificato** .</span><span class="sxs-lookup"><span data-stu-id="fff30-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="fff30-112">*pbstrSigningCertName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fff30-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fff30-113">Puntatore a una stringa che restituisce il nome del certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="fff30-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="fff30-114">Il certificato di firma verrà usato per firmare la [*richiesta di certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fff30-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fff30-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fff30-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="fff30-116">C++</span><span class="sxs-lookup"><span data-stu-id="fff30-116">C++</span></span>

<span data-ttu-id="fff30-117">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fff30-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="fff30-118">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="fff30-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="fff30-119">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="fff30-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="fff30-120">VB</span><span class="sxs-lookup"><span data-stu-id="fff30-120">VB</span></span>

<span data-ttu-id="fff30-121">Stringa che rappresenta il nome del certificato di firma.</span><span class="sxs-lookup"><span data-stu-id="fff30-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="fff30-122">Il certificato di firma verrà usato per firmare la [*richiesta di certificato*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fff30-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fff30-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fff30-123">Remarks</span></span>

<span data-ttu-id="fff30-124">Il metodo **getSigningCertificateName** restituisce il nome del soggetto del certificato selezionato dall'utente (o da un altro amministratore) in una chiamata precedente riuscita a [**ISCrdEnr:: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) o [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="fff30-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="fff30-125">Questo metodo chiama la funzione [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per recuperare il nome del soggetto in base alla sequenza descritta per il \_ nome del certificato \_ \_ \_ del tipo di visualizzazione semplice valore del parametro *dwType* di **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="fff30-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff30-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fff30-126">Requirements</span></span>



| <span data-ttu-id="fff30-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff30-127">Requirement</span></span> | <span data-ttu-id="fff30-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fff30-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fff30-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fff30-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fff30-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fff30-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fff30-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fff30-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fff30-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fff30-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fff30-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fff30-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff30-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff30-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="fff30-135">IID</span><span class="sxs-lookup"><span data-stu-id="fff30-135">IID</span></span><br/>                      | <span data-ttu-id="fff30-136">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="fff30-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fff30-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fff30-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff30-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="fff30-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="fff30-139">**ISCrdEnr::selectSigningCertificate**</span><span class="sxs-lookup"><span data-stu-id="fff30-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
