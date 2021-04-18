---
description: Crea una firma digitale sul contenuto da firmare. Una firma digitale è costituita da un hash del contenuto da firmare crittografato tramite la chiave privata del firmatario.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Metodo SignedData. Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325150"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="97abc-104">Metodo SignedData. Sign</span><span class="sxs-lookup"><span data-stu-id="97abc-104">SignedData.Sign method</span></span>

<span data-ttu-id="97abc-105">\[Il metodo **Sign** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="97abc-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97abc-106">Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="97abc-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="97abc-107">Il metodo **Sign** crea una [*firma digitale*](../secgloss/d-gly.md) sul contenuto da firmare.</span><span class="sxs-lookup"><span data-stu-id="97abc-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="97abc-108">Una firma digitale è costituita da un [*hash*](../secgloss/h-gly.md) del contenuto da firmare crittografato tramite la chiave privata del firmatario.</span><span class="sxs-lookup"><span data-stu-id="97abc-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="97abc-109">Questo metodo può essere utilizzato solo dopo l'inizializzazione della proprietà [**SignedData. Content**](signeddata-content.md) .</span><span class="sxs-lookup"><span data-stu-id="97abc-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="97abc-110">Se il metodo **Sign** viene chiamato su un oggetto che dispone già di una firma, la firma precedente viene sostituita.</span><span class="sxs-lookup"><span data-stu-id="97abc-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="97abc-111">La firma viene creata utilizzando l'algoritmo di firma SHA1.</span><span class="sxs-lookup"><span data-stu-id="97abc-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="97abc-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97abc-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="97abc-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="97abc-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97abc-114">*Firmatario* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="97abc-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97abc-115">Riferimento all'oggetto [**firmatario**](signer.md) del firmatario dei dati.</span><span class="sxs-lookup"><span data-stu-id="97abc-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="97abc-116">L'oggetto **firmatario** deve avere accesso alla [*chiave privata*](../secgloss/p-gly.md) del [*certificato*](../secgloss/c-gly.md) usato per la firma.</span><span class="sxs-lookup"><span data-stu-id="97abc-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="97abc-117">Questo parametro può essere **null**. Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="97abc-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="97abc-118">*bDetached* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="97abc-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97abc-119">Se **true**, i dati da firmare sono scollegati. ovvero, il contenuto firmato non è incluso come parte dell'oggetto firmato.</span><span class="sxs-lookup"><span data-stu-id="97abc-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="97abc-120">Per verificare la firma sul contenuto scollegato, un'applicazione deve disporre di una copia del contenuto originale.</span><span class="sxs-lookup"><span data-stu-id="97abc-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="97abc-121">Il contenuto scollegato viene spesso utilizzato per ridurre le dimensioni di un oggetto firmato da inviare sul Web, se il destinatario del messaggio firmato dispone di una copia originale dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="97abc-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="97abc-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="97abc-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="97abc-123">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="97abc-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97abc-124">Valore dell'enumerazione del [ \_ \_ tipo di codifica CAPICOM](capicom-encoding-type.md) che indica la modalità di codifica dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="97abc-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="97abc-125">Il valore predefinito è CAPICOM \_ Encode \_ base64.</span><span class="sxs-lookup"><span data-stu-id="97abc-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="97abc-126">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="97abc-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="97abc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="97abc-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="97abc-128">Significato</span><span class="sxs-lookup"><span data-stu-id="97abc-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="97abc-129"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="97abc-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="97abc-130">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="97abc-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="97abc-131">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="97abc-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="97abc-132">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="97abc-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="97abc-133"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97abc-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="97abc-134">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="97abc-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="97abc-135"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="97abc-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="97abc-136">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="97abc-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97abc-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97abc-137">Return value</span></span>

<span data-ttu-id="97abc-138">Questo metodo restituisce una stringa che contiene i dati firmati codificati.</span><span class="sxs-lookup"><span data-stu-id="97abc-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="97abc-139">Se questo metodo ha esito negativo, verrà generato un errore.</span><span class="sxs-lookup"><span data-stu-id="97abc-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="97abc-140">L'oggetto **Err** conterrà informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="97abc-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="97abc-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="97abc-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97abc-142">Quando questo metodo viene chiamato da uno script Web, lo script deve usare la chiave privata per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="97abc-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="97abc-143">Consentire ai siti Web non attendibili di usare la chiave privata costituisce un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="97abc-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="97abc-144">Una finestra di dialogo in cui viene chiesto se il sito Web può utilizzare la chiave privata viene visualizzata quando questo metodo viene chiamato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="97abc-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="97abc-145">Se si consente allo script di usare la chiave privata per creare una firma digitale e selezionare "non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per alcuno script all'interno del dominio che usa la chiave privata per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="97abc-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="97abc-146">Tuttavia, gli script all'esterno del dominio che tentano di usare la chiave privata per creare una firma digitale comporteranno comunque la visualizzazione di questa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="97abc-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="97abc-147">Se non si consente allo script di utilizzare la chiave privata e selezionare "non visualizzare più questa finestra di dialogo", gli script all'interno di tale dominio verranno automaticamente rifiutati di utilizzare la chiave privata per creare firme digitali.</span><span class="sxs-lookup"><span data-stu-id="97abc-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="97abc-148">Poiché la creazione di una [*firma digitale*](../secgloss/d-gly.md) richiede l'uso di una [*chiave privata*](../secgloss/p-gly.md), le applicazioni basate sul Web che tentano di usare questo metodo richiederanno richieste di interfaccia utente che consentono all'utente di approvare l'uso della chiave privata, per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="97abc-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="97abc-149">I risultati seguenti si applicano al valore del parametro del *firmatario* :</span><span class="sxs-lookup"><span data-stu-id="97abc-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="97abc-150">Se il parametro del *firmatario* non è **null**, questo metodo usa la chiave privata a cui fa riferimento il certificato associato per crittografare la firma.</span><span class="sxs-lookup"><span data-stu-id="97abc-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="97abc-151">Se la chiave privata a cui fa riferimento il certificato non è disponibile, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97abc-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="97abc-152">Se il parametro del *firmatario* è **null** ed è presente esattamente un certificato nell' \_ archivio My dell'utente corrente che ha accesso a una chiave privata, il certificato viene usato per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="97abc-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="97abc-153">Se il parametro del *firmatario* è **null**, il valore della proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed esiste più di un certificato nell' \_ archivio My dell'utente corrente con una chiave privata disponibile, viene visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato usato.</span><span class="sxs-lookup"><span data-stu-id="97abc-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="97abc-154">Se il parametro del *firmatario* è **null** e la proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97abc-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="97abc-155">Se il parametro del *firmatario* è **null** e non è presente alcun certificato nell' \_ utente corrente My Store con una chiave privata disponibile, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97abc-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="97abc-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97abc-156">Requirements</span></span>



| <span data-ttu-id="97abc-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="97abc-157">Requirement</span></span> | <span data-ttu-id="97abc-158">Valore</span><span class="sxs-lookup"><span data-stu-id="97abc-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97abc-159">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="97abc-159">Redistributable</span></span><br/> | <span data-ttu-id="97abc-160">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="97abc-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="97abc-161">DLL</span><span class="sxs-lookup"><span data-stu-id="97abc-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="97abc-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97abc-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97abc-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97abc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97abc-164">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="97abc-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="97abc-165">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="97abc-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
