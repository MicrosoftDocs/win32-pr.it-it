---
description: Rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione che vengono utilizzate per sbloccare automaticamente i volumi di dati.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Metodo ClearAllAutoUnlockKeys della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306408"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c141c-103">Metodo ClearAllAutoUnlockKeys della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="c141c-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c141c-104">Il metodo **ClearAllAutoUnlockKeys** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione che vengono usate per sbloccare automaticamente i volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="c141c-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c141c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c141c-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="c141c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c141c-106">Parameters</span></span>

<span data-ttu-id="c141c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c141c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c141c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c141c-108">Return value</span></span>

<span data-ttu-id="c141c-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c141c-109">Type: **uint32**</span></span>

<span data-ttu-id="c141c-110">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c141c-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c141c-111">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c141c-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="c141c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c141c-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c141c-113"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c141c-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="c141c-114">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c141c-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c141c-115"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c141c-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="c141c-116">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c141c-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c141c-117">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c141c-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="c141c-118"><dt>**FVE \_ E \_ non \_ \_ volume del sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="c141c-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="c141c-119">Il metodo può essere eseguito solo per il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c141c-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c141c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c141c-120">Remarks</span></span>

<span data-ttu-id="c141c-121">**ClearAllAutoUnlockKeys** ottiene le stesse funzionalità di esecuzione di [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) per ogni volume di dati associato al sistema operativo attualmente in esecuzione, anche per i volumi di dati che non sono attualmente connessi al computer.</span><span class="sxs-lookup"><span data-stu-id="c141c-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="c141c-122">Rimuove anche eventuali informazioni di sblocco non aggiornate associate a volumi di dati che non esistono più.</span><span class="sxs-lookup"><span data-stu-id="c141c-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="c141c-123">Prima di chiamare [**Decrypt**](decrypt-win32-encryptablevolume.md) sul volume del sistema operativo attualmente in esecuzione, usare **ClearAllAutoUnlockKeys** per assicurarsi che le informazioni inserite nel registro di sistema del sistema operativo per sbloccare automaticamente i volumi di dati non siano accessibili in chiaro su disco.</span><span class="sxs-lookup"><span data-stu-id="c141c-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="c141c-124">Dopo l'esecuzione corretta di **ClearAllAutoUnlockKeys** , è possibile usare i metodi [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per sbloccare tutti i volumi di dati nel computer.</span><span class="sxs-lookup"><span data-stu-id="c141c-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="c141c-125">Usare [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) per abilitare di nuovo lo sblocco automatico di un volume di dati.</span><span class="sxs-lookup"><span data-stu-id="c141c-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="c141c-126">Se non vengono restituiti altri errori, **ClearAllAutoUnlockKeys** rimuove dal registro di sistema tutti gli ID di protezione del volume e le chiavi esterne usate per sbloccare automaticamente qualsiasi volume di dati associato al volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c141c-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="c141c-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c141c-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c141c-128">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c141c-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c141c-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c141c-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c141c-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c141c-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c141c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c141c-131">Requirements</span></span>



| <span data-ttu-id="c141c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c141c-132">Requirement</span></span> | <span data-ttu-id="c141c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c141c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c141c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c141c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c141c-135">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="c141c-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c141c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c141c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c141c-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c141c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c141c-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c141c-138">Namespace</span></span><br/>                | <span data-ttu-id="c141c-139">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c141c-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c141c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c141c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c141c-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c141c-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c141c-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c141c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c141c-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c141c-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
