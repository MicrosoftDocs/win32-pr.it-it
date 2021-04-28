---
description: "Metodo ProtectKeyWithCertificateFile della classe Win32_EncryptableVolume : convalida l'identificatore di oggetto EKU (Enhanced Key Usage) del certificato fornito."
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Metodo ProtectKeyWithCertificateFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110565"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1052a-103">Metodo ProtectKeyWithCertificateFile della classe \_ EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="1052a-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1052a-104">Il **metodo ProtectKeyWithCertificateFile** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) convalida l'identificatore di oggetto EKU [*(Enhanced*](../secgloss/o-gly.md) Key Usage) del certificato fornito.</span><span class="sxs-lookup"><span data-stu-id="1052a-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="1052a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1052a-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="1052a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1052a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1052a-107">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="1052a-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1052a-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="1052a-108">Type: **string**</span></span>

<span data-ttu-id="1052a-109">Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione della chiave.</span><span class="sxs-lookup"><span data-stu-id="1052a-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="1052a-110">Se questo parametro non viene specificato, il *parametro FriendlyName* viene creato usando il nome soggetto nel certificato.</span><span class="sxs-lookup"><span data-stu-id="1052a-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="1052a-111">*FileName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1052a-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1052a-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="1052a-112">Type: **string**</span></span>

<span data-ttu-id="1052a-113">Stringa che specifica il percorso e il nome del file cer usato per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1052a-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="1052a-114">Un certificato di crittografia deve essere esportato in formato con estensione [*cer (Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) binario con codifica [*X.509*](../secgloss/x-gly.md) o Con codifica Base 64 X.509.</span><span class="sxs-lookup"><span data-stu-id="1052a-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="1052a-115">Il certificato di crittografia può essere generato da Microsoft PKI, PKI di terze parti o autofirmato.</span><span class="sxs-lookup"><span data-stu-id="1052a-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="1052a-116">*VolumeKeyProtectorID* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1052a-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1052a-117">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="1052a-117">Type: **string**</span></span>

<span data-ttu-id="1052a-118">Stringa che identifica in modo univoco la protezione della chiave creata che può essere usata per gestire la protezione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="1052a-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="1052a-119">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione della chiave viene scritta in per ogni metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="1052a-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1052a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1052a-120">Return value</span></span>

<span data-ttu-id="1052a-121">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="1052a-121">Type: **uint32**</span></span>

<span data-ttu-id="1052a-122">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.</span><span class="sxs-lookup"><span data-stu-id="1052a-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1052a-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="1052a-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="1052a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1052a-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1052a-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="1052a-126">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="1052a-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1052a-127"><dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="1052a-128">L'attributo EKU del certificato specificato non ne consente l'uso per Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1052a-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="1052a-129">BitLocker non richiede che un certificato abbia un attributo EKU, ma se ne è configurato uno, deve essere impostato su un OID corrispondente all'OID configurato per BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1052a-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="1052a-130"><dt>**FVE \_ E \_ CERTIFICATO UTENTE CRITERI NON \_ \_ \_ \_ CONSENTITO**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="1052a-131">Criteri di gruppo non consente l'uso di certificati utente, ad esempio smart card, con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1052a-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1052a-132"><dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUST BE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="1052a-133">Criteri di gruppo necessario specificare un nome smart card utilizzare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1052a-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="1052a-134"><dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="1052a-135">Criteri di gruppo non consente l'uso di certificati autofirmati.</span><span class="sxs-lookup"><span data-stu-id="1052a-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1052a-136"><dt>**ERRORE \_ FILE \_ NON \_ TROVATO**</dt> <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="1052a-137">Impossibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="1052a-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="1052a-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="1052a-138">Remarks</span></span>

<span data-ttu-id="1052a-139">Se l'OID non corrisponde a quello associato al controller del servizio nel Registro di sistema, questo metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1052a-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="1052a-140">In questo modo si impedisce all'utente di impostare manualmente le protezione dell'agente di recupero dati (DRA) nel volume.</span><span class="sxs-lookup"><span data-stu-id="1052a-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="1052a-141">I dra devono essere impostati solo dal servizio.</span><span class="sxs-lookup"><span data-stu-id="1052a-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="1052a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1052a-142">Requirements</span></span>



| <span data-ttu-id="1052a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1052a-143">Requirement</span></span> | <span data-ttu-id="1052a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="1052a-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1052a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1052a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1052a-146">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="1052a-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1052a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1052a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1052a-148">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1052a-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1052a-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1052a-149">Namespace</span></span><br/>                | <span data-ttu-id="1052a-150">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1052a-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1052a-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1052a-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1052a-152"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1052a-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1052a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1052a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1052a-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1052a-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
