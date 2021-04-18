---
description: Abilita o riprende tutte le protezioni con chiave disabilitate o sospese.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Metodo EnableKeyProtectors della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306405"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0141c-103">Metodo EnableKeyProtectors della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="0141c-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0141c-104">Il metodo **EnableKeyProtectors** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) Abilita o riprende tutte le protezioni con chiave disabilitate o sospese.</span><span class="sxs-lookup"><span data-stu-id="0141c-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="0141c-105">È possibile utilizzare questo metodo per riabilitare o riprendere la protezione BitLocker su un volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="0141c-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="0141c-106">Questo metodo garantisce che la chiave di crittografia del volume non venga esposta in chiaro sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="0141c-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="0141c-107">Se il disco supporta la crittografia hardware, lo stato della banda passa a "sbloccato" da "sempre sbloccato".</span><span class="sxs-lookup"><span data-stu-id="0141c-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0141c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0141c-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="0141c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0141c-109">Parameters</span></span>

<span data-ttu-id="0141c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0141c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0141c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0141c-111">Return value</span></span>

<span data-ttu-id="0141c-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0141c-112">Type: **uint32**</span></span>

<span data-ttu-id="0141c-113">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0141c-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="0141c-114">Se le protezioni con chiave sono già abilitate e non si verificano altri errori, questo metodo restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0141c-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0141c-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="0141c-115">Return code/value</span></span></th>
<th><span data-ttu-id="0141c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0141c-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="0141c-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="0141c-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="0141c-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="0141c-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="0141c-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span><span class="sxs-lookup"><span data-stu-id="0141c-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="0141c-120">Nel volume non esistono protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="0141c-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="0141c-121">Usare uno dei metodi seguenti per specificare le protezioni con chiave per il volume:</span><span class="sxs-lookup"><span data-stu-id="0141c-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="0141c-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="0141c-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="0141c-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="0141c-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="0141c-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="0141c-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="0141c-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="0141c-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="0141c-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="0141c-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="0141c-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span><span class="sxs-lookup"><span data-stu-id="0141c-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="0141c-132">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0141c-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="0141c-133">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0141c-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0141c-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="0141c-134">Remarks</span></span>

<span data-ttu-id="0141c-135">Se il volume è completamente crittografato, l'esecuzione di questo metodo garantisce che il volume sia protetto.</span><span class="sxs-lookup"><span data-stu-id="0141c-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="0141c-136">Se il volume è parzialmente crittografato, l'esecuzione di questo metodo implica che il volume verrà protetto quando diventerà completamente crittografato.</span><span class="sxs-lookup"><span data-stu-id="0141c-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="0141c-137">Per ulteriori informazioni, vedere il metodo [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="0141c-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="0141c-138">Se per il volume sono presenti protezioni con chiave basate su TPM, l'esecuzione di questo metodo consente inoltre di aggiornare tali protezioni in modo da convalidare il TPM rispetto ai servizi di avvio correnti della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="0141c-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="0141c-139">In altre parole, si dichiara che lo stato del computer corrente è lo stato corretto che verrà verificato dal TPM nei successivi riavvii del computer.</span><span class="sxs-lookup"><span data-stu-id="0141c-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="0141c-140">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0141c-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0141c-141">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0141c-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0141c-142">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0141c-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0141c-143">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0141c-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0141c-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0141c-144">Requirements</span></span>



| <span data-ttu-id="0141c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0141c-145">Requirement</span></span> | <span data-ttu-id="0141c-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0141c-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0141c-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0141c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0141c-148">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="0141c-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0141c-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0141c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0141c-150">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0141c-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0141c-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0141c-151">Namespace</span></span><br/>                | <span data-ttu-id="0141c-152">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="0141c-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0141c-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0141c-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0141c-154"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0141c-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0141c-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0141c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0141c-156">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="0141c-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-157">**DisableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="0141c-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-158">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="0141c-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-159">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="0141c-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-160">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="0141c-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-161">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="0141c-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-162">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="0141c-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-163">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="0141c-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-164">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="0141c-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="0141c-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0141c-166">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="0141c-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
