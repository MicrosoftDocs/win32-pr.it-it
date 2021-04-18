---
description: Fornisce informazioni sullo stato di un test dell'hardware di un volume del sistema operativo completamente decrittografato.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Metodo GetHardwareTestStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316111"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b1343-103">Metodo GetHardwareTestStatus della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b1343-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b1343-104">Il metodo **GetHardwareTestStatus** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) fornisce informazioni sullo stato di un test hardware di un volume del sistema operativo completamente decrittografato.</span><span class="sxs-lookup"><span data-stu-id="b1343-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="b1343-105">Utilizzare questo metodo per indicare se un test hardware è in sospeso, nonché l'esito positivo o negativo di un test hardware completato durante l'ultimo riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="b1343-106">Per richiedere un test hardware, usare il metodo [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b1343-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1343-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1343-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="b1343-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1343-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1343-109">*TestStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1343-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1343-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1343-110">Type: **uint32**</span></span>

<span data-ttu-id="b1343-111">Specifica se un test hardware è in sospeso, nonché l'esito negativo di un test hardware completato durante l'ultimo riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1343-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b1343-112">Value</span></span></th>
<th><span data-ttu-id="b1343-113">Significato</span><span class="sxs-lookup"><span data-stu-id="b1343-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="b1343-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="b1343-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="b1343-115">Se è stato richiesto un test, il test ha avuto esito positivo sull'ultimo riavvio del computer e la crittografia del volume è ora in corso.</span><span class="sxs-lookup"><span data-stu-id="b1343-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="b1343-116">Per lo stato della crittografia, vedere il metodo <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b1343-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="b1343-117">In caso contrario, non viene eseguito alcun test sull'ultimo riavvio del computer e nessuno è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="b1343-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="b1343-118"><dt><strong>Non riuscito</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="b1343-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="b1343-119">La crittografia del volume non è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="b1343-119">Volume encryption did not start.</span></span> <span data-ttu-id="b1343-120">Sono state rimosse tutte le protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="b1343-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="b1343-121">Per risolvere un test non superato:</span><span class="sxs-lookup"><span data-stu-id="b1343-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="b1343-122">Consultare le informazioni nel parametro <em>testError</em> .</span><span class="sxs-lookup"><span data-stu-id="b1343-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="b1343-123">Aggiungere protezioni con chiave e utilizzare nuovamente il metodo <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b1343-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="b1343-124"><dt><strong>In sospeso</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="b1343-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="b1343-125">È stato richiesto un test che verrà eseguito al riavvio successivo del computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="b1343-126">*TestError* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1343-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1343-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1343-127">Type: **uint32**</span></span>

<span data-ttu-id="b1343-128">Specifica l'errore dell'ultimo test hardware completato.</span><span class="sxs-lookup"><span data-stu-id="b1343-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="b1343-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b1343-129">Value</span></span>                                                                                               | <span data-ttu-id="b1343-130">Significato</span><span class="sxs-lookup"><span data-stu-id="b1343-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1343-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="b1343-132">Non si sono verificati errori o non è stato eseguito alcun test hardware nell'ultimo riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="b1343-133"><dt> 2150694972 (0x8031003C)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="b1343-134">il \_ file di FVE E non è stato \_ \_ \_ trovato</span><span class="sxs-lookup"><span data-stu-id="b1343-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="b1343-135">Non è stata trovata un'unità flash USB con un file di chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="b1343-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="b1343-136">Se il problema non viene mantenuto, il computer non è in grado di leggere le unità USB durante il riavvio.</span><span class="sxs-lookup"><span data-stu-id="b1343-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="b1343-137">Potrebbe non essere possibile utilizzare chiavi esterne per sbloccare il volume del sistema operativo durante il riavvio.</span><span class="sxs-lookup"><span data-stu-id="b1343-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b1343-138"><dt> 2150694973 (0x8031003D)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="b1343-139">FVE \_ E il \_ file \_ non è valido</span><span class="sxs-lookup"><span data-stu-id="b1343-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="b1343-140">Il file di chiave esterna nell'unità flash USB è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="b1343-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="b1343-141">Provare con un'altra unità flash USB per archiviare il file di chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="b1343-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="b1343-142"><dt> 2150694975 (0x8031003F)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="b1343-143">FVE \_ E \_ TPM \_ disabilitato</span><span class="sxs-lookup"><span data-stu-id="b1343-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="b1343-144">Il TPM è disabilitato o disattivato o disabilitato e disattivato.</span><span class="sxs-lookup"><span data-stu-id="b1343-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="b1343-145">Per attivare il TPM, utilizzare il provider [**WMI \_ TPM Win32**](win32-tpm.md) o eseguire lo snap-in Gestione TPM (TPM. msc).</span><span class="sxs-lookup"><span data-stu-id="b1343-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="b1343-146"><dt> 2150694977 (0x80310041)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="b1343-147">\_ \_ \_ PCR non valida FVE E TPM \_</span><span class="sxs-lookup"><span data-stu-id="b1343-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="b1343-148">Il TPM ha rilevato una modifica nei servizi di riavvio del sistema operativo all'interno del profilo di convalida della piattaforma corrente.</span><span class="sxs-lookup"><span data-stu-id="b1343-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="b1343-149">Rimuovere qualsiasi CD o DVD di avvio dal computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="b1343-150">Se il problema si verifica in modo permanente, verificare che siano installati gli aggiornamenti più recenti del firmware e del BIOS e che il TPM funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1343-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="b1343-151"><dt>2150694979 (0x80310043)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="b1343-152">FVE \_ E \_ pin \_ non validi</span><span class="sxs-lookup"><span data-stu-id="b1343-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="b1343-153">Il PIN specificato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="b1343-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1343-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1343-154">Return value</span></span>

