---
description: Recupera la chiave pubblica e l'identificazione personale del certificato per una protezione con chiave pubblica.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Metodo GetKeyProtectorCertificate della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316107"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b5338-103">Metodo GetKeyProtectorCertificate della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b5338-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b5338-104">Il metodo **GetKeyProtectorCertificate** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera la [*chiave pubblica*](../secgloss/p-gly.md) e l'identificazione personale del [*certificato*](../secgloss/c-gly.md) per una protezione con chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="b5338-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5338-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5338-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="b5338-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5338-107">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5338-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5338-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="b5338-108">Type: **string**</span></span>

<span data-ttu-id="b5338-109">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="b5338-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="b5338-110">*PublicKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5338-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5338-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b5338-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="b5338-112">Matrice di byte che specifica la chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="b5338-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="b5338-113">*CertThumbprint* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5338-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5338-114">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="b5338-114">Type: **string**</span></span>

<span data-ttu-id="b5338-115">Stringa che specifica l'identificazione digitale del certificato.</span><span class="sxs-lookup"><span data-stu-id="b5338-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="b5338-116">*Tipo certificato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5338-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5338-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5338-117">Type: **uint32**</span></span>

<span data-ttu-id="b5338-118">Unsigned Integer che specifica il tipo della protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="b5338-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="b5338-119">Questo valore integer viene utilizzato per distinguere tra l'agente recupero dati (DRA) e i certificati utente.</span><span class="sxs-lookup"><span data-stu-id="b5338-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="b5338-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b5338-120">Value</span></span>                                                                        | <span data-ttu-id="b5338-121">Significato</span><span class="sxs-lookup"><span data-stu-id="b5338-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="b5338-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b5338-123">Il certificato è un DRA.</span><span class="sxs-lookup"><span data-stu-id="b5338-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="b5338-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b5338-125">Il certificato non è un DRA.</span><span class="sxs-lookup"><span data-stu-id="b5338-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5338-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5338-126">Return value</span></span>

<span data-ttu-id="b5338-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5338-127">Type: **uint32**</span></span>

<span data-ttu-id="b5338-128">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b5338-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b5338-129">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5338-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="b5338-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5338-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5338-131"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="b5338-132">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b5338-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="b5338-133"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="b5338-134">La protezione con chiave specificata non è una protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="b5338-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="b5338-135">È necessario immettere un'altra protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="b5338-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="b5338-136"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="b5338-137">Questa unità è bloccata da Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b5338-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="b5338-138">È necessario sbloccare questo volume dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="b5338-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="b5338-139"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="b5338-140">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b5338-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b5338-141">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b5338-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="b5338-142"><dt>**FVE \_ \_Certificato utente del criterio E \_ \_ \_ obbligatorio**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="b5338-143">Criteri di gruppo richiede l'utilizzo di un certificato utente, ad esempio una smart card.</span><span class="sxs-lookup"><span data-stu-id="b5338-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="b5338-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5338-144">Remarks</span></span>

<span data-ttu-id="b5338-145">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b5338-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b5338-146">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b5338-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b5338-147">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b5338-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b5338-148">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b5338-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5338-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5338-149">Requirements</span></span>



| <span data-ttu-id="b5338-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5338-150">Requirement</span></span> | <span data-ttu-id="b5338-151">Valore</span><span class="sxs-lookup"><span data-stu-id="b5338-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5338-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5338-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b5338-153">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="b5338-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5338-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5338-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b5338-155">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5338-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5338-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5338-156">Namespace</span></span><br/>                | <span data-ttu-id="b5338-157">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b5338-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b5338-158">MOF</span><span class="sxs-lookup"><span data-stu-id="b5338-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5338-159"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5338-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5338-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5338-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5338-161">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b5338-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
