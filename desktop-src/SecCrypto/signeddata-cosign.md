---
description: Crea una firma digitale per il contenuto precedentemente firmato.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Metodo SignedData. cosign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332824"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="39e1d-103">Metodo SignedData. cosign</span><span class="sxs-lookup"><span data-stu-id="39e1d-103">SignedData.CoSign method</span></span>

<span data-ttu-id="39e1d-104">\[Il metodo **cosign** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="39e1d-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="39e1d-105">Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="39e1d-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="39e1d-106">Il metodo **cosign** crea una [*firma digitale*](../secgloss/d-gly.md) per il contenuto precedentemente firmato.</span><span class="sxs-lookup"><span data-stu-id="39e1d-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39e1d-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="39e1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="39e1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e1d-109">*Firmatario* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="39e1d-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e1d-110">Riferimento all'oggetto [**firmatario**](signer.md) del firmatario dei dati.</span><span class="sxs-lookup"><span data-stu-id="39e1d-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="39e1d-111">L'oggetto **firmatario** deve avere accesso alla chiave privata del certificato usato per la firma.</span><span class="sxs-lookup"><span data-stu-id="39e1d-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="39e1d-112">Questo parametro può essere **null**. Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="39e1d-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="39e1d-113">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="39e1d-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39e1d-114">Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica la modalità di codifica dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="39e1d-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="39e1d-115">Il valore predefinito è CAPICOM \_ Encode \_ base64.</span><span class="sxs-lookup"><span data-stu-id="39e1d-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="39e1d-116">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="39e1d-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="39e1d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="39e1d-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="39e1d-118">Significato</span><span class="sxs-lookup"><span data-stu-id="39e1d-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="39e1d-119"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="39e1d-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="39e1d-120">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="39e1d-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="39e1d-121">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="39e1d-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="39e1d-122">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="39e1d-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="39e1d-123"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39e1d-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="39e1d-124">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="39e1d-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="39e1d-125"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="39e1d-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="39e1d-126">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="39e1d-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e1d-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39e1d-127">Return value</span></span>

<span data-ttu-id="39e1d-128">Questo metodo restituisce una stringa che contiene i dati firmati codificati.</span><span class="sxs-lookup"><span data-stu-id="39e1d-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="39e1d-129">Se questo metodo ha esito negativo, verrà generato un errore.</span><span class="sxs-lookup"><span data-stu-id="39e1d-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="39e1d-130">L'oggetto **Err** conterrà informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="39e1d-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e1d-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="39e1d-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39e1d-132">Quando questo metodo viene chiamato da uno script Web, lo script deve usare la [*chiave privata*](../secgloss/p-gly.md) per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="39e1d-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="39e1d-133">Consentire ai siti Web non attendibili di usare la chiave privata costituisce un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="39e1d-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="39e1d-134">Una finestra di dialogo in cui viene chiesto se il sito Web può utilizzare la chiave privata viene visualizzata quando questo metodo viene chiamato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="39e1d-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="39e1d-135">Se si consente allo script di usare la chiave privata per creare una firma digitale e selezionare "non visualizzare più questa finestra di dialogo", la finestra di dialogo non verrà più visualizzata per alcuno script all'interno del dominio che usa la chiave privata per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="39e1d-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="39e1d-136">Tuttavia, gli script all'esterno del dominio che tentano di usare la chiave privata per creare una firma digitale comporteranno comunque la visualizzazione di questa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="39e1d-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="39e1d-137">Se non si consente allo script di utilizzare la chiave privata e selezionare "non visualizzare più questa finestra di dialogo", gli script all'interno di tale dominio verranno automaticamente rifiutati di utilizzare la chiave privata per creare firme digitali.</span><span class="sxs-lookup"><span data-stu-id="39e1d-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="39e1d-138">Non è garantito che i cofirmatari siano in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="39e1d-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="39e1d-139">I risultati seguenti si applicano al valore del parametro del *firmatario* :</span><span class="sxs-lookup"><span data-stu-id="39e1d-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="39e1d-140">Se il parametro del *firmatario* non è **null**, questo metodo usa la chiave privata a cui fa riferimento il certificato associato per crittografare la cofirma.</span><span class="sxs-lookup"><span data-stu-id="39e1d-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="39e1d-141">Se la chiave privata a cui fa riferimento il certificato non è disponibile, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="39e1d-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="39e1d-142">Se il parametro del *firmatario* è **null** ed è presente esattamente un certificato nell' \_ archivio My dell'utente corrente che ha accesso a una chiave privata, il certificato viene usato per creare la cofirma.</span><span class="sxs-lookup"><span data-stu-id="39e1d-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="39e1d-143">Se il parametro del *firmatario* è **null**, il valore della proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed esiste più di un certificato nell' \_ archivio My dell'utente corrente con una chiave privata disponibile, viene visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato usato.</span><span class="sxs-lookup"><span data-stu-id="39e1d-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="39e1d-144">Se il parametro del *firmatario* è **null** e la proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="39e1d-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="39e1d-145">Se il parametro del *firmatario* è **null** e non è presente alcun certificato nell' \_ utente corrente My Store con una chiave privata disponibile, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="39e1d-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e1d-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39e1d-146">Requirements</span></span>



| <span data-ttu-id="39e1d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e1d-147">Requirement</span></span> | <span data-ttu-id="39e1d-148">Valore</span><span class="sxs-lookup"><span data-stu-id="39e1d-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e1d-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="39e1d-149">Redistributable</span></span><br/> | <span data-ttu-id="39e1d-150">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="39e1d-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="39e1d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="39e1d-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="39e1d-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e1d-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e1d-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39e1d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e1d-154">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="39e1d-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="39e1d-155">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="39e1d-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
