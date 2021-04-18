---
description: Indica se il volume viene sbloccato automaticamente quando viene montato.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Metodo IsAutoUnlockEnabled della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306389"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f9c62-103">Metodo IsAutoUnlockEnabled della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="f9c62-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f9c62-104">Il metodo **IsAutoUnlockEnabled** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il volume viene sbloccato automaticamente quando viene montato, ad esempio quando i dispositivi di memoria rimovibili sono connessi al computer.</span><span class="sxs-lookup"><span data-stu-id="f9c62-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c62-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9c62-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="f9c62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9c62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c62-107">*IsAutoUnlockEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9c62-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c62-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f9c62-108">Type: **boolean**</span></span>

<span data-ttu-id="f9c62-109">Valore booleano che è true se la chiave esterna utilizzata per sbloccare automaticamente il volume esiste ed è stata archiviata nel volume del sistema operativo attualmente in esecuzione; in caso contrario, è false.</span><span class="sxs-lookup"><span data-stu-id="f9c62-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="f9c62-110">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9c62-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c62-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="f9c62-111">Type: **string**</span></span>

<span data-ttu-id="f9c62-112">Identificatore di stringa univoco che contiene l'ID della protezione con chiave del volume crittografato associato se *IsAutoUnlockEnabled* è true.</span><span class="sxs-lookup"><span data-stu-id="f9c62-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="f9c62-113">Se *IsAutoUnlockEnabled* è false, *VolumeKeyProtectorID* è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="f9c62-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c62-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9c62-114">Return value</span></span>

<span data-ttu-id="f9c62-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9c62-115">Type: **uint32**</span></span>

<span data-ttu-id="f9c62-116">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f9c62-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f9c62-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9c62-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="f9c62-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9c62-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9c62-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f9c62-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="f9c62-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f9c62-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f9c62-121"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f9c62-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="f9c62-122">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f9c62-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f9c62-123">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f9c62-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="f9c62-124"><dt>**FVE \_ E \_ non \_ il \_ VOLUME di dati**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="f9c62-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="f9c62-125">Impossibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f9c62-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f9c62-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9c62-126">Remarks</span></span>

<span data-ttu-id="f9c62-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9c62-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9c62-128">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f9c62-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f9c62-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f9c62-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9c62-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f9c62-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c62-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9c62-131">Requirements</span></span>



| <span data-ttu-id="f9c62-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9c62-132">Requirement</span></span> | <span data-ttu-id="f9c62-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f9c62-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c62-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9c62-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c62-135">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="f9c62-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f9c62-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9c62-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c62-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9c62-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9c62-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9c62-138">Namespace</span></span><br/>                | <span data-ttu-id="f9c62-139">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f9c62-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f9c62-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f9c62-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9c62-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9c62-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c62-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9c62-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c62-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f9c62-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
