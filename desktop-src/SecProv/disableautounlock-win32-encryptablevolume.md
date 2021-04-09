---
description: Rimuove la chiave esterna salvata nel volume del sistema operativo attualmente in esecuzione.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Metodo DisableAutoUnlock della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882078"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f9847-103">Metodo DisableAutoUnlock della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="f9847-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f9847-104">Il metodo **DisableAutoUnlock** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) rimuove la chiave esterna salvata nel volume del sistema operativo attualmente in esecuzione, in modo che un volume di dati non venga sbloccato automaticamente quando viene montato, ad esempio quando i dispositivi di memoria rimovibili sono connessi al computer.</span><span class="sxs-lookup"><span data-stu-id="f9847-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="f9847-105">Se lo sblocco automatico è disabilitato o sospeso, è necessario utilizzare i metodi [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="f9847-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9847-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9847-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="f9847-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9847-107">Parameters</span></span>

<span data-ttu-id="f9847-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f9847-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9847-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9847-109">Return value</span></span>

<span data-ttu-id="f9847-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9847-110">Type: **uint32**</span></span>

<span data-ttu-id="f9847-111">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f9847-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f9847-112">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9847-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f9847-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9847-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9847-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f9847-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="f9847-115">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f9847-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f9847-116"><dt> **FVE \_ E \_ volume \_ non \_ associato**</dt> <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="f9847-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="f9847-117">Lo sblocco automatico sul volume è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f9847-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f9847-118"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f9847-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="f9847-119">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f9847-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f9847-120">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f9847-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="f9847-121"><dt>**FVE \_ E \_ non \_ il \_ VOLUME di dati**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="f9847-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="f9847-122">Impossibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f9847-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f9847-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9847-123">Remarks</span></span>

<span data-ttu-id="f9847-124">Se non vengono restituiti errori, questo metodo rimuove dal registro di sistema tutti gli ID di protezione del volume e le chiavi esterne usate per sbloccare automaticamente il volume.</span><span class="sxs-lookup"><span data-stu-id="f9847-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="f9847-125">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9847-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9847-126">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f9847-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f9847-127">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f9847-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9847-128">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f9847-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9847-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9847-129">Requirements</span></span>



| <span data-ttu-id="f9847-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9847-130">Requirement</span></span> | <span data-ttu-id="f9847-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f9847-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9847-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9847-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f9847-133">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="f9847-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f9847-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9847-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f9847-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9847-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9847-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9847-136">Namespace</span></span><br/>                | <span data-ttu-id="f9847-137">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f9847-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f9847-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f9847-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9847-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9847-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9847-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9847-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9847-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f9847-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
