---
description: Protegge la chiave di crittografia del volume con una chiave esterna a 256 bit.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Metodo ProtectKeyWithExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306381"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2dee7-103">Metodo ProtectKeyWithExternalKey della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="2dee7-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2dee7-104">Il metodo **ProtectKeyWithExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume con una chiave esterna a 256 bit.</span><span class="sxs-lookup"><span data-stu-id="2dee7-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="2dee7-105">Questa chiave esterna può essere usata per il ripristino in caso di errori di autenticazione di altre protezioni con chiave (ad esempio, TPM).</span><span class="sxs-lookup"><span data-stu-id="2dee7-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="2dee7-106">Usare il metodo [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) per salvare la chiave esterna in un file.</span><span class="sxs-lookup"><span data-stu-id="2dee7-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="2dee7-107">I dispositivi di memoria USB che contengono la chiave esterna possono essere utilizzati come chiave di avvio o chiave di ripristino all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="2dee7-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="2dee7-108">Viene creata una protezione con chiave di tipo "chiave esterna" per il volume.</span><span class="sxs-lookup"><span data-stu-id="2dee7-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dee7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dee7-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="2dee7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dee7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dee7-111">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2dee7-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2dee7-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="2dee7-112">Type: **string**</span></span>

<span data-ttu-id="2dee7-113">Stringa che specifica un identificatore assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="2dee7-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="2dee7-114">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="2dee7-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="2dee7-115">*ExternalKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2dee7-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2dee7-116">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="2dee7-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="2dee7-117">Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="2dee7-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="2dee7-118">Se non viene specificata alcuna chiave esterna, ne viene generata una in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="2dee7-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="2dee7-119">Usare il metodo [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) per ottenere la chiave generata in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="2dee7-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="2dee7-120">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2dee7-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dee7-121">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="2dee7-121">Type: **string**</span></span>

<span data-ttu-id="2dee7-122">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="2dee7-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="2dee7-123">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="2dee7-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dee7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dee7-124">Return value</span></span>

<span data-ttu-id="2dee7-125">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2dee7-125">Type: **uint32**</span></span>

<span data-ttu-id="2dee7-126">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2dee7-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2dee7-127">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dee7-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="2dee7-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dee7-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dee7-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2dee7-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="2dee7-130">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="2dee7-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2dee7-131"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="2dee7-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="2dee7-132">Il parametro *ExternalKey* è specificato ma non è una matrice di dimensione 4.</span><span class="sxs-lookup"><span data-stu-id="2dee7-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="2dee7-133"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2dee7-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="2dee7-134">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="2dee7-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2dee7-135"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2dee7-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="2dee7-136">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2dee7-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2dee7-137">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2dee7-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2dee7-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dee7-138">Remarks</span></span>

<span data-ttu-id="2dee7-139">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2dee7-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2dee7-140">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2dee7-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2dee7-141">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2dee7-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2dee7-142">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2dee7-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2dee7-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dee7-143">Requirements</span></span>



| <span data-ttu-id="2dee7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dee7-144">Requirement</span></span> | <span data-ttu-id="2dee7-145">Valore</span><span class="sxs-lookup"><span data-stu-id="2dee7-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dee7-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dee7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2dee7-147">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="2dee7-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2dee7-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dee7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2dee7-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2dee7-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2dee7-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2dee7-150">Namespace</span></span><br/>                | <span data-ttu-id="2dee7-151">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2dee7-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2dee7-152">MOF</span><span class="sxs-lookup"><span data-stu-id="2dee7-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2dee7-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2dee7-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dee7-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dee7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dee7-155">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="2dee7-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
