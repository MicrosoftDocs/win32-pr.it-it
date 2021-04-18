---
description: Determina se le firme sui dati firmati nell'oggetto SignedData sono valide.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Metodo SignedData. Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325147"
---
# <a name="signeddataverify-method"></a><span data-ttu-id="da662-103">Metodo SignedData. Verify</span><span class="sxs-lookup"><span data-stu-id="da662-103">SignedData.Verify method</span></span>

<span data-ttu-id="da662-104">\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="da662-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="da662-105">Usare invece la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="da662-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="da662-106">Il metodo **Verify** determina se le [*firme*](../secgloss/d-gly.md) sui dati firmati nell'oggetto [**SignedData**](signeddata.md) sono valide.</span><span class="sxs-lookup"><span data-stu-id="da662-106">The **Verify** method determines whether the [*signatures*](../secgloss/d-gly.md) on signed data in the [**SignedData**](signeddata.md) object are valid.</span></span> <span data-ttu-id="da662-107">Per verificare una firma, l' [*hash*](../secgloss/h-gly.md) crittografato del contenuto viene decrittografato usando la chiave pubblica del firmatario dal certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="da662-107">To verify a signature, the encrypted [*hash*](../secgloss/h-gly.md) of the contents is decrypted by using the signer's public key from the signer's certificate.</span></span> <span data-ttu-id="da662-108">L'hash decrittografato viene confrontato con un nuovo hash del contenuto dei dati.</span><span class="sxs-lookup"><span data-stu-id="da662-108">The decrypted hash is compared to a new hash of the data content.</span></span> <span data-ttu-id="da662-109">Una firma è valida se gli hash corrispondono.</span><span class="sxs-lookup"><span data-stu-id="da662-109">A signature is valid if the hashes match.</span></span> <span data-ttu-id="da662-110">Inoltre, questo metodo compila una catena di certificati per determinare la validità del certificato che fornisce la [*chiave pubblica*](../secgloss/p-gly.md) utilizzata per decrittografare l'hash.</span><span class="sxs-lookup"><span data-stu-id="da662-110">In addition, this method also builds a certificate chain to determine the validity of the certificate that provides the [*public key*](../secgloss/p-gly.md) used to decrypt the hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="da662-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da662-111">Syntax</span></span>


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="da662-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="da662-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da662-113">*SignedMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da662-113">*SignedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da662-114">Stringa che contiene il messaggio firmato da verificare.</span><span class="sxs-lookup"><span data-stu-id="da662-114">A string that contains the signed message to be verified.</span></span>

</dd> <dt>

<span data-ttu-id="da662-115">*bDetached* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="da662-115">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da662-116">Se **true**, i dati da firmare sono scollegati. ovvero, il contenuto firmato non è incluso come parte dell'oggetto firmato.</span><span class="sxs-lookup"><span data-stu-id="da662-116">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="da662-117">Per verificare la firma sul contenuto scollegato, un'applicazione deve disporre di una copia del contenuto originale.</span><span class="sxs-lookup"><span data-stu-id="da662-117">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="da662-118">Il contenuto scollegato viene spesso utilizzato per ridurre le dimensioni di un oggetto firmato da inviare sul Web, se il destinatario del messaggio firmato dispone di una copia originale dei dati firmati.</span><span class="sxs-lookup"><span data-stu-id="da662-118">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="da662-119">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="da662-119">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="da662-120">*VerifyFlag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="da662-120">*VerifyFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da662-121">Valore dell'enumerazione del [ \_ \_ \_ \_ flag di verifica dei dati con firma CAPICOM](capicom-signed-data-verify-flag.md) che indica i criteri di verifica.</span><span class="sxs-lookup"><span data-stu-id="da662-121">A value of the [CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG](capicom-signed-data-verify-flag.md) enumeration that indicates the verification policy.</span></span> <span data-ttu-id="da662-122">Il valore predefinito è CAPICOM verificare la \_ \_ firma \_ e il \_ certificato.</span><span class="sxs-lookup"><span data-stu-id="da662-122">The default value is CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE.</span></span> <span data-ttu-id="da662-123">Utilizzando questo valore, vengono controllati sia la validità del certificato che la validità della firma.</span><span class="sxs-lookup"><span data-stu-id="da662-123">Using this value, both the validity of the certificate and the validity of the signature are checked.</span></span> <span data-ttu-id="da662-124">Questo parametro può essere impostato per verificare la firma e non il certificato.</span><span class="sxs-lookup"><span data-stu-id="da662-124">This parameter may be set to verify the signature and not the certificate.</span></span> <span data-ttu-id="da662-125">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="da662-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="da662-126">Valore</span><span class="sxs-lookup"><span data-stu-id="da662-126">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="da662-127">Significato</span><span class="sxs-lookup"><span data-stu-id="da662-127">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <span data-ttu-id="da662-128"><dt>**CAPICOM \_ verificare solo la \_ firma \_**</dt></span><span class="sxs-lookup"><span data-stu-id="da662-128"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</dt></span></span> </dl>                                   | <span data-ttu-id="da662-129">Viene controllata solo la firma.</span><span class="sxs-lookup"><span data-stu-id="da662-129">Only the signature is checked.</span></span><br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <span data-ttu-id="da662-130"><dt>**\_verificare la \_ firma e il \_ \_ certificato di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="da662-130"><dt>**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</dt></span></span> </dl> | <span data-ttu-id="da662-131">Vengono controllati sia la firma che la validità del certificato utilizzato per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="da662-131">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da662-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da662-132">Return value</span></span>

<span data-ttu-id="da662-133">Questo metodo restituisce una stringa che contiene i dati firmati codificati.</span><span class="sxs-lookup"><span data-stu-id="da662-133">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="da662-134">Se questo metodo ha esito negativo, verrà generato un errore.</span><span class="sxs-lookup"><span data-stu-id="da662-134">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="da662-135">L'oggetto **Err** conterrà informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="da662-135">The **Err** object will contain additional information about the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="da662-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da662-136">Requirements</span></span>



| <span data-ttu-id="da662-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="da662-137">Requirement</span></span> | <span data-ttu-id="da662-138">Valore</span><span class="sxs-lookup"><span data-stu-id="da662-138">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da662-139">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="da662-139">Redistributable</span></span><br/> | <span data-ttu-id="da662-140">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="da662-140">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="da662-141">DLL</span><span class="sxs-lookup"><span data-stu-id="da662-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="da662-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da662-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da662-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da662-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da662-144">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="da662-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="da662-145">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="da662-145">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
