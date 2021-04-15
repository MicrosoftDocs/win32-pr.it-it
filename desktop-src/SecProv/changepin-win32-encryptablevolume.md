---
description: Modifica il PIN associato a un volume crittografato.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Metodo Changepin aggiorna della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525693"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="effc2-103">Metodo Changepin aggiorna della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="effc2-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="effc2-104">Il metodo **changepin Aggiorna** della classe [**\_ ENCRYPTABLEVOLUME Win32**](win32-encryptablevolume.md) modifica il PIN associato a un volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="effc2-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="effc2-105">Se è abilitato il criterio di gruppo "Consenti PIN avanzati per l'avvio", un PIN può contenere lettere, simboli e spazi, oltre ai numeri.</span><span class="sxs-lookup"><span data-stu-id="effc2-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="effc2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="effc2-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="effc2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="effc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effc2-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="effc2-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effc2-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="effc2-109">Type: **string**</span></span>

<span data-ttu-id="effc2-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="effc2-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="effc2-111">*NewPIN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="effc2-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effc2-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="effc2-112">Type: **string**</span></span>

<span data-ttu-id="effc2-113">Stringa di identificazione personale specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="effc2-113">A user-specified personal identification string.</span></span> <span data-ttu-id="effc2-114">Questa stringa deve essere composta da una sequenza da 4 a 20 cifre oppure, se è abilitato il criterio di gruppo "Consenti PIN avanzati per l'avvio", da 4 a 20 lettere, simboli, spazi o numeri.</span><span class="sxs-lookup"><span data-stu-id="effc2-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effc2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="effc2-115">Return value</span></span>

<span data-ttu-id="effc2-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="effc2-116">Type: **uint32**</span></span>

<span data-ttu-id="effc2-117">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="effc2-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="effc2-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="effc2-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="effc2-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="effc2-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="effc2-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="effc2-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="effc2-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="effc2-122"><dt>**FVE \_ E \_ \_ CDDVD di avvio**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="effc2-123">Nel computer è presente un CD/DVD di avvio.</span><span class="sxs-lookup"><span data-stu-id="effc2-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="effc2-124">Rimuovere il CD/DVD e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="effc2-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="effc2-125"><dt>**FVE \_ E \_ \_ \_ caratteri PIN non validi**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="effc2-126">Il parametro *NewPIN* contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="effc2-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="effc2-127">Quando il Criteri di gruppo "Consenti PIN avanzati per l'avvio" è disabilitato, sono supportati solo i numeri.</span><span class="sxs-lookup"><span data-stu-id="effc2-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="effc2-128"><dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="effc2-129">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password" o "External Key".</span><span class="sxs-lookup"><span data-stu-id="effc2-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="effc2-130">Usare il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="effc2-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="effc2-131"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="effc2-132">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="effc2-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="effc2-133"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="effc2-134">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="effc2-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="effc2-135">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="effc2-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="effc2-136"><dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza PIN non valida**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="effc2-137">Il parametro *NewPIN* specificato può essere composto da più di 20 caratteri, più corto di 4 caratteri o più breve della lunghezza minima specificata da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="effc2-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="effc2-138"><dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="effc2-139">La protezione con chiave specificata non esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="effc2-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="effc2-140"><dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="effc2-141">Nel computer non sono stati trovati Trusted Platform Module compatibili (TPM).</span><span class="sxs-lookup"><span data-stu-id="effc2-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="effc2-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="effc2-142">Remarks</span></span>

<span data-ttu-id="effc2-143">Il metodo **changepin Aggiorna** crea una nuova protezione con TPM e pin in base alle informazioni di protezione esistenti e al pin appena fornito.</span><span class="sxs-lookup"><span data-stu-id="effc2-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="effc2-144">La nuova protezione avrà lo stesso GUID.</span><span class="sxs-lookup"><span data-stu-id="effc2-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="effc2-145">Il metodo **changepin Aggiorna** può essere chiamato anche per modificare il pin di una protezione con chiave che usa un PIN, ad esempio TPM e PIN o TPM con pin e USB.</span><span class="sxs-lookup"><span data-stu-id="effc2-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="effc2-146">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="effc2-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="effc2-147">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="effc2-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="effc2-148">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="effc2-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="effc2-149">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="effc2-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="effc2-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="effc2-150">Requirements</span></span>



| <span data-ttu-id="effc2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="effc2-151">Requirement</span></span> | <span data-ttu-id="effc2-152">Valore</span><span class="sxs-lookup"><span data-stu-id="effc2-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effc2-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="effc2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="effc2-154">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="effc2-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="effc2-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="effc2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="effc2-156">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="effc2-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="effc2-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="effc2-157">Namespace</span></span><br/>                | <span data-ttu-id="effc2-158">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="effc2-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="effc2-159">MOF</span><span class="sxs-lookup"><span data-stu-id="effc2-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="effc2-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="effc2-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="effc2-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="effc2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effc2-162">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="effc2-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
