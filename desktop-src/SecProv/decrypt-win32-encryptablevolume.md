---
description: Inizia la decrittografia di un volume completamente crittografato oppure riprende la decrittografia di un volume parzialmente crittografato.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Metodo Decrypt della classe Win32_EncryptableVolume (infocard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882081"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3e434-103">Metodo Decrypt della \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="3e434-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3e434-104">Il metodo **Decrypt** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inizia la decrittografia di un volume completamente crittografato oppure riprende la decrittografia di un volume parzialmente crittografato.</span><span class="sxs-lookup"><span data-stu-id="3e434-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="3e434-105">Quando la decrittografia viene sospesa o in corso, il comportamento di questo metodo è uguale a quello di [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="3e434-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="3e434-106">Quando la crittografia viene sospesa o in corso, questo metodo ripristina la crittografia e inizia la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="3e434-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="3e434-107">Al termine della decrittografia, tutte le protezioni con chiave presenti in questo volume vengono rimosse dal sistema e il volume viene convertito in un file system NTFS standard.</span><span class="sxs-lookup"><span data-stu-id="3e434-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="3e434-108">Se il disco è crittografato con hardware, il metodo **Decrypt** imposta lo stato della banda su "always Unlocked", rimuove tutti i metadati associati e azzera l'ID di sicurezza per l'unità.</span><span class="sxs-lookup"><span data-stu-id="3e434-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3e434-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e434-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="3e434-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e434-110">Parameters</span></span>

<span data-ttu-id="3e434-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3e434-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e434-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e434-112">Return value</span></span>

<span data-ttu-id="3e434-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e434-113">Type: **uint32**</span></span>

<span data-ttu-id="3e434-114">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3e434-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="3e434-115">Questo metodo restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="3e434-115">This method returns immediately.</span></span> <span data-ttu-id="3e434-116">Se il volume è già completamente decrittografato e non esistono altri errori, questo metodo restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="3e434-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="3e434-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e434-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="3e434-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e434-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e434-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3e434-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="3e434-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3e434-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="3e434-121"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3e434-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="3e434-122">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3e434-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="3e434-123"><dt>**FVE \_ \_Sblocco automatico \_ abilitato**</dt> <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="3e434-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="3e434-124">Non è possibile decrittografare questo volume perché sono disponibili le chiavi usate per sbloccare automaticamente i volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="3e434-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="3e434-125">Usare [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) per rimuovere queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="3e434-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="3e434-126">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="3e434-126">Security Considerations</span></span>

<span data-ttu-id="3e434-127">La chiamata al metodo **Decrypt** lascia i dati non protetti.</span><span class="sxs-lookup"><span data-stu-id="3e434-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="3e434-128">Se lo stato di protezione del volume è 1 (PROTECTION ON) prima che questo metodo venga usato, il completamento di questo metodo modifica lo stato di protezione in 0 (PROTECTION OFF), poiché per definizione un volume parzialmente crittografato non è protetto.</span><span class="sxs-lookup"><span data-stu-id="3e434-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e434-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e434-129">Remarks</span></span>

<span data-ttu-id="3e434-130">Se il volume non è già completamente decrittografato, l'esecuzione di **decrittografia** fa sì che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che la decrittografia è in corso e Mostra la percentuale del volume che rimane crittografato.</span><span class="sxs-lookup"><span data-stu-id="3e434-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="3e434-131">Se lo stato di protezione del volume è "on" prima dell'esecuzione di questo metodo, l'esecuzione di questo metodo imposta lo stato di protezione su "off", poiché per definizione un volume parzialmente crittografato non è protetto.</span><span class="sxs-lookup"><span data-stu-id="3e434-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="3e434-132">Se questo metodo viene eseguito nel volume del sistema operativo attualmente in esecuzione e questo volume del sistema operativo viene usato per sbloccare automaticamente i volumi di dati (vedere il metodo [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), è necessario chiamare prima il metodo [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="3e434-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="3e434-133">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3e434-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3e434-134">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3e434-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3e434-135">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3e434-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3e434-136">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3e434-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e434-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e434-137">Requirements</span></span>



| <span data-ttu-id="3e434-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e434-138">Requirement</span></span> | <span data-ttu-id="3e434-139">Valore</span><span class="sxs-lookup"><span data-stu-id="3e434-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e434-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e434-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3e434-141">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="3e434-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3e434-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e434-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3e434-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e434-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e434-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e434-144">Namespace</span></span><br/>                | <span data-ttu-id="3e434-145">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="3e434-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3e434-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e434-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e434-147"><dt>Infocard. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e434-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="3e434-148">MOF</span><span class="sxs-lookup"><span data-stu-id="3e434-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e434-149"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e434-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e434-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e434-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e434-151">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="3e434-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
