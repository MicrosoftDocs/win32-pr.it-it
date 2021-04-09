---
description: Aggiorna un volume dal formato Windows Vista al formato Windows 7.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Metodo UpgradeVolume della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966582"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="31ab4-103">Metodo UpgradeVolume della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="31ab4-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="31ab4-104">Il metodo **UpgradeVolume** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) aggiorna un volume dal formato Windows Vista al formato Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31ab4-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="31ab4-105">Si tratta di un'operazione non reversibile.</span><span class="sxs-lookup"><span data-stu-id="31ab4-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ab4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31ab4-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="31ab4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="31ab4-107">Parameters</span></span>

<span data-ttu-id="31ab4-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="31ab4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31ab4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31ab4-109">Return value</span></span>

<span data-ttu-id="31ab4-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31ab4-110">Type: **uint32**</span></span>

<span data-ttu-id="31ab4-111">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="31ab4-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="31ab4-112">Se il volume è già sbloccato e non si verificano altri errori, questo metodo restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="31ab4-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="31ab4-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="31ab4-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="31ab4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31ab4-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31ab4-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="31ab4-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="31ab4-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="31ab4-117"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="31ab4-118">Uno o più argomenti non sono validi.</span><span class="sxs-lookup"><span data-stu-id="31ab4-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="31ab4-119"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="31ab4-120">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="31ab4-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="31ab4-121"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="31ab4-122">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="31ab4-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="31ab4-123">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="31ab4-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="31ab4-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="31ab4-124">Remarks</span></span>

<span data-ttu-id="31ab4-125">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="31ab4-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="31ab4-126">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="31ab4-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="31ab4-127">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="31ab4-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="31ab4-128">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="31ab4-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31ab4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31ab4-129">Requirements</span></span>



| <span data-ttu-id="31ab4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="31ab4-130">Requirement</span></span> | <span data-ttu-id="31ab4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="31ab4-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ab4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31ab4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="31ab4-133">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="31ab4-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="31ab4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31ab4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="31ab4-135">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="31ab4-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31ab4-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31ab4-136">Namespace</span></span><br/>                | <span data-ttu-id="31ab4-137">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="31ab4-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="31ab4-138">MOF</span><span class="sxs-lookup"><span data-stu-id="31ab4-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31ab4-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31ab4-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31ab4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31ab4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ab4-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="31ab4-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
