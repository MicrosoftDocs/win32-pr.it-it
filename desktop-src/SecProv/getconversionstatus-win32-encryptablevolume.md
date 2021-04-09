---
description: Indica lo stato della crittografia o della decrittografia nel volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Metodo GetConversionStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878934"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b09cb-103">Metodo GetConversionStatus della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b09cb-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b09cb-104">Il metodo **GetConversionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica lo stato della crittografia o della decrittografia nel volume.</span><span class="sxs-lookup"><span data-stu-id="b09cb-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="b09cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b09cb-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="b09cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b09cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b09cb-107">*ConversionStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b09cb-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-108">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-109">Stato di crittografia o decrittografia del volume.</span><span class="sxs-lookup"><span data-stu-id="b09cb-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="b09cb-110">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b09cb-110">This can be one of the following values.</span></span>



| <span data-ttu-id="b09cb-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b09cb-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="b09cb-112">Significato</span><span class="sxs-lookup"><span data-stu-id="b09cb-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="b09cb-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="b09cb-114">Per un disco rigido standard (HDD), il volume viene completamente decrittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="b09cb-115">Per un disco rigido crittografato hardware (EHDD), il volume viene costantemente sbloccato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="b09cb-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="b09cb-117">Per un disco rigido standard (HDD), il volume è completamente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="b09cb-118">Per un disco rigido crittografato hardware (EHDD), il volume non viene sbloccato continuamente.</span><span class="sxs-lookup"><span data-stu-id="b09cb-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="b09cb-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b09cb-120">Il volume è parzialmente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="b09cb-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b09cb-122">Il volume è parzialmente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="b09cb-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="b09cb-124">Il volume è stato sospeso durante lo stato della crittografia.</span><span class="sxs-lookup"><span data-stu-id="b09cb-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="b09cb-125">Il volume è parzialmente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="b09cb-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="b09cb-127">Il volume è stato sospeso durante lo stato di decrittografia.</span><span class="sxs-lookup"><span data-stu-id="b09cb-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="b09cb-128">Il volume è parzialmente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="b09cb-129">*EncryptionPercentage* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b09cb-130">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-130">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-131">Percentuale del volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="b09cb-132">Si tratta di un numero intero compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="b09cb-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="b09cb-133">A causa dell'arrotondamento dei numeri, una percentuale di crittografia pari a 0 o 100 non indica necessariamente che il disco è completamente decrittografato o completamente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="b09cb-134">Usare sempre *ConversionStatus* per determinare se il disco è effettivamente completamente decrittografato o completamente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="b09cb-135">*EncryptionFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b09cb-136">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-136">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-137">Flag che descrivono il comportamento di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b09cb-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="b09cb-138">Una combinazione di 32 bit con i bit seguenti attualmente definiti.</span><span class="sxs-lookup"><span data-stu-id="b09cb-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="b09cb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="b09cb-139">Value</span></span>                                                                                  | <span data-ttu-id="b09cb-140">Significato</span><span class="sxs-lookup"><span data-stu-id="b09cb-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b09cb-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="b09cb-142">Eseguire la crittografia del volume in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b09cb-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="b09cb-143">Se la crittografia è stata sospesa o arrestata, la chiamata del metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) riprende effettivamente la conversione e il valore di questo bit viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="b09cb-144">Questo bit ha effetto solo quando i metodi **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) avviano la crittografia dallo stato completamente decrittografato, decrittografia nello stato di avanzamento o decrittografia in pausa.</span><span class="sxs-lookup"><span data-stu-id="b09cb-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="b09cb-145">Se questo bit è zero, vale a dire che non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="b09cb-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="b09cb-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="b09cb-147">Eseguire la cancellazione su richiesta dello spazio disponibile nel volume.</span><span class="sxs-lookup"><span data-stu-id="b09cb-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="b09cb-148">La chiamata al metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) con questo set di bit è consentita solo quando il volume non è attualmente in fase di conversione o cancellazione e si trova in uno stato "crittografato".</span><span class="sxs-lookup"><span data-stu-id="b09cb-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="b09cb-149"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="b09cb-150">Eseguire in modo sincrono l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="b09cb-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="b09cb-151">La chiamata verrà bloccata fino a quando l'operazione richiesta non è stata completata o è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="b09cb-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="b09cb-152">Questo flag è supportato solo con il metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b09cb-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="b09cb-153">Questo flag può essere **specificato quando viene chiamata la crittografia per** riprendere la crittografia arrestata o interrotta o cancellare o quando è in corso la crittografia o la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="b09cb-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="b09cb-154">Ciò consente al chiamante di riprendere l'attesa in modo sincrono finché il processo non viene completato o interrotto.</span><span class="sxs-lookup"><span data-stu-id="b09cb-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="b09cb-155">*WipingStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b09cb-156">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-156">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-157">Stato cancellazione spazio libero.</span><span class="sxs-lookup"><span data-stu-id="b09cb-157">Free space wiping status.</span></span> <span data-ttu-id="b09cb-158">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b09cb-158">This can be one of the following values.</span></span>



| <span data-ttu-id="b09cb-159">Valore</span><span class="sxs-lookup"><span data-stu-id="b09cb-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="b09cb-160">Significato</span><span class="sxs-lookup"><span data-stu-id="b09cb-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="b09cb-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="b09cb-162">Lo spazio libero non è stato cancellato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="b09cb-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="b09cb-164">Lo spazio libero è stato cancellato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="b09cb-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b09cb-166">La cancellazione dello spazio disponibile è attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="b09cb-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="b09cb-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="b09cb-168">Cancellazione dello spazio disponibile sospesa.</span><span class="sxs-lookup"><span data-stu-id="b09cb-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="b09cb-169">*WipingPercentage* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b09cb-170">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-170">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-171">Valore compreso tra 0 e 100 che specifica la percentuale di spazio libero che è stata cancellata.</span><span class="sxs-lookup"><span data-stu-id="b09cb-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="b09cb-172">*PrecisionFactor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b09cb-173">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-173">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-174">Valore compreso tra 0 e 4 che specifica il livello di precisione</span><span class="sxs-lookup"><span data-stu-id="b09cb-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b09cb-175">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b09cb-175">Return value</span></span>

<span data-ttu-id="b09cb-176">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-176">Type: **uint32**</span></span>

<span data-ttu-id="b09cb-177">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b09cb-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b09cb-178">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b09cb-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="b09cb-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b09cb-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b09cb-180"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="b09cb-181">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b09cb-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="b09cb-182"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="b09cb-183">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b09cb-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="b09cb-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="b09cb-184">Remarks</span></span>

<span data-ttu-id="b09cb-185">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b09cb-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b09cb-186">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b09cb-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b09cb-187">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b09cb-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b09cb-188">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b09cb-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b09cb-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b09cb-189">Requirements</span></span>



| <span data-ttu-id="b09cb-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="b09cb-190">Requirement</span></span> | <span data-ttu-id="b09cb-191">Valore</span><span class="sxs-lookup"><span data-stu-id="b09cb-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b09cb-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b09cb-192">Minimum supported client</span></span><br/> | <span data-ttu-id="b09cb-193">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b09cb-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b09cb-194">Minimum supported server</span></span><br/> | <span data-ttu-id="b09cb-195">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b09cb-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b09cb-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b09cb-196">Namespace</span></span><br/>                | <span data-ttu-id="b09cb-197">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b09cb-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b09cb-198">MOF</span><span class="sxs-lookup"><span data-stu-id="b09cb-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b09cb-199"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b09cb-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b09cb-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b09cb-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09cb-201">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b09cb-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
