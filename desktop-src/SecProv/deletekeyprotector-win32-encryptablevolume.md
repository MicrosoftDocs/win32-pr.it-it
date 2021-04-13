---
description: Elimina una protezione con chiave specificata per il volume.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Metodo DeleteKeyProtector della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343076"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b88de-103">Metodo DeleteKeyProtector della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b88de-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b88de-104">Il metodo **DeleteKeyProtector** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Elimina una determinata protezione con chiave per il volume.</span><span class="sxs-lookup"><span data-stu-id="b88de-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="b88de-105">Se un volume non crittografato dispone di protezioni con chiave, quando **DeleteKeyProtector** rimuove l'ultima protezione con chiave, il volume ripristina un file system NTFS standard.</span><span class="sxs-lookup"><span data-stu-id="b88de-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="b88de-106">Se un volume non è mai stato crittografato, l'eliminazione della protezione con chiave verrà ripristinata in NTFS.</span><span class="sxs-lookup"><span data-stu-id="b88de-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="b88de-107">Se il volume non è ancora completamente decrittografato, usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di rimuovere l'ultima protezione con chiave del volume per assicurarsi che le parti crittografate del volume rimangano accessibili.</span><span class="sxs-lookup"><span data-stu-id="b88de-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88de-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b88de-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="b88de-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b88de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88de-110">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b88de-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88de-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="b88de-111">Type: **string**</span></span>

<span data-ttu-id="b88de-112">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="b88de-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88de-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b88de-113">Return value</span></span>

<span data-ttu-id="b88de-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b88de-114">Type: **uint32**</span></span>

<span data-ttu-id="b88de-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b88de-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b88de-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b88de-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="b88de-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b88de-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b88de-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="b88de-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b88de-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="b88de-120"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="b88de-121">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b88de-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b88de-122"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="b88de-123">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b88de-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b88de-124">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b88de-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="b88de-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="b88de-126">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave valida.</span><span class="sxs-lookup"><span data-stu-id="b88de-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="b88de-127"><dt>**FVE \_ \_Chiave E \_ obbligatoria**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="b88de-128">Non è possibile rimuovere l'ultima protezione con chiave per un volume parzialmente o completamente crittografato se sono abilitate le protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="b88de-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="b88de-129">Usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di rimuovere l'ultima protezione con chiave per assicurarsi che le parti crittografate del volume rimangano accessibili.</span><span class="sxs-lookup"><span data-stu-id="b88de-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="b88de-130"><dt>**FVE \_ E \_ \_ con binding VOLUME \_ già**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="b88de-131">Questa protezione con chiave non può essere eliminata perché viene usata per sbloccare automaticamente il volume.</span><span class="sxs-lookup"><span data-stu-id="b88de-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="b88de-132">Usare [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) per disabilitare lo sblocco automatico prima di eliminare questa protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="b88de-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b88de-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="b88de-133">Remarks</span></span>

<span data-ttu-id="b88de-134">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b88de-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b88de-135">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b88de-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b88de-136">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b88de-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b88de-137">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b88de-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b88de-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b88de-138">Requirements</span></span>



| <span data-ttu-id="b88de-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88de-139">Requirement</span></span> | <span data-ttu-id="b88de-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b88de-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88de-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88de-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b88de-142">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="b88de-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b88de-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b88de-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b88de-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b88de-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b88de-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b88de-145">Namespace</span></span><br/>                | <span data-ttu-id="b88de-146">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b88de-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b88de-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b88de-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b88de-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b88de-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88de-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b88de-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88de-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b88de-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
