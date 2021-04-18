---
description: Scrive la chiave esterna associata alla protezione con chiave del volume specificata in un file di sistema, nascosto o di sola lettura nella cartella specificata.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Metodo SaveExternalKeyToFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314671"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d366b-103">Metodo SaveExternalKeyToFile della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="d366b-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d366b-104">Il metodo **SaveExternalKeyToFile** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) scrive la chiave esterna associata alla protezione con chiave del volume specificata in un file di sistema, nascosto o di sola lettura nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="d366b-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="d366b-105">Questo metodo è applicabile solo per le protezioni con chiave di tipo "chiave esterna" o "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="d366b-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="d366b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d366b-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="d366b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d366b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d366b-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d366b-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366b-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="d366b-109">Type: **string**</span></span>

<span data-ttu-id="d366b-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="d366b-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="d366b-111">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d366b-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366b-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="d366b-112">Type: **string**</span></span>

<span data-ttu-id="d366b-113">Stringa che contiene il percorso del volume o della cartella in cui salvare la chiave esterna associata alla protezione con chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="d366b-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="d366b-114">Questo percorso non include il nome del file, che è interno e può variare da una versione all'altra.</span><span class="sxs-lookup"><span data-stu-id="d366b-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="d366b-115">Usare **GetExternalKeyFileName** per ottenere il nome del file.</span><span class="sxs-lookup"><span data-stu-id="d366b-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d366b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d366b-116">Return value</span></span>

<span data-ttu-id="d366b-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d366b-117">Type: **uint32**</span></span>

<span data-ttu-id="d366b-118">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d366b-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d366b-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d366b-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="d366b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d366b-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d366b-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d366b-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="d366b-122">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="d366b-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="d366b-123"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="d366b-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="d366b-124">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="d366b-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="d366b-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="d366b-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="d366b-126">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave del tipo "chiave esterna" o "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="d366b-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="d366b-127"><dt>**Errore \_ PERCORSO \_ non \_ trovato**</dt> <dt>2147942403 (0 x 80070003)</dt></span><span class="sxs-lookup"><span data-stu-id="d366b-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="d366b-128">Il parametro *path* non fa riferimento a un percorso valido.</span><span class="sxs-lookup"><span data-stu-id="d366b-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="d366b-129">Verificare che il nome file non sia incluso nel parametro *path* .</span><span class="sxs-lookup"><span data-stu-id="d366b-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="d366b-130"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="d366b-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="d366b-131">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d366b-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="d366b-132">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d366b-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d366b-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="d366b-133">Remarks</span></span>

<span data-ttu-id="d366b-134">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d366b-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d366b-135">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d366b-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d366b-136">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="d366b-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d366b-137">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d366b-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d366b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d366b-138">Requirements</span></span>



| <span data-ttu-id="d366b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d366b-139">Requirement</span></span> | <span data-ttu-id="d366b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="d366b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d366b-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d366b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d366b-142">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="d366b-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d366b-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d366b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d366b-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d366b-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d366b-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d366b-145">Namespace</span></span><br/>                | <span data-ttu-id="d366b-146">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="d366b-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d366b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d366b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d366b-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d366b-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d366b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d366b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d366b-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="d366b-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
