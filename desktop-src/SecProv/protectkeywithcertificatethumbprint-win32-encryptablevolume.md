---
description: "Metodo ProtectKeyWithCertificateThumbprint della classe Win32_EncryptableVolume: convalida l'identificatore di oggetto (OID) di utilizzo chiavi avanzato (EKU) del certificato fornito."
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Metodo ProtectKeyWithCertificateThumbprint della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110579"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="42789-103">Metodo ProtectKeyWithCertificateThumbprint della classe \_ EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="42789-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="42789-104">Il **metodo ProtectKeyWithCertificateThumbprint** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) convalida l'identificatore di oggetto (OID) [](../secgloss/o-gly.md) di Utilizzo chiavi avanzato (EKU) del certificato fornito.</span><span class="sxs-lookup"><span data-stu-id="42789-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="42789-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42789-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="42789-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42789-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42789-107">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="42789-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42789-108">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="42789-108">Type: **string**</span></span>

<span data-ttu-id="42789-109">Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="42789-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="42789-110">Se questo parametro non viene specificato, il *parametro FriendlyName* viene creato usando il nome soggetto nel certificato.</span><span class="sxs-lookup"><span data-stu-id="42789-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="42789-111">*CertThumbprint* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="42789-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42789-112">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="42789-112">Type: **string**</span></span>

<span data-ttu-id="42789-113">Stringa che specifica l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="42789-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="42789-114">*VolumeKeyProtectorID* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="42789-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42789-115">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="42789-115">Type: **string**</span></span>

<span data-ttu-id="42789-116">Stringa che identifica in modo univoco la protezione con chiave creata che può essere usata per gestire la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="42789-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="42789-117">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione con chiave viene scritta per metadati di banda.</span><span class="sxs-lookup"><span data-stu-id="42789-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42789-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42789-118">Return value</span></span>

<span data-ttu-id="42789-119">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="42789-119">Type: **uint32**</span></span>

<span data-ttu-id="42789-120">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="42789-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="42789-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="42789-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="42789-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42789-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42789-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="42789-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="42789-124">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="42789-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="42789-125"><dt>**ERRORE \_ DATI \_ NON**</dt> <dt>VALIDI 13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="42789-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="42789-126">I dati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="42789-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="42789-127"><dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="42789-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="42789-128">L'attributo EKU del certificato specificato non ne consente l'uso per Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="42789-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="42789-129">BitLocker non richiede che un certificato abbia un attributo EKU, ma se ne è configurato uno, deve essere impostato su un OID corrispondente all'OID configurato per BitLocker.</span><span class="sxs-lookup"><span data-stu-id="42789-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="42789-130"><dt>**FVE \_ E \_ CERTIFICATO UTENTE CRITERI NON \_ \_ \_ \_ CONSENTITO**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="42789-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="42789-131">Criteri di gruppo non consente l'uso di certificati utente, ad esempio smart card, con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="42789-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="42789-132"><dt>**FVE \_ E \_ POLICY \_ USER \_ CERT DEVE ESSERE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="42789-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="42789-133">Criteri di gruppo è necessario specificare un smart card usare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="42789-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="42789-134"><dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="42789-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="42789-135">Criteri di gruppo non consente l'uso di certificati autofirmati.</span><span class="sxs-lookup"><span data-stu-id="42789-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="42789-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="42789-136">Remarks</span></span>

<span data-ttu-id="42789-137">Se l'OID non corrisponde a quello associato al controller del servizio nel Registro di sistema, questo metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="42789-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="42789-138">Ciò impedisce all'utente di impostare manualmente le protezione dell'agente di recupero dati (DRA) nel volume.</span><span class="sxs-lookup"><span data-stu-id="42789-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="42789-139">I contratti di ripristino di emergenza devono essere impostati solo dal servizio.</span><span class="sxs-lookup"><span data-stu-id="42789-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="42789-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42789-140">Requirements</span></span>



| <span data-ttu-id="42789-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="42789-141">Requirement</span></span> | <span data-ttu-id="42789-142">Valore</span><span class="sxs-lookup"><span data-stu-id="42789-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42789-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42789-143">Minimum supported client</span></span><br/> | <span data-ttu-id="42789-144">Solo app desktop di Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="42789-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42789-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42789-145">Minimum supported server</span></span><br/> | <span data-ttu-id="42789-146">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="42789-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="42789-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="42789-147">Namespace</span></span><br/>                | <span data-ttu-id="42789-148">Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="42789-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="42789-149">MOF</span><span class="sxs-lookup"><span data-stu-id="42789-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42789-150"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="42789-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42789-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42789-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42789-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="42789-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
