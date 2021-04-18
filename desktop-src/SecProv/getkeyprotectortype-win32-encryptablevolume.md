---
description: Indica il tipo di una protezione con chiave specificata.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Metodo GetKeyProtectorType della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529785"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="562bb-103">Metodo GetKeyProtectorType della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="562bb-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="562bb-104">Il metodo **GetKeyProtectorType** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica il tipo di una protezione con chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="562bb-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="562bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="562bb-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="562bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="562bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="562bb-107">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="562bb-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562bb-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="562bb-108">Type: **string**</span></span>

<span data-ttu-id="562bb-109">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="562bb-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="562bb-110">*KeyProtectorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="562bb-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="562bb-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="562bb-111">Type: **uint32**</span></span>

<span data-ttu-id="562bb-112">Unsigned Integer che specifica il tipo della protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="562bb-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="562bb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="562bb-113">Value</span></span>                                                                         | <span data-ttu-id="562bb-114">Significato</span><span class="sxs-lookup"><span data-stu-id="562bb-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="562bb-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="562bb-116">Tipo di protezione sconosciuto o altro</span><span class="sxs-lookup"><span data-stu-id="562bb-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="562bb-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="562bb-118">TPM (Trusted Platform Module)</span><span class="sxs-lookup"><span data-stu-id="562bb-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="562bb-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="562bb-120">Chiave esterna</span><span class="sxs-lookup"><span data-stu-id="562bb-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="562bb-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="562bb-122">Password numerica</span><span class="sxs-lookup"><span data-stu-id="562bb-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="562bb-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="562bb-124">TPM e PIN</span><span class="sxs-lookup"><span data-stu-id="562bb-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="562bb-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="562bb-126">TPM e chiave di avvio</span><span class="sxs-lookup"><span data-stu-id="562bb-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="562bb-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="562bb-128">TPM, PIN e chiave di avvio</span><span class="sxs-lookup"><span data-stu-id="562bb-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="562bb-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="562bb-130">Chiave pubblica</span><span class="sxs-lookup"><span data-stu-id="562bb-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="562bb-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="562bb-132">Passphrase</span><span class="sxs-lookup"><span data-stu-id="562bb-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="562bb-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="562bb-134">Certificato TPM</span><span class="sxs-lookup"><span data-stu-id="562bb-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="562bb-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="562bb-136">Protezione CNG (CryptoAPI Next Generation)</span><span class="sxs-lookup"><span data-stu-id="562bb-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="562bb-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="562bb-137">Return value</span></span>

<span data-ttu-id="562bb-138">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="562bb-138">Type: **uint32**</span></span>

<span data-ttu-id="562bb-139">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="562bb-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="562bb-140">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="562bb-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="562bb-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="562bb-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="562bb-142"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="562bb-143">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="562bb-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="562bb-144"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="562bb-145">Il parametro *VolumeKeyProtectorID* non fa riferimento a un *KeyProtectorType* valido.</span><span class="sxs-lookup"><span data-stu-id="562bb-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="562bb-146"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="562bb-147">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="562bb-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="562bb-148">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="562bb-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="562bb-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="562bb-149">Remarks</span></span>

<span data-ttu-id="562bb-150">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="562bb-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="562bb-151">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="562bb-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="562bb-152">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="562bb-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="562bb-153">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="562bb-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="562bb-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="562bb-154">Requirements</span></span>



| <span data-ttu-id="562bb-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="562bb-155">Requirement</span></span> | <span data-ttu-id="562bb-156">Valore</span><span class="sxs-lookup"><span data-stu-id="562bb-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="562bb-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="562bb-157">Minimum supported client</span></span><br/> | <span data-ttu-id="562bb-158">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="562bb-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="562bb-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="562bb-159">Minimum supported server</span></span><br/> | <span data-ttu-id="562bb-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="562bb-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="562bb-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="562bb-161">Namespace</span></span><br/>                | <span data-ttu-id="562bb-162">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="562bb-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="562bb-163">MOF</span><span class="sxs-lookup"><span data-stu-id="562bb-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="562bb-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="562bb-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562bb-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="562bb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562bb-166">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="562bb-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
