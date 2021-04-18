---
description: Elimina tutte le protezioni con chiave per il volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Metodo DeleteKeyProtectors della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312765"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b23dc-103">Metodo DeleteKeyProtectors della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b23dc-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b23dc-104">Il metodo **DeleteKeyProtectors** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Elimina tutte le protezioni con chiave per il volume.</span><span class="sxs-lookup"><span data-stu-id="b23dc-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="b23dc-105">Se un volume non crittografato dispone di protezioni con chiave, quando **DeleteKeyProtectors** viene eseguito correttamente, il volume ripristina un file system NTFS standard.</span><span class="sxs-lookup"><span data-stu-id="b23dc-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="b23dc-106">Se il volume non è ancora completamente decrittografato, usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di eseguire **DeleteKeyProtectors** per assicurarsi che le parti crittografate del volume rimangano accessibili.</span><span class="sxs-lookup"><span data-stu-id="b23dc-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23dc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b23dc-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="b23dc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b23dc-108">Parameters</span></span>

<span data-ttu-id="b23dc-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b23dc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b23dc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b23dc-110">Return value</span></span>

<span data-ttu-id="b23dc-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b23dc-111">Type: **uint32**</span></span>

<span data-ttu-id="b23dc-112">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b23dc-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b23dc-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b23dc-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="b23dc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b23dc-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b23dc-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b23dc-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="b23dc-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b23dc-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="b23dc-117"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b23dc-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="b23dc-118">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b23dc-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b23dc-119"><dt>**FVE \_ \_Chiave E \_ obbligatoria**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="b23dc-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="b23dc-120">Non è possibile rimuovere l'ultima protezione con chiave per un volume parzialmente o completamente crittografato se sono abilitate le protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="b23dc-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="b23dc-121">Usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di rimuovere l'ultima protezione con chiave per assicurarsi che le parti crittografate del volume rimangano accessibili.</span><span class="sxs-lookup"><span data-stu-id="b23dc-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="b23dc-122"><dt>**FVE \_ E \_ \_ con binding VOLUME \_ già**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="b23dc-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="b23dc-123">Non è possibile eliminare le protezioni con chiave perché uno di essi è usato per sbloccare automaticamente il volume.</span><span class="sxs-lookup"><span data-stu-id="b23dc-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="b23dc-124">Usare [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) per disabilitare lo sblocco automatico prima di eseguire questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b23dc-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b23dc-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b23dc-125">Remarks</span></span>

<span data-ttu-id="b23dc-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b23dc-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b23dc-127">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b23dc-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b23dc-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b23dc-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b23dc-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b23dc-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b23dc-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b23dc-130">Requirements</span></span>



| <span data-ttu-id="b23dc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b23dc-131">Requirement</span></span> | <span data-ttu-id="b23dc-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b23dc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b23dc-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b23dc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b23dc-134">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="b23dc-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b23dc-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b23dc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b23dc-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b23dc-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b23dc-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b23dc-137">Namespace</span></span><br/>                | <span data-ttu-id="b23dc-138">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b23dc-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b23dc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b23dc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b23dc-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b23dc-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b23dc-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b23dc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23dc-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b23dc-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
