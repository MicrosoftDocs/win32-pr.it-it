---
description: Restituisce la versione dei metadati FVE del volume.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Metodo GetVersion della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306390"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9c2e9-103">Metodo GetVersion della classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="9c2e9-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9c2e9-104">Il metodo **GetVersion** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) restituisce la versione dei metadati FVE del volume.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c2e9-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="9c2e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c2e9-107">*Versione* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9c2e9-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2e9-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c2e9-108">Type: **uint32**</span></span>

<span data-ttu-id="9c2e9-109">Unsigned Integer che indica la versione dei metadati del volume.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="9c2e9-110">Valore</span><span class="sxs-lookup"><span data-stu-id="9c2e9-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="9c2e9-111">Significato</span><span class="sxs-lookup"><span data-stu-id="9c2e9-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9c2e9-112"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="9c2e9-113">Il sistema operativo è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="9c2e9-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="9c2e9-115">Formato di Windows Vista, che significa che il volume è stato protetto con BitLocker in un computer in cui è in esecuzione Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="9c2e9-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="9c2e9-117">Formato Windows 7, ovvero il volume è stato protetto con BitLocker in un computer che esegue Windows 7 o il formato dei metadati è stato aggiornato tramite il metodo [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="9c2e9-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c2e9-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c2e9-118">Return value</span></span>

<span data-ttu-id="9c2e9-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9c2e9-119">Type: **uint32**</span></span>

<span data-ttu-id="9c2e9-120">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="9c2e9-121">Se il volume è già sbloccato e non si verificano altri errori, questo metodo restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="9c2e9-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c2e9-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="9c2e9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c2e9-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="9c2e9-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="9c2e9-125">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="9c2e9-126"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="9c2e9-127">Il valore del parametro *Version* non è valido.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="9c2e9-128"><dt>**Errore \_ \_Data 13 non valida**</dt> <dt>(0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="9c2e9-129">Il driver ha restituito un formato di dati non supportato.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="9c2e9-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c2e9-130">Remarks</span></span>

<span data-ttu-id="9c2e9-131">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9c2e9-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9c2e9-132">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9c2e9-133">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9c2e9-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9c2e9-134">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9c2e9-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2e9-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c2e9-135">Requirements</span></span>



| <span data-ttu-id="9c2e9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c2e9-136">Requirement</span></span> | <span data-ttu-id="9c2e9-137">Valore</span><span class="sxs-lookup"><span data-stu-id="9c2e9-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2e9-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c2e9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9c2e9-139">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="9c2e9-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c2e9-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c2e9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9c2e9-141">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c2e9-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c2e9-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9c2e9-142">Namespace</span></span><br/>                | <span data-ttu-id="9c2e9-143">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="9c2e9-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9c2e9-144">MOF</span><span class="sxs-lookup"><span data-stu-id="9c2e9-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c2e9-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c2e9-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c2e9-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c2e9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2e9-147">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="9c2e9-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