<span data-ttu-id="b1343-155">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1343-155">Type: **uint32**</span></span>

<span data-ttu-id="b1343-156">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="b1343-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="b1343-157">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1343-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="b1343-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1343-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b1343-159"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="b1343-160">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b1343-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="b1343-161"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="b1343-162">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b1343-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1343-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1343-163">Remarks</span></span>

<span data-ttu-id="b1343-164">Per richiedere un test hardware, usare il metodo [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b1343-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="b1343-165">Per eseguire un test hardware quando lo stato è in sospeso, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="b1343-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="b1343-166">Inserire nel computer un'unità flash USB contenente un file di chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="b1343-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="b1343-167">Questo passaggio si applica solo se il volume ha una protezione con chiave di tipo "chiave esterna" o "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="b1343-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="b1343-168">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-168">Restart the computer.</span></span> <span data-ttu-id="b1343-169">Al riavvio del computer, il test dell'hardware viene eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b1343-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="b1343-170">Per annullare il test dell'hardware, utilizzare il metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b1343-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="b1343-171">Un test con esito positivo determina che:</span><span class="sxs-lookup"><span data-stu-id="b1343-171">A successful test determines that:</span></span>

-   <span data-ttu-id="b1343-172">Il TPM può sbloccare il volume se esiste una protezione con chiave TPM correlata.</span><span class="sxs-lookup"><span data-stu-id="b1343-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="b1343-173">Il computer può leggere un'unità flash USB che contiene un file di chiave esterna durante l'avvio se il volume può essere sbloccato da una chiave esterna (inclusa una chiave di avvio).</span><span class="sxs-lookup"><span data-stu-id="b1343-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="b1343-174">I risultati dei test hardware non saranno disponibili dopo le modifiche apportate alla conversione o dopo il riavvio successivo del computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="b1343-175">Controllare nel registro eventi di sistema le informazioni relative a tutti i test hardware eseguiti in precedenza nel computer.</span><span class="sxs-lookup"><span data-stu-id="b1343-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="b1343-176">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b1343-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b1343-177">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b1343-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b1343-178">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b1343-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b1343-179">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b1343-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1343-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1343-180">Requirements</span></span>



| <span data-ttu-id="b1343-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1343-181">Requirement</span></span> | <span data-ttu-id="b1343-182">Valore</span><span class="sxs-lookup"><span data-stu-id="b1343-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1343-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1343-183">Minimum supported client</span></span><br/> | <span data-ttu-id="b1343-184">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="b1343-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b1343-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1343-185">Minimum supported server</span></span><br/> | <span data-ttu-id="b1343-186">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1343-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1343-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1343-187">Namespace</span></span><br/>                | <span data-ttu-id="b1343-188">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b1343-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b1343-189">MOF</span><span class="sxs-lookup"><span data-stu-id="b1343-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1343-190"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1343-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1343-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1343-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1343-192">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b1343-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
