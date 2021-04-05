---
description: Consente di sbloccare automaticamente un volume di dati quando viene montato il volume.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Metodo EnableAutoUnlock della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882069"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3519a-103">Metodo EnableAutoUnlock della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="3519a-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3519a-104">Il metodo **EnableAutoUnlock** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) consente di sbloccare automaticamente un volume di dati quando viene montato il volume.</span><span class="sxs-lookup"><span data-stu-id="3519a-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="3519a-105">Lo sblocco automatico salva una chiave esterna nel sistema operativo in grado di sbloccare automaticamente il volume nel volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3519a-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="3519a-106">Per usare questo metodo, il volume del sistema operativo deve essere già protetto da Crittografia unità BitLocker o deve avere la crittografia in corso.</span><span class="sxs-lookup"><span data-stu-id="3519a-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="3519a-107">Inoltre, è necessario che esista già una chiave esterna per il volume di dati.</span><span class="sxs-lookup"><span data-stu-id="3519a-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="3519a-108">Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare la chiave esterna che può sbloccare automaticamente il volume.</span><span class="sxs-lookup"><span data-stu-id="3519a-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="3519a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3519a-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="3519a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3519a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3519a-111">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3519a-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3519a-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="3519a-112">Type: **string**</span></span>

<span data-ttu-id="3519a-113">Stringa che identifica la protezione con chiave del tipo "chiave esterna" utilizzata per sbloccare automaticamente il volume.</span><span class="sxs-lookup"><span data-stu-id="3519a-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3519a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3519a-114">Return value</span></span>

<span data-ttu-id="3519a-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3519a-115">Type: **uint32**</span></span>

<span data-ttu-id="3519a-116">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3519a-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3519a-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3519a-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="3519a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3519a-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3519a-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="3519a-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3519a-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="3519a-121"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="3519a-122">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3519a-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="3519a-123"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="3519a-124">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3519a-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3519a-125">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3519a-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="3519a-126"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="3519a-127">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave valida del tipo "External Key".</span><span class="sxs-lookup"><span data-stu-id="3519a-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="3519a-128"><dt>**FVE \_ E \_ non \_ il \_ VOLUME di dati**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="3519a-129">Impossibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3519a-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="3519a-130"><dt>**FVE \_ \_Sistema operativo E \_ non \_ protetto**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="3519a-131">Il metodo non può essere eseguito se il volume del sistema operativo attualmente in esecuzione non è protetto da Crittografia unità BitLocker o se la crittografia non è in corso.</span><span class="sxs-lookup"><span data-stu-id="3519a-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="3519a-132"><dt> **FVE \_ E \_ volume \_ binding \_ già**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="3519a-133">Lo sblocco automatico sul volume è stato precedentemente abilitato.</span><span class="sxs-lookup"><span data-stu-id="3519a-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3519a-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="3519a-134">Remarks</span></span>

<span data-ttu-id="3519a-135">Data una protezione con chiave del volume valida del tipo "chiave esterna", la chiave esterna a 256 bit correlata viene estratta dalla protezione e archiviata nel registro di sistema del sistema operativo attualmente in esecuzione, insieme all'ID della protezione con chiave del volume.</span><span class="sxs-lookup"><span data-stu-id="3519a-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="3519a-136">Se la chiave esterna associata all'ID della protezione con chiave del volume viene eliminata, la funzionalità di sblocco automatico del volume viene disabilitata o sospesa.</span><span class="sxs-lookup"><span data-stu-id="3519a-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="3519a-137">I supporti rimovibili non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="3519a-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="3519a-138">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3519a-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3519a-139">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3519a-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3519a-140">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3519a-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3519a-141">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3519a-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3519a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3519a-142">Requirements</span></span>



| <span data-ttu-id="3519a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3519a-143">Requirement</span></span> | <span data-ttu-id="3519a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="3519a-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3519a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3519a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3519a-146">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="3519a-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3519a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3519a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3519a-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3519a-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3519a-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3519a-149">Namespace</span></span><br/>                | <span data-ttu-id="3519a-150">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="3519a-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3519a-151">MOF</span><span class="sxs-lookup"><span data-stu-id="3519a-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3519a-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3519a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3519a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3519a-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="3519a-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
