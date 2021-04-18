---
description: Crea una firma digitale Authenticode e firma il file eseguibile specificato nella proprietà SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Metodo SignedCode. Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331267"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="972ad-103">Metodo SignedCode. Sign</span><span class="sxs-lookup"><span data-stu-id="972ad-103">SignedCode.Sign method</span></span>

<span data-ttu-id="972ad-104">\[Il metodo **Sign** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="972ad-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="972ad-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="972ad-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="972ad-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="972ad-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="972ad-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="972ad-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="972ad-108">Il metodo **Sign** crea una firma digitale Authenticode e firma il file eseguibile specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="972ad-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="972ad-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="972ad-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="972ad-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="972ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="972ad-111">*Firmatario* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="972ad-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="972ad-112">Oggetto [**firmatario**](signer.md) che ha accesso alla chiave privata del certificato utilizzato per firmare il codice.</span><span class="sxs-lookup"><span data-stu-id="972ad-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="972ad-113">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="972ad-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="972ad-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="972ad-114">Return value</span></span>

<span data-ttu-id="972ad-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="972ad-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="972ad-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="972ad-116">Remarks</span></span>

<span data-ttu-id="972ad-117">Prima che venga chiamato il metodo **Sign** , il file che contiene il codice deve essere specificato nella proprietà [**filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="972ad-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="972ad-118">Se il file eseguibile è già firmato, questo metodo sovrascrive la firma esistente.</span><span class="sxs-lookup"><span data-stu-id="972ad-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="972ad-119">I risultati seguenti si applicano al valore del parametro del *firmatario* :</span><span class="sxs-lookup"><span data-stu-id="972ad-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="972ad-120">Se il parametro del *firmatario* non è **null**, questo metodo usa la chiave privata a cui fa riferimento il certificato associato per crittografare la firma.</span><span class="sxs-lookup"><span data-stu-id="972ad-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="972ad-121">Se la chiave privata a cui fa riferimento il certificato non è disponibile, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="972ad-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="972ad-122">Se il parametro del *firmatario* è **null** ed è presente esattamente un certificato nell' \_ archivio My Store che ha accesso a una chiave privata con funzionalità di firma del codice, il certificato viene usato per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="972ad-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="972ad-123">Se il parametro del *firmatario* è **null**, il valore della proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed esiste più di un certificato nell' \_ archivio My dell'utente corrente con una chiave privata disponibile con funzionalità di firma del codice, viene visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato usato.</span><span class="sxs-lookup"><span data-stu-id="972ad-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="972ad-124">Se il parametro del *firmatario* è **null** e la proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="972ad-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="972ad-125">Se il parametro del *firmatario* è **null** e non sono presenti certificati nell' \_ utente corrente My Store con una chiave privata disponibile con funzionalità di firma del codice, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="972ad-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="972ad-126">Questo metodo usa l'algoritmo di hash SHA-1.</span><span class="sxs-lookup"><span data-stu-id="972ad-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="972ad-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="972ad-127">Requirements</span></span>



| <span data-ttu-id="972ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="972ad-128">Requirement</span></span> | <span data-ttu-id="972ad-129">Valore</span><span class="sxs-lookup"><span data-stu-id="972ad-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="972ad-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="972ad-130">Redistributable</span></span><br/> | <span data-ttu-id="972ad-131">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="972ad-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="972ad-132">DLL</span><span class="sxs-lookup"><span data-stu-id="972ad-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="972ad-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972ad-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
