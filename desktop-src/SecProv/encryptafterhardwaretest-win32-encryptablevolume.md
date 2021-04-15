---
description: Inizia la crittografia di un volume del sistema operativo completamente decrittografato dopo un test hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Metodo EncryptAfterHardwareTest della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525687"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b65c9-103">Metodo EncryptAfterHardwareTest della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b65c9-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b65c9-104">Il metodo **EncryptAfterHardwareTest** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) inizia la crittografia di un volume del sistema operativo completamente decrittografato dopo un test hardware.</span><span class="sxs-lookup"><span data-stu-id="b65c9-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="b65c9-105">Per eseguire questo test hardware è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b65c9-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="b65c9-106">Utilizzare questo metodo anziché il metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) per verificare che BitLocker funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="b65c9-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="b65c9-107">Se il disco rigido è crittografato con hardware, questo metodo non crittografa i dati.</span><span class="sxs-lookup"><span data-stu-id="b65c9-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="b65c9-108">Imposta invece lo stato della banda su sbloccato da "perennemente sbloccato".</span><span class="sxs-lookup"><span data-stu-id="b65c9-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="b65c9-109">Se la banda è bloccata, sbloccata o di sola lettura, l'unità viene considerata crittografata.</span><span class="sxs-lookup"><span data-stu-id="b65c9-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b65c9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b65c9-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b65c9-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b65c9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65c9-112">*EncryptionMethod* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b65c9-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b65c9-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b65c9-113">Type: **uint32**</span></span>

<span data-ttu-id="b65c9-114">Specifica l'algoritmo di crittografia e le dimensioni della chiave usati per crittografare il volume.</span><span class="sxs-lookup"><span data-stu-id="b65c9-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="b65c9-115">Lasciare vuoto questo parametro per usare il valore predefinito zero.</span><span class="sxs-lookup"><span data-stu-id="b65c9-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="b65c9-116">Se il volume è parzialmente o completamente crittografato, il valore di questo parametro deve essere 0 o corrispondere al metodo di crittografia esistente del volume.</span><span class="sxs-lookup"><span data-stu-id="b65c9-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="b65c9-117">Se l'impostazione di Criteri di gruppo corrispondente è stata abilitata con un valore valido, il valore di questo parametro deve essere 0 o corrispondere all'impostazione Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b65c9-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="b65c9-118">Se l'impostazione di Criteri di gruppo corrispondente non è valida, viene usato il valore predefinito di AES 128 con diffusore.</span><span class="sxs-lookup"><span data-stu-id="b65c9-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="b65c9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b65c9-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="b65c9-120">Significato</span><span class="sxs-lookup"><span data-stu-id="b65c9-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="b65c9-121">Non <dt>**specificato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="b65c9-122">Usare l'impostazione del Criteri di gruppo corrente, se disponibile e valida, oppure il metodo di crittografia predefinito in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b65c9-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b65c9-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="b65c9-124">AES 128 CON DIFFUSIONE</span><span class="sxs-lookup"><span data-stu-id="b65c9-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="b65c9-125">Crittografare il volume usando l'algoritmo di Advanced Encryption Standard (AES) migliorato con un livello di diffusione e usando una dimensione della chiave AES di 128 bit.</span><span class="sxs-lookup"><span data-stu-id="b65c9-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="b65c9-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="b65c9-127">AES 256 CON DIFFUSIONE</span><span class="sxs-lookup"><span data-stu-id="b65c9-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="b65c9-128">Crittografare il volume usando l'algoritmo di Advanced Encryption Standard (AES) migliorato con un livello di diffusione e usando una dimensione della chiave AES di 256 bit.</span><span class="sxs-lookup"><span data-stu-id="b65c9-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="b65c9-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="b65c9-130">Crittografare il volume usando l'algoritmo Advanced Encryption Standard (AES) e usando una dimensione della chiave AES di 128 bit.</span><span class="sxs-lookup"><span data-stu-id="b65c9-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="b65c9-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="b65c9-132">Crittografare il volume usando l'algoritmo Advanced Encryption Standard (AES) e usando una dimensione della chiave AES di 256 bit.</span><span class="sxs-lookup"><span data-stu-id="b65c9-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="b65c9-133">*EncryptionFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b65c9-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b65c9-134">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b65c9-134">Type: **uint32**</span></span>

