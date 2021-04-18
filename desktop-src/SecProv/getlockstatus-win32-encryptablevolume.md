---
description: Indica se il contenuto del volume è accessibile da Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Metodo GetLockStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306394"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f008e-103">Metodo GetLockStatus della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="f008e-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f008e-104">Il metodo **GetLockStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il contenuto del volume è accessibile da Windows.</span><span class="sxs-lookup"><span data-stu-id="f008e-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="f008e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f008e-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f008e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f008e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f008e-107">*LockStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f008e-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f008e-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f008e-108">Type: **uint32**</span></span>

<span data-ttu-id="f008e-109">Specifica se il contenuto del volume è accessibile da Windows.</span><span class="sxs-lookup"><span data-stu-id="f008e-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="f008e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f008e-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="f008e-111">Significato</span><span class="sxs-lookup"><span data-stu-id="f008e-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="f008e-112"><dt>**Sbloccato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f008e-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="f008e-113">Per un HDD standard:</span><span class="sxs-lookup"><span data-stu-id="f008e-113">For a standard HDD:</span></span><br/> <span data-ttu-id="f008e-114">Il contenuto completo del volume è accessibile.</span><span class="sxs-lookup"><span data-stu-id="f008e-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="f008e-115">Un volume sbloccato è completamente decrittografato o la chiave di crittografia è disponibile nel disco chiaro su disco.</span><span class="sxs-lookup"><span data-stu-id="f008e-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="f008e-116">Il volume che contiene il sistema operativo attualmente in esecuzione, ad esempio il volume di Windows in esecuzione, è sempre accessibile e non può essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="f008e-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="f008e-117">Per un EHDD:</span><span class="sxs-lookup"><span data-stu-id="f008e-117">For an EHDD:</span></span><br/> <span data-ttu-id="f008e-118">La banda viene continuamente sbloccata.</span><span class="sxs-lookup"><span data-stu-id="f008e-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="f008e-119"><dt>**Bloccato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f008e-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="f008e-120">Per un HDD standard:</span><span class="sxs-lookup"><span data-stu-id="f008e-120">For a standard HDD:</span></span><br/> <span data-ttu-id="f008e-121">Tutto o una parte del contenuto del volume non sono accessibili.</span><span class="sxs-lookup"><span data-stu-id="f008e-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="f008e-122">Un volume bloccato deve essere parzialmente o completamente crittografato e non deve avere la chiave di crittografia disponibile in Clear su disco.</span><span class="sxs-lookup"><span data-stu-id="f008e-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="f008e-123">Per un EHDD:</span><span class="sxs-lookup"><span data-stu-id="f008e-123">For an EHDD:</span></span><br/> <span data-ttu-id="f008e-124">La banda è sbloccata o bloccata.</span><span class="sxs-lookup"><span data-stu-id="f008e-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f008e-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f008e-125">Return value</span></span>

<span data-ttu-id="f008e-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f008e-126">Type: **uint32**</span></span>

<span data-ttu-id="f008e-127">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f008e-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f008e-128">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f008e-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f008e-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f008e-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f008e-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f008e-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f008e-131">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f008e-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f008e-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f008e-132">Remarks</span></span>

<span data-ttu-id="f008e-133">Usare [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) e [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per ottenere l'accesso al contenuto del volume.</span><span class="sxs-lookup"><span data-stu-id="f008e-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="f008e-134">Usare il metodo [**Lock**](lock-win32-encryptablevolume.md) per abbandonare l'accesso al contenuto del volume.</span><span class="sxs-lookup"><span data-stu-id="f008e-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="f008e-135">Il volume che contiene il sistema operativo attualmente in esecuzione è sempre accessibile e non può essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="f008e-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="f008e-136">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f008e-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f008e-137">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f008e-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f008e-138">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f008e-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f008e-139">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f008e-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f008e-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f008e-140">Requirements</span></span>



| <span data-ttu-id="f008e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f008e-141">Requirement</span></span> | <span data-ttu-id="f008e-142">Valore</span><span class="sxs-lookup"><span data-stu-id="f008e-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f008e-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f008e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f008e-144">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="f008e-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f008e-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f008e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f008e-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f008e-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f008e-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f008e-147">Namespace</span></span><br/>                | <span data-ttu-id="f008e-148">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f008e-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f008e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f008e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f008e-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f008e-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f008e-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f008e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f008e-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f008e-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
