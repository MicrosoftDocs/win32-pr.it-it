---
description: Restituisce il nome del file che contiene la chiave esterna.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Metodo GetExternalKeyFileName della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306403"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f5dc2-103">Metodo GetExternalKeyFileName della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="f5dc2-103">GetExternalKeyFileName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f5dc2-104">Il metodo **GetExternalKeyFileName** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) restituisce il nome del file che contiene la chiave esterna, se questa chiave esterna viene salvata in un percorso di file usando il metodo [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="f5dc2-104">The **GetExternalKeyFileName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the name of the file that contains the external key, if this external key is saved to a file location by using the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="f5dc2-105">Questo metodo è applicabile solo per le protezioni con chiave di tipo "chiave esterna", "TPM, PIN e chiave di avvio" oppure "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="f5dc2-105">This method is only applicable for key protectors of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="f5dc2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5dc2-106">Syntax</span></span>


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="f5dc2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5dc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5dc2-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5dc2-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5dc2-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="f5dc2-109">Type: **string**</span></span>

<span data-ttu-id="f5dc2-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="f5dc2-111">*Nome file* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f5dc2-111">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5dc2-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="f5dc2-112">Type: **string**</span></span>

<span data-ttu-id="f5dc2-113">Stringa che specifica il nome con estensione, ma senza il percorso del file, del file che contiene la chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-113">A string that specifies the name with extension but without the file path, of the file that contains the external key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5dc2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5dc2-114">Return value</span></span>

<span data-ttu-id="f5dc2-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5dc2-115">Type: **uint32**</span></span>

<span data-ttu-id="f5dc2-116">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f5dc2-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5dc2-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f5dc2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5dc2-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5dc2-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc2-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f5dc2-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="f5dc2-121"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc2-121"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="f5dc2-122">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "chiave esterna", "TPM, pin e chiave di avvio" oppure "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="f5dc2-122">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="f5dc2-123"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc2-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f5dc2-124">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-124">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="f5dc2-125"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc2-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="f5dc2-126">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f5dc2-127">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="f5dc2-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5dc2-128">Remarks</span></span>

<span data-ttu-id="f5dc2-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5dc2-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5dc2-130">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f5dc2-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f5dc2-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5dc2-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f5dc2-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5dc2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5dc2-133">Requirements</span></span>



| <span data-ttu-id="f5dc2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5dc2-134">Requirement</span></span> | <span data-ttu-id="f5dc2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f5dc2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5dc2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5dc2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f5dc2-137">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="f5dc2-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f5dc2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5dc2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f5dc2-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5dc2-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5dc2-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5dc2-140">Namespace</span></span><br/>                | <span data-ttu-id="f5dc2-141">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f5dc2-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f5dc2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f5dc2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5dc2-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5dc2-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5dc2-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5dc2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5dc2-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f5dc2-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="f5dc2-146">**SaveExternalKeyToFile**</span><span class="sxs-lookup"><span data-stu-id="f5dc2-146">**SaveExternalKeyToFile**</span></span>](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 