<span data-ttu-id="b65c9-135">Flag che descrivono il comportamento di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b65c9-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="b65c9-136">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise e Windows server 2008:** Questo parametro non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b65c9-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="b65c9-137">Una combinazione di 32 bit con i bit seguenti attualmente definiti.</span><span class="sxs-lookup"><span data-stu-id="b65c9-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="b65c9-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b65c9-138">Value</span></span>                                                                                  | <span data-ttu-id="b65c9-139">Significato</span><span class="sxs-lookup"><span data-stu-id="b65c9-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b65c9-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="b65c9-141">Eseguire la crittografia del volume in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b65c9-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="b65c9-142">Se la crittografia è stata sospesa o arrestata, la chiamata del metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) riprende effettivamente la conversione e il valore di questo bit viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b65c9-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="b65c9-143">Questo bit ha effetto solo quando i metodi **Encrypt** o **EncryptAfterHardwareTest** avviano la crittografia dallo stato completamente decrittografato, decrittografia nello stato di avanzamento o decrittografia in pausa.</span><span class="sxs-lookup"><span data-stu-id="b65c9-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="b65c9-144">Se questo bit è zero, vale a dire che non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="b65c9-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="b65c9-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="b65c9-146">Eseguire la cancellazione su richiesta dello spazio disponibile nel volume.</span><span class="sxs-lookup"><span data-stu-id="b65c9-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="b65c9-147">La chiamata al metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) con questo set di bit è consentita solo quando il volume non è attualmente in fase di conversione o cancellazione e si trova in uno stato "crittografato".</span><span class="sxs-lookup"><span data-stu-id="b65c9-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="b65c9-148"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="b65c9-149">Eseguire in modo sincrono l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="b65c9-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="b65c9-150">La chiamata verrà bloccata fino a quando l'operazione richiesta non è stata completata o è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="b65c9-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="b65c9-151">Questo flag è supportato solo con il metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b65c9-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="b65c9-152">Questo flag può essere **specificato quando viene chiamata la crittografia per** riprendere la crittografia arrestata o interrotta o cancellare o quando è in corso la crittografia o la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="b65c9-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="b65c9-153">Ciò consente al chiamante di riprendere l'attesa in modo sincrono finché il processo non viene completato o interrotto.</span><span class="sxs-lookup"><span data-stu-id="b65c9-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65c9-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b65c9-154">Return value</span></span>

<span data-ttu-id="b65c9-155">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b65c9-155">Type: **uint32**</span></span>

<span data-ttu-id="b65c9-156">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b65c9-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="b65c9-157">Questo metodo restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="b65c9-157">This method returns immediately.</span></span> <span data-ttu-id="b65c9-158">Se il volume è già completamente crittografato e non vengono restituiti altri errori, questo metodo restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b65c9-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b65c9-159">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b65c9-159">Return code/value</span></span></th>
<th><span data-ttu-id="b65c9-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b65c9-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="b65c9-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-162">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b65c9-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b65c9-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-164">Il parametro <em>EncryptionMethod</em> è specificato ma non rientra nell'intervallo noto o non corrisponde all'impostazione criteri di gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="b65c9-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b65c9-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-166">Non esiste alcuna chiave di crittografia per il volume.</span><span class="sxs-lookup"><span data-stu-id="b65c9-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="b65c9-167">Disabilitare le protezioni con chiave utilizzando il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> oppure utilizzare uno dei metodi seguenti per specificare le protezioni con chiave per il volume:</span><span class="sxs-lookup"><span data-stu-id="b65c9-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="b65c9-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b65c9-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-175">Non è possibile crittografare il volume perché questo computer è configurato come parte di un cluster di server.</span><span class="sxs-lookup"><span data-stu-id="b65c9-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b65c9-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-177">Non è possibile trovare protezioni con chiave di tipo &quot; TPM &quot; , &quot; TPM e pin &quot; , &quot; TPM, pin e chiave di avvio &quot; , &quot; TPM e chiave di avvio &quot; oppure &quot; chiave esterna &quot; .</span><span class="sxs-lookup"><span data-stu-id="b65c9-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="b65c9-178">Il test hardware riguarda solo le protezioni con chiave precedenti.</span><span class="sxs-lookup"><span data-stu-id="b65c9-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="b65c9-179">Se si vuole comunque eseguire un test dell'hardware, è necessario usare uno dei metodi seguenti per specificare le protezioni con chiave per il volume:</span><span class="sxs-lookup"><span data-stu-id="b65c9-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="b65c9-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b65c9-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-187">Il volume è parzialmente o completamente crittografato.</span><span class="sxs-lookup"><span data-stu-id="b65c9-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="b65c9-188">Il test dell'hardware viene applicato prima della crittografia.</span><span class="sxs-lookup"><span data-stu-id="b65c9-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="b65c9-189">Se si vuole ancora eseguire il test, usare prima il metodo <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> e quindi usare uno dei metodi seguenti per aggiungere protezioni con chiave:</span><span class="sxs-lookup"><span data-stu-id="b65c9-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="b65c9-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="b65c9-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="b65c9-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b65c9-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-196">Il volume è un volume di dati.</span><span class="sxs-lookup"><span data-stu-id="b65c9-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="b65c9-197">Il test dell'hardware si applica solo ai volumi che possono avviare il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b65c9-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="b65c9-198">Eseguire questo metodo sul volume del sistema operativo attualmente avviato.</span><span class="sxs-lookup"><span data-stu-id="b65c9-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b65c9-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="b65c9-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="b65c9-200">Non è stata specificata alcuna protezione con chiave della &quot; password numerica di tipo &quot; .</span><span class="sxs-lookup"><span data-stu-id="b65c9-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="b65c9-201">Per Active Directory Domain Services, il Criteri di gruppo richiede un backup delle informazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b65c9-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="b65c9-202">Per aggiungere almeno una protezione con chiave di quel tipo, usare il metodo <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b65c9-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b65c9-203">Commenti</span><span class="sxs-lookup"><span data-stu-id="b65c9-203">Remarks</span></span>

