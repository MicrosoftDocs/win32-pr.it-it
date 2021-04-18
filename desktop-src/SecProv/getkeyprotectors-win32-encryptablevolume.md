---
description: Elenca le protezioni utilizzate per proteggere la chiave di crittografia del volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Metodo GetKeyProtectors della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306395"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="88c34-103">Metodo GetKeyProtectors della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="88c34-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="88c34-104">Il metodo **GetKeyProtectors** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) elenca le protezioni usate per proteggere la chiave di crittografia del volume.</span><span class="sxs-lookup"><span data-stu-id="88c34-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="88c34-105">Se viene fornito un tipo di protezione, vengono restituite solo le protezioni con chiave del volume del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="88c34-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c34-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88c34-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="88c34-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="88c34-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88c34-108">*KeyProtectorType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="88c34-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88c34-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88c34-109">Type: **uint32**</span></span>

<span data-ttu-id="88c34-110">Unsigned Integer che specifica il tipo di protezione con chiave da restituire.</span><span class="sxs-lookup"><span data-stu-id="88c34-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="88c34-111">Se questo parametro non viene specificato, vengono restituite tutte le protezioni con chiave disponibili del volume.</span><span class="sxs-lookup"><span data-stu-id="88c34-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="88c34-112">Valore</span><span class="sxs-lookup"><span data-stu-id="88c34-112">Value</span></span>                                                                         | <span data-ttu-id="88c34-113">Significato</span><span class="sxs-lookup"><span data-stu-id="88c34-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="88c34-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="88c34-115">Tutti i tipi.</span><span class="sxs-lookup"><span data-stu-id="88c34-115">All types.</span></span><br/> <span data-ttu-id="88c34-116">Vengono restituite tutte le protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="88c34-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="88c34-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="88c34-118">Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="88c34-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="88c34-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="88c34-120">Chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="88c34-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="88c34-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="88c34-122">Password numerica.</span><span class="sxs-lookup"><span data-stu-id="88c34-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="88c34-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="88c34-124">TPM e PIN.</span><span class="sxs-lookup"><span data-stu-id="88c34-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="88c34-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="88c34-126">TPM e chiave di avvio.</span><span class="sxs-lookup"><span data-stu-id="88c34-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="88c34-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="88c34-128">TPM, PIN e chiave di avvio.</span><span class="sxs-lookup"><span data-stu-id="88c34-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="88c34-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="88c34-130">Chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="88c34-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="88c34-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="88c34-132">Passphrase.</span><span class="sxs-lookup"><span data-stu-id="88c34-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="88c34-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="88c34-134">Certificato TPM</span><span class="sxs-lookup"><span data-stu-id="88c34-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="88c34-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="88c34-136">ID di sicurezza (SID)</span><span class="sxs-lookup"><span data-stu-id="88c34-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="88c34-137">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="88c34-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88c34-138">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="88c34-138">Type: **string\[\]**</span></span>

<span data-ttu-id="88c34-139">Matrice di stringhe che identificano le protezioni con chiave utilizzate per proteggere la chiave di crittografia del volume.</span><span class="sxs-lookup"><span data-stu-id="88c34-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88c34-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88c34-140">Return value</span></span>

<span data-ttu-id="88c34-141">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="88c34-141">Type: **uint32**</span></span>

<span data-ttu-id="88c34-142">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="88c34-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="88c34-143">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="88c34-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="88c34-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88c34-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88c34-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="88c34-146">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="88c34-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="88c34-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="88c34-148">Il parametro *VolumeKeyProtectorID* è specificato ma non fa riferimento a un *KeyProtectorType* valido.</span><span class="sxs-lookup"><span data-stu-id="88c34-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="88c34-149"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="88c34-150">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="88c34-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="88c34-151">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="88c34-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="88c34-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="88c34-152">Remarks</span></span>

<span data-ttu-id="88c34-153">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="88c34-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="88c34-154">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="88c34-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="88c34-155">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="88c34-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="88c34-156">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="88c34-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88c34-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88c34-157">Requirements</span></span>



| <span data-ttu-id="88c34-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c34-158">Requirement</span></span> | <span data-ttu-id="88c34-159">Valore</span><span class="sxs-lookup"><span data-stu-id="88c34-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c34-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88c34-160">Minimum supported client</span></span><br/> | <span data-ttu-id="88c34-161">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="88c34-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="88c34-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88c34-162">Minimum supported server</span></span><br/> | <span data-ttu-id="88c34-163">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88c34-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="88c34-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88c34-164">Namespace</span></span><br/>                | <span data-ttu-id="88c34-165">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="88c34-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="88c34-166">MOF</span><span class="sxs-lookup"><span data-stu-id="88c34-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88c34-167"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88c34-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c34-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88c34-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c34-169">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="88c34-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
