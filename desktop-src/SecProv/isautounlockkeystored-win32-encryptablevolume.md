---
description: Indica se le chiavi esterne o le informazioni correlate che possono essere utilizzate per sbloccare automaticamente i volumi di dati sono presenti nel volume del sistema operativo attualmente in esecuzione.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Metodo IsAutoUnlockKeyStored della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316094"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ed66e-103">Metodo IsAutoUnlockKeyStored della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="ed66e-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ed66e-104">Il metodo **IsAutoUnlockKeyStored** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se sono presenti chiavi esterne o informazioni correlate che possono essere usate per sbloccare automaticamente i volumi di dati nel volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed66e-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed66e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed66e-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="ed66e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed66e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed66e-107">*IsAutoUnlockKeyStored* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed66e-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed66e-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ed66e-108">Type: **boolean**</span></span>

<span data-ttu-id="ed66e-109">È **true** se le informazioni che possono essere utilizzate per sbloccare automaticamente i volumi di dati vengono archiviate nel registro di sistema del volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed66e-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed66e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed66e-110">Return value</span></span>

<span data-ttu-id="ed66e-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed66e-111">Type: **uint32**</span></span>

<span data-ttu-id="ed66e-112">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ed66e-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ed66e-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed66e-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="ed66e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed66e-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed66e-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ed66e-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="ed66e-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ed66e-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ed66e-117"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="ed66e-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="ed66e-118">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ed66e-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="ed66e-119">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ed66e-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="ed66e-120"><dt>**FVE \_ E \_ non \_ \_ volume del sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="ed66e-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="ed66e-121">Il metodo può essere eseguito solo per il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed66e-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ed66e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed66e-122">Remarks</span></span>

<span data-ttu-id="ed66e-123">Usare [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) per rimuovere tutte le informazioni di sblocco dal volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed66e-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="ed66e-124">Le informazioni usate per sbloccare un volume vengono archiviate quando si esegue [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) per un volume di dati mentre è in esecuzione il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ed66e-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="ed66e-125">**IsAutoUnlockKeyStored** differisce da [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in quanto, anche se lo sblocco automatico è disabilitato per tutti i volumi di dati attualmente connessi al computer, potrebbero essere ancora presenti informazioni di sblocco associate a volumi di dati o volumi di dati disconnessi che non esistono più.</span><span class="sxs-lookup"><span data-stu-id="ed66e-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="ed66e-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed66e-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed66e-127">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ed66e-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ed66e-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ed66e-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed66e-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ed66e-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed66e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed66e-130">Requirements</span></span>



| <span data-ttu-id="ed66e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed66e-131">Requirement</span></span> | <span data-ttu-id="ed66e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ed66e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed66e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed66e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ed66e-134">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="ed66e-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed66e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed66e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ed66e-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed66e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed66e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed66e-137">Namespace</span></span><br/>                | <span data-ttu-id="ed66e-138">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ed66e-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ed66e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ed66e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed66e-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed66e-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed66e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed66e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed66e-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ed66e-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