<span data-ttu-id="b65c9-204">Quando si utilizza questo metodo senza il secondo parametro facoltativo (in base alla definizione di Windows 7 e Windows Vista Enterprise), il metodo avvierà sempre la conversione in modalità completa per mantenere il comportamento compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b65c9-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="b65c9-205">In questo modo la sicurezza prevista per le applicazioni e gli script esistenti non verrà interruppe con l'aggiunta del secondo parametro facoltativo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b65c9-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="b65c9-206">A differenza del metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) , questo metodo esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b65c9-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="b65c9-207">Verifica se il TPM sarà in grado di sbloccare il volume, se esiste una protezione con chiave TPM correlata.</span><span class="sxs-lookup"><span data-stu-id="b65c9-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="b65c9-208">Verifica se il computer è in grado di leggere un'unità flash USB che contiene un file di chiave esterna durante l'avvio, se il volume verrà sbloccato da una chiave esterna (inclusa una chiave di avvio).</span><span class="sxs-lookup"><span data-stu-id="b65c9-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="b65c9-209">Richiede il riavvio del computer per eseguire il test dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="b65c9-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="b65c9-210">Inizia la crittografia solo se il test dell'hardware riesce.</span><span class="sxs-lookup"><span data-stu-id="b65c9-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="b65c9-211">Non può essere usato in un volume di dati, in un volume parzialmente o completamente crittografato o per riprendere la crittografia.</span><span class="sxs-lookup"><span data-stu-id="b65c9-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="b65c9-212">Prima di eseguire questo metodo, usare i metodi seguenti per creare le protezioni con chiave correlate:</span><span class="sxs-lookup"><span data-stu-id="b65c9-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="b65c9-213">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="b65c9-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="b65c9-214">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="b65c9-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="b65c9-215">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="b65c9-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="b65c9-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="b65c9-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="b65c9-217">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="b65c9-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="b65c9-218">Dopo l'esecuzione di questo metodo, eseguire i passaggi aggiuntivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b65c9-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="b65c9-219">Inserire nel computer un'unità flash USB contenente un file di chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="b65c9-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="b65c9-220">Questo passaggio si applica solo se il volume ha una protezione con chiave di tipo "chiave esterna" o "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="b65c9-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="b65c9-221">Riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b65c9-221">Restart the computer.</span></span>

<span data-ttu-id="b65c9-222">Al riavvio del computer, il test dell'hardware viene eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b65c9-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="b65c9-223">La crittografia viene avviata in caso di esito positivo del test hardware.</span><span class="sxs-lookup"><span data-stu-id="b65c9-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="b65c9-224">In caso contrario, tentare di risolvere eventuali errori hardware.</span><span class="sxs-lookup"><span data-stu-id="b65c9-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="b65c9-225">Eseguire [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) dopo il riavvio del computer per ottenere i risultati del test.</span><span class="sxs-lookup"><span data-stu-id="b65c9-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="b65c9-226">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b65c9-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b65c9-227">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b65c9-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b65c9-228">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b65c9-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b65c9-229">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b65c9-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b65c9-230">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b65c9-230">Requirements</span></span>



| <span data-ttu-id="b65c9-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65c9-231">Requirement</span></span> | <span data-ttu-id="b65c9-232">Valore</span><span class="sxs-lookup"><span data-stu-id="b65c9-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b65c9-233">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65c9-233">Minimum supported client</span></span><br/> | <span data-ttu-id="b65c9-234">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="b65c9-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b65c9-235">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65c9-235">Minimum supported server</span></span><br/> | <span data-ttu-id="b65c9-236">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b65c9-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b65c9-237">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b65c9-237">Namespace</span></span><br/>                | <span data-ttu-id="b65c9-238">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b65c9-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b65c9-239">MOF</span><span class="sxs-lookup"><span data-stu-id="b65c9-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b65c9-240"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b65c9-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65c9-241">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b65c9-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65c9-242">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b65c9-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
