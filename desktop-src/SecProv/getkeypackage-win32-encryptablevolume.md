---
description: Esporta informazioni che possono aiutare a recuperare i dati crittografati quando l'unità è gravemente danneggiata e non sono presenti file di backup dei dati.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Metodo GetKeyPackage della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316108"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="342aa-103">Metodo GetKeyPackage della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="342aa-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="342aa-104">Il metodo **GetKeyPackage** della classe [**\_ EncryptableVolume di Win32**](win32-encryptablevolume.md) Esporta informazioni che possono aiutare a recuperare i dati crittografati quando l'unità è gravemente danneggiata e non sono presenti file di backup dei dati.</span><span class="sxs-lookup"><span data-stu-id="342aa-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="342aa-105">Le informazioni esportate sono costituite dalla chiave di crittografia del volume protetta da una protezione con chiave di tipo "Numerical password" o "External Key".</span><span class="sxs-lookup"><span data-stu-id="342aa-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="342aa-106">Per utilizzare questo pacchetto, è necessario salvare anche la password numerica o la chiave esterna corrispondente.</span><span class="sxs-lookup"><span data-stu-id="342aa-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="342aa-107">Se si sceglie di esportare un pacchetto di chiavi, assicurarsi di conservarle in una posizione ben protetta.</span><span class="sxs-lookup"><span data-stu-id="342aa-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="342aa-108">Non includere queste informazioni nel computer.</span><span class="sxs-lookup"><span data-stu-id="342aa-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="342aa-109">Se il pacchetto di chiavi viene smarrito o rubato, sarà necessario decrittografare il volume e ricrittografarlo utilizzando una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="342aa-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="342aa-110">In caso di errore di un'unità, lo strumento di ripristino di BitLocker esiste per facilitare il recupero dei dati disponibili.</span><span class="sxs-lookup"><span data-stu-id="342aa-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="342aa-111">Per ulteriori informazioni sul modo in cui questo strumento può utilizzare il pacchetto di chiavi, vedere [come utilizzare lo strumento di ripristino di BitLocker per ripristinare i dati da un volume crittografato in Windows Vista](https://support.microsoft.com/kb/928201).</span><span class="sxs-lookup"><span data-stu-id="342aa-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="342aa-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="342aa-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="342aa-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="342aa-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="342aa-114">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="342aa-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="342aa-115">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="342aa-115">Type: **string**</span></span>

<span data-ttu-id="342aa-116">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="342aa-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="342aa-117">Per esportare un pacchetto di chiavi, è necessario usare una protezione con chiave di tipo "Numerical password" o "External Key".</span><span class="sxs-lookup"><span data-stu-id="342aa-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="342aa-118">*Pacchetto di \[ \] pacchetti* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="342aa-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="342aa-119">Tipo: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="342aa-119">Type: **uint8**</span></span>

<span data-ttu-id="342aa-120">Flusso di byte che contiene la chiave di crittografia per un volume, protetto dalla protezione con chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="342aa-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="342aa-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="342aa-121">Return value</span></span>

<span data-ttu-id="342aa-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="342aa-122">Type: **uint32**</span></span>

<span data-ttu-id="342aa-123">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="342aa-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="342aa-124">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="342aa-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="342aa-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="342aa-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="342aa-126"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="342aa-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="342aa-127">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="342aa-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="342aa-128"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="342aa-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="342aa-129">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="342aa-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="342aa-130"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="342aa-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="342aa-131">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="342aa-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="342aa-132">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="342aa-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="342aa-133"><dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="342aa-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="342aa-134">La protezione con chiave specificata non esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="342aa-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="342aa-135"><dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="342aa-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="342aa-136">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password" o "External Key".</span><span class="sxs-lookup"><span data-stu-id="342aa-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="342aa-137">Usare il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="342aa-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="342aa-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="342aa-138">Remarks</span></span>

<span data-ttu-id="342aa-139">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="342aa-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="342aa-140">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="342aa-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="342aa-141">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="342aa-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="342aa-142">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="342aa-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="342aa-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="342aa-143">Requirements</span></span>



| <span data-ttu-id="342aa-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="342aa-144">Requirement</span></span> | <span data-ttu-id="342aa-145">Valore</span><span class="sxs-lookup"><span data-stu-id="342aa-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="342aa-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="342aa-146">Minimum supported client</span></span><br/> | <span data-ttu-id="342aa-147">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="342aa-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="342aa-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="342aa-148">Minimum supported server</span></span><br/> | <span data-ttu-id="342aa-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="342aa-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="342aa-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="342aa-150">Namespace</span></span><br/>                | <span data-ttu-id="342aa-151">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="342aa-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="342aa-152">MOF</span><span class="sxs-lookup"><span data-stu-id="342aa-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="342aa-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="342aa-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="342aa-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="342aa-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="342aa-155">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="342aa-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
