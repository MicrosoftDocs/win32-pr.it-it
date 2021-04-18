---
description: Indica l'algoritmo di crittografia e le dimensioni della chiave usati nel volume.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Metodo GetEncryptionMethod della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316118"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="52689-103">Metodo GetEncryptionMethod della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="52689-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="52689-104">Il metodo **GetEncryptionMethod** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica l'algoritmo di crittografia e le dimensioni della chiave usati nel volume.</span><span class="sxs-lookup"><span data-stu-id="52689-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="52689-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52689-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="52689-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52689-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52689-107">*EncryptionMethod* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52689-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52689-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52689-108">Type: **uint32**</span></span>

<span data-ttu-id="52689-109">Unsigned Integer che specifica l'algoritmo di crittografia e le dimensioni della chiave utilizzati nel volume.</span><span class="sxs-lookup"><span data-stu-id="52689-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="52689-110">Valore</span><span class="sxs-lookup"><span data-stu-id="52689-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="52689-111">Significato</span><span class="sxs-lookup"><span data-stu-id="52689-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="52689-112"><dt>**Nessuno**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52689-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="52689-113">Il volume non è crittografato.</span><span class="sxs-lookup"><span data-stu-id="52689-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="52689-114"><dt>**AES \_ 128 \_ con \_ diffusore**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="52689-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="52689-115">Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello di diffusione, usando una dimensione della chiave AES di 128 bit.</span><span class="sxs-lookup"><span data-stu-id="52689-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="52689-116">Questo metodo non è più disponibile nei dispositivi che eseguono Windows 8.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="52689-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="52689-117"><dt>**AES \_ 256 \_ con \_ diffusore**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="52689-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="52689-118">Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello di diffusione, usando una dimensione della chiave AES di 256 bit.</span><span class="sxs-lookup"><span data-stu-id="52689-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="52689-119">Questo metodo non è più disponibile nei dispositivi che eseguono Windows 8.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="52689-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="52689-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="52689-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="52689-121">Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES), usando una dimensione della chiave AES di 128 bit.</span><span class="sxs-lookup"><span data-stu-id="52689-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="52689-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="52689-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="52689-123">Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES), usando una dimensione della chiave AES di 256 bit.</span><span class="sxs-lookup"><span data-stu-id="52689-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="52689-124"><dt>**Hardware \_ CRITTOGRAFIA**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="52689-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="52689-125">Il volume è stato completamente o parzialmente crittografato utilizzando le funzionalità hardware dell'unità.</span><span class="sxs-lookup"><span data-stu-id="52689-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="52689-126"><dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="52689-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="52689-127">Il volume è stato completamente o parzialmente crittografato con XTS usando il Advanced Encryption Standard (AES) e una dimensione della chiave AES di 128 bit.</span><span class="sxs-lookup"><span data-stu-id="52689-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="52689-128">Questo metodo è disponibile solo nei dispositivi che eseguono Windows 10, versione 1511 o successiva.</span><span class="sxs-lookup"><span data-stu-id="52689-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="52689-129"><dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="52689-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="52689-130">Il volume è stato completamente o parzialmente crittografato con XTS usando il Advanced Encryption Standard (AES) e una dimensione della chiave AES di 256 bit.</span><span class="sxs-lookup"><span data-stu-id="52689-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="52689-131">Questo metodo è disponibile solo nei dispositivi che eseguono Windows 10, versione 1511 o successiva.</span><span class="sxs-lookup"><span data-stu-id="52689-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="52689-132"><dt>(UInt32) – 1</dt></span><span class="sxs-lookup"><span data-stu-id="52689-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="52689-133">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="52689-133">UNKNOWN</span></span><br/> <span data-ttu-id="52689-134">Il volume è stato completamente o parzialmente crittografato con un algoritmo sconosciuto e le dimensioni della chiave.</span><span class="sxs-lookup"><span data-stu-id="52689-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="52689-135">*SelfEncryptionDriveEncryptionMethod* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52689-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52689-136">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="52689-136">Type: **string**</span></span>

<span data-ttu-id="52689-137">L'algoritmo di crittografia viene configurato nell'unità di crittografia automatica.</span><span class="sxs-lookup"><span data-stu-id="52689-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="52689-138">Una stringa null indica che BitLocker utilizza la crittografia software o che non viene segnalato alcun metodo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="52689-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52689-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52689-139">Return value</span></span>

<span data-ttu-id="52689-140">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52689-140">Type: **uint32**</span></span>

<span data-ttu-id="52689-141">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="52689-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="52689-142">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="52689-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="52689-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52689-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="52689-144"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="52689-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="52689-145">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="52689-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52689-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="52689-146">Remarks</span></span>

<span data-ttu-id="52689-147">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52689-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52689-148">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="52689-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="52689-149">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="52689-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52689-150">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="52689-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52689-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52689-151">Requirements</span></span>



| <span data-ttu-id="52689-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="52689-152">Requirement</span></span> | <span data-ttu-id="52689-153">Valore</span><span class="sxs-lookup"><span data-stu-id="52689-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52689-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52689-154">Minimum supported client</span></span><br/> | <span data-ttu-id="52689-155">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="52689-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="52689-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52689-156">Minimum supported server</span></span><br/> | <span data-ttu-id="52689-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52689-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52689-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52689-158">Namespace</span></span><br/>                | <span data-ttu-id="52689-159">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="52689-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="52689-160">MOF</span><span class="sxs-lookup"><span data-stu-id="52689-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52689-161"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52689-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52689-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52689-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52689-163">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="52689-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
