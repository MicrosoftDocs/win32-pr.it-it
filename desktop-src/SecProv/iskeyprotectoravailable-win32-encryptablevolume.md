---
description: Indica se sono disponibili protezioni per il volume.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Metodo IsKeyProtectorAvailable della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226006"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3c43a-103">Metodo IsKeyProtectorAvailable della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="3c43a-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3c43a-104">Il metodo **IsKeyProtectorAvailable** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se sono disponibili protezioni per il volume.</span><span class="sxs-lookup"><span data-stu-id="3c43a-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="3c43a-105">Se viene fornito un tipo di protezione, il metodo indica se sono disponibili protezioni del tipo specificato per il volume.</span><span class="sxs-lookup"><span data-stu-id="3c43a-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c43a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c43a-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="3c43a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c43a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c43a-108">*KeyProtectorType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c43a-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c43a-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c43a-109">Type: **uint32**</span></span>

<span data-ttu-id="3c43a-110">Unsigned Integer che indica il tipo di protezione con chiave del volume sottoposto a query.</span><span class="sxs-lookup"><span data-stu-id="3c43a-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="3c43a-111">Se questo parametro non viene specificato, vengono eseguite query su tutte le protezioni con chiave disponibili del volume.</span><span class="sxs-lookup"><span data-stu-id="3c43a-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="3c43a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3c43a-112">Value</span></span>                                                                         | <span data-ttu-id="3c43a-113">Significato</span><span class="sxs-lookup"><span data-stu-id="3c43a-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c43a-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="3c43a-115">Tutti i tipi.</span><span class="sxs-lookup"><span data-stu-id="3c43a-115">All types.</span></span><br/> <span data-ttu-id="3c43a-116">Viene eseguita una query su tutte le protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="3c43a-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="3c43a-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="3c43a-118">Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="3c43a-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="3c43a-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="3c43a-120">Chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="3c43a-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="3c43a-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="3c43a-122">Password numerica.</span><span class="sxs-lookup"><span data-stu-id="3c43a-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3c43a-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="3c43a-124">TPM e PIN.</span><span class="sxs-lookup"><span data-stu-id="3c43a-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="3c43a-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="3c43a-126">TPM e chiave di avvio.</span><span class="sxs-lookup"><span data-stu-id="3c43a-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="3c43a-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="3c43a-128">TPM, PIN e chiave di avvio.</span><span class="sxs-lookup"><span data-stu-id="3c43a-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="3c43a-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="3c43a-130">Chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="3c43a-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="3c43a-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="3c43a-132">Passphrase.</span><span class="sxs-lookup"><span data-stu-id="3c43a-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="3c43a-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="3c43a-134">Certificato TPM</span><span class="sxs-lookup"><span data-stu-id="3c43a-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="3c43a-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="3c43a-136">ID di sicurezza (SID)</span><span class="sxs-lookup"><span data-stu-id="3c43a-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="3c43a-137">*IsKeyProtectorAvailable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c43a-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c43a-138">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3c43a-138">Type: **boolean**</span></span>

<span data-ttu-id="3c43a-139">Valore booleano che indica se una protezione con chiave del volume del tipo specificato esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="3c43a-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c43a-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c43a-140">Return value</span></span>

<span data-ttu-id="3c43a-141">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c43a-141">Type: **uint32**</span></span>

<span data-ttu-id="3c43a-142">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3c43a-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3c43a-143">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c43a-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="3c43a-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c43a-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c43a-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="3c43a-146">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3c43a-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="3c43a-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="3c43a-148">Il parametro *KeyProtectorType* è specificato ma non fa riferimento a un tipo di protezione con chiave valido.</span><span class="sxs-lookup"><span data-stu-id="3c43a-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c43a-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c43a-149">Remarks</span></span>

<span data-ttu-id="3c43a-150">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3c43a-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c43a-151">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3c43a-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3c43a-152">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3c43a-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c43a-153">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3c43a-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c43a-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c43a-154">Requirements</span></span>



| <span data-ttu-id="3c43a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c43a-155">Requirement</span></span> | <span data-ttu-id="3c43a-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3c43a-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c43a-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c43a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3c43a-158">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="3c43a-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c43a-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c43a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3c43a-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c43a-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c43a-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c43a-161">Namespace</span></span><br/>                | <span data-ttu-id="3c43a-162">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="3c43a-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3c43a-163">MOF</span><span class="sxs-lookup"><span data-stu-id="3c43a-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c43a-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c43a-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c43a-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c43a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c43a-166">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="3c43a-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
