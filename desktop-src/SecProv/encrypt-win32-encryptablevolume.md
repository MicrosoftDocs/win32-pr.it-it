---
description: Inizia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Metodo Encrypt della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058224"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e5b0b-103">Metodo Encrypt della classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="e5b0b-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e5b0b-104">Il metodo **Encrypt** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inizia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="e5b0b-105">Quando la crittografia viene sospesa o in corso, questo metodo si comporta in modo analogo a [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="e5b0b-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="e5b0b-106">Quando la decrittografia è sospesa o in corso, questo metodo interrompe la decrittografia e inizia la crittografia.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="e5b0b-107">Se l'unità è crittografata con hardware, questo metodo non crittografa i dati.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="e5b0b-108">Imposta invece lo stato della banda su "sbloccato" da "sempre sbloccato".</span><span class="sxs-lookup"><span data-stu-id="e5b0b-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="e5b0b-109">Se la banda è bloccata, sbloccata o di sola lettura, l'unità viene considerata crittografata.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="e5b0b-110">**Windows Vista:** La crittografia di un volume diverso dal volume del sistema operativo attualmente in esecuzione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b0b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5b0b-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e5b0b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5b0b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b0b-113">*EncryptionMethod* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5b0b-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b0b-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5b0b-114">Type: **uint32**</span></span>

<span data-ttu-id="e5b0b-115">Unsigned Integer che specifica l'algoritmo di crittografia e le dimensioni della chiave usati per crittografare il volume.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="e5b0b-116">Se questo parametro è maggiore di zero e il volume è parzialmente o completamente crittografato, *EncryptionMethod* deve corrispondere al metodo di crittografia esistente del volume.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="e5b0b-117">Se questo parametro è maggiore di zero e l'impostazione Criteri di gruppo corrispondente è abilitata con un valore valido, *EncryptionMethod* deve corrispondere all'impostazione criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="e5b0b-118">Per un elenco dei valori EncryptionMethod possibili, vedere il metodo [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b0b-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="e5b0b-119">Il valore predefinito per Windows 7 o versioni precedenti è: 1 (AES \_ 128 \_ con \_ diffusore).</span><span class="sxs-lookup"><span data-stu-id="e5b0b-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="e5b0b-120">Il valore predefinito per Windows 8, Windows 8.1 o Windows 10, versione 1507 è: 3 (AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="e5b0b-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="e5b0b-121">Il valore predefinito per Windows 10, versione 1511 o successiva è: 6 (XTS \_ AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="e5b0b-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="e5b0b-122">*EncryptionFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e5b0b-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e5b0b-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5b0b-123">Type: **uint32**</span></span>

<span data-ttu-id="e5b0b-124">Flag che descrivono il comportamento di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="e5b0b-125">**Windows 7, Windows server 2008 R2, Windows Vista Enterprise e Windows server 2008:** Questo parametro non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="e5b0b-126">Una combinazione di 32 bit con i bit seguenti attualmente definiti.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="e5b0b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b0b-127">Value</span></span>                                                                                  | <span data-ttu-id="e5b0b-128">Significato</span><span class="sxs-lookup"><span data-stu-id="e5b0b-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5b0b-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e5b0b-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="e5b0b-130">Eseguire la crittografia del volume in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="e5b0b-131">Se la crittografia è stata sospesa o arrestata, la chiamata del metodo **Encrypt** riprende effettivamente la conversione e il valore di questo bit viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="e5b0b-132">Questo bit ha effetto solo quando i metodi **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) avviano la crittografia dallo stato completamente decrittografato, decrittografia nello stato di avanzamento o decrittografia in pausa.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="e5b0b-133">Se questo bit è zero, vale a dire che non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="e5b0b-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e5b0b-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="e5b0b-135">Eseguire la cancellazione su richiesta dello spazio disponibile nel volume.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="e5b0b-136">La chiamata al metodo **Encrypt** con questo set di bit è consentita solo quando il volume non è attualmente in fase di conversione o cancellazione e si trova in uno stato "crittografato".</span><span class="sxs-lookup"><span data-stu-id="e5b0b-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e5b0b-137"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="e5b0b-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="e5b0b-138">Eseguire in modo sincrono l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="e5b0b-139">La chiamata verrà bloccata fino a quando l'operazione richiesta non è stata completata o è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="e5b0b-140">Questo flag è supportato solo con il metodo **Encrypt** .</span><span class="sxs-lookup"><span data-stu-id="e5b0b-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="e5b0b-141">Questo flag può essere **specificato quando viene chiamata la crittografia per** riprendere la crittografia arrestata o interrotta o cancellare o quando è in corso la crittografia o la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="e5b0b-142">Ciò consente al chiamante di riprendere l'attesa in modo sincrono finché il processo non viene completato o interrotto.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b0b-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5b0b-143">Return value</span></span>

<span data-ttu-id="e5b0b-144">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5b0b-144">Type: **uint32**</span></span>

<span data-ttu-id="e5b0b-145">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="e5b0b-146">Questo metodo restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-146">This method returns immediately.</span></span> <span data-ttu-id="e5b0b-147">Se il volume è già completamente crittografato e non vengono restituiti altri errori, questo metodo restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5b0b-148">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5b0b-148">Return code/value</span></span></th>
<th><span data-ttu-id="e5b0b-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5b0b-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="e5b0b-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-151">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e5b0b-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-153">Il parametro <em>EncryptionMethod</em> è specificato ma non rientra nell'intervallo noto o non corrisponde all'impostazione criteri di gruppo corrente.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e5b0b-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-155">Non esiste alcuna chiave di crittografia per il volume.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="e5b0b-156">Disabilitare le protezioni con chiave utilizzando il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o utilizzare uno dei metodi seguenti per specificare le protezioni con chiave per il volume:</span><span class="sxs-lookup"><span data-stu-id="e5b0b-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="e5b0b-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5b0b-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="e5b0b-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5b0b-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="e5b0b-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5b0b-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="e5b0b-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5b0b-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="e5b0b-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5b0b-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="e5b0b-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5b0b-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="e5b0b-163">
<strong>Windows Vista:</strong> Quando non esiste alcuna chiave di crittografia per il volume, viene invece restituito ERROR_INVALID_OPERATION.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="e5b0b-164">Il valore decimale è 4317 e il valore esadecimale è 0x10DD.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e5b0b-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-166">Il metodo di crittografia specificato non corrisponde a quello del volume parzialmente o completamente crittografato.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="e5b0b-167">Per continuare la crittografia, lasciare vuoto il parametro <em>EncryptionMethod</em> o usare un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e5b0b-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-169">Non è possibile crittografare il volume perché questo computer è configurato come parte di un cluster di server.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="e5b0b-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-171">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="e5b0b-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="e5b0b-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="e5b0b-173">Non è stata specificata alcuna protezione con chiave della &quot; password numerica di tipo &quot; .</span><span class="sxs-lookup"><span data-stu-id="e5b0b-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="e5b0b-174">Per Active Directory Domain Services, il Criteri di gruppo richiede un backup delle informazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="e5b0b-175">Per aggiungere almeno una protezione con chiave di quel tipo, usare il metodo <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e5b0b-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e5b0b-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5b0b-176">Remarks</span></span>

<span data-ttu-id="e5b0b-177">Quando si utilizza questo metodo senza il secondo parametro facoltativo (in base alla definizione di Windows 7 e Windows Vista Enterprise), il metodo avvierà sempre la conversione in modalità completa per mantenere il comportamento compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="e5b0b-178">In questo modo la sicurezza prevista per le applicazioni e gli script esistenti non verrà interruppe con l'aggiunta del secondo parametro facoltativo in Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="e5b0b-179">È possibile chiamare [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) per determinare se la crittografia è in corso e la percentuale del volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="e5b0b-180">Dopo che il volume è stato completamente crittografato e se sono state aggiunte e abilitate le protezioni con chiave, lo stato di protezione del volume viene modificato in "on".</span><span class="sxs-lookup"><span data-stu-id="e5b0b-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="e5b0b-181">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e5b0b-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e5b0b-182">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e5b0b-183">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e5b0b-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e5b0b-184">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e5b0b-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b0b-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5b0b-185">Requirements</span></span>



| <span data-ttu-id="e5b0b-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b0b-186">Requirement</span></span> | <span data-ttu-id="e5b0b-187">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b0b-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b0b-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b0b-188">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b0b-189">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="e5b0b-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e5b0b-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b0b-190">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b0b-191">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5b0b-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5b0b-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e5b0b-192">Namespace</span></span><br/>                | <span data-ttu-id="e5b0b-193">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="e5b0b-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e5b0b-194">MOF</span><span class="sxs-lookup"><span data-stu-id="e5b0b-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5b0b-195"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5b0b-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b0b-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5b0b-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b0b-197">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="e5b0b-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
