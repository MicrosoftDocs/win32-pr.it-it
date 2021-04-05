---
description: Indica se il volume e la relativa chiave di crittografia sono protetti.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Metodo GetProtectionStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750842"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1cf21-103">Metodo GetProtectionStatus della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="1cf21-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1cf21-104">Il metodo **GetProtectionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il volume e la relativa chiave di crittografia (se presenti) sono protetti.</span><span class="sxs-lookup"><span data-stu-id="1cf21-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="1cf21-105">La protezione è disattivata se un volume non è crittografato o parzialmente crittografato o se la chiave di crittografia del volume è disponibile in chiaro sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1cf21-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf21-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cf21-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1cf21-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cf21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf21-108">*ProtectionStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1cf21-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cf21-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1cf21-109">Type: **uint32**</span></span>

<span data-ttu-id="1cf21-110">Specifica se il volume e la chiave di crittografia (se presenti) sono protetti.</span><span class="sxs-lookup"><span data-stu-id="1cf21-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1cf21-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1cf21-111">Value</span></span></th>
<th><span data-ttu-id="1cf21-112">Significato</span><span class="sxs-lookup"><span data-stu-id="1cf21-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="1cf21-113"><dt><strong></strong></dt> <dt>0</dt> non protetto </span><span class="sxs-lookup"><span data-stu-id="1cf21-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="1cf21-114">PROTEZIONE NON ATTIVA</span><span class="sxs-lookup"><span data-stu-id="1cf21-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="1cf21-115">Per un HDD standard:</span><span class="sxs-lookup"><span data-stu-id="1cf21-115">For a standard HDD:</span></span><br/> <span data-ttu-id="1cf21-116">Il volume non è crittografato, parzialmente crittografato o la chiave di crittografia del volume è disponibile in chiaro sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1cf21-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="1cf21-117">La chiave di crittografia è disponibile in chiaro sul disco rigido se le protezioni con chiave sono state disabilitate tramite il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o se non sono state specificate protezioni con chiave utilizzando i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cf21-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="1cf21-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="1cf21-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="1cf21-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="1cf21-127">Per un EHDD:</span><span class="sxs-lookup"><span data-stu-id="1cf21-127">For an EHDD:</span></span><br/> <span data-ttu-id="1cf21-128">La banda per il volume viene continuamente sbloccata, non ha un gestore chiavi o è gestita da un gestore di chiavi di terze parti.</span><span class="sxs-lookup"><span data-stu-id="1cf21-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="1cf21-129">Questo può anche significare che la banda è gestita da BitLocker, ma il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> è stato chiamato e l'unità viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="1cf21-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="1cf21-130"><dt><strong>Protetto</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="1cf21-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="1cf21-131">PROTEZIONE SU</span><span class="sxs-lookup"><span data-stu-id="1cf21-131">PROTECTION ON</span></span><br/> <span data-ttu-id="1cf21-132">Per un HDD standard:</span><span class="sxs-lookup"><span data-stu-id="1cf21-132">For a standard HDD:</span></span><br/> <span data-ttu-id="1cf21-133">Il volume è completamente crittografato e la chiave di crittografia per il volume non è disponibile in chiaro sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1cf21-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="1cf21-134">Per un EHDD:</span><span class="sxs-lookup"><span data-stu-id="1cf21-134">For an EHDD:</span></span><br/> <span data-ttu-id="1cf21-135">BitLocker è il gestore chiavi della banda.</span><span class="sxs-lookup"><span data-stu-id="1cf21-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="1cf21-136">L'unità può essere bloccata o sbloccata, ma non può essere sbloccata continuamente.</span><span class="sxs-lookup"><span data-stu-id="1cf21-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1cf21-137"><dt><strong>Sconosciuto</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="1cf21-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="1cf21-138">Impossibile determinare lo stato di protezione del volume.</span><span class="sxs-lookup"><span data-stu-id="1cf21-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="1cf21-139">Questo problema può essere causato dal fatto che il volume si trova in uno stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="1cf21-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="1cf21-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise e Windows Server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1cf21-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="1cf21-141">Questo valore è supportato a partire da Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1cf21-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cf21-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cf21-142">Return value</span></span>

<span data-ttu-id="1cf21-143">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1cf21-143">Type: **uint32**</span></span>

<span data-ttu-id="1cf21-144">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1cf21-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1cf21-145">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cf21-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="1cf21-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cf21-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1cf21-147"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1cf21-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="1cf21-148">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="1cf21-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1cf21-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cf21-149">Remarks</span></span>

<span data-ttu-id="1cf21-150">È possibile crittografare un volume solo se si chiama prima [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) o si usa uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cf21-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="1cf21-151">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="1cf21-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-152">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="1cf21-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-153">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="1cf21-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-154">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="1cf21-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-155">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="1cf21-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-156">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="1cf21-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-157">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="1cf21-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="1cf21-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="1cf21-159">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="1cf21-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="1cf21-160">Se pertanto il disco è crittografato e *ProtectionStatus* restituisce zero (Protection off), le chiavi vengono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="1cf21-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="1cf21-161">Usare [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) per elencare le protezioni con chiave che sono state specificate per proteggere la chiave di crittografia del volume.</span><span class="sxs-lookup"><span data-stu-id="1cf21-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="1cf21-162">Se esistono protezioni con chiave ma la protezione è zero (protezione disattivata), usare [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) per attivare la protezione del volume.</span><span class="sxs-lookup"><span data-stu-id="1cf21-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="1cf21-163">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1cf21-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1cf21-164">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1cf21-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1cf21-165">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1cf21-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1cf21-166">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1cf21-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf21-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cf21-167">Requirements</span></span>



| <span data-ttu-id="1cf21-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf21-168">Requirement</span></span> | <span data-ttu-id="1cf21-169">Valore</span><span class="sxs-lookup"><span data-stu-id="1cf21-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf21-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cf21-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf21-171">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="1cf21-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1cf21-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cf21-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf21-173">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1cf21-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cf21-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1cf21-174">Namespace</span></span><br/>                | <span data-ttu-id="1cf21-175">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1cf21-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1cf21-176">MOF</span><span class="sxs-lookup"><span data-stu-id="1cf21-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cf21-177"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cf21-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf21-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cf21-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf21-179">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1cf21-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
