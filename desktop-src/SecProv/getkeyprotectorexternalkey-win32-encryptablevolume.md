---
description: Recupera la chiave esterna per una protezione con chiave specificata.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Metodo GetKeyProtectorExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226009"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5aaf0-103">Metodo GetKeyProtectorExternalKey della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="5aaf0-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5aaf0-104">Il metodo **GetKeyProtectorExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera la chiave esterna per una protezione con chiave specificata del tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="5aaf0-105">L'identificatore di protezione con chiave deve fare riferimento a una protezione con chiave di tipo "chiave esterna", "TPM, PIN e chiave di avvio" oppure "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="5aaf0-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="5aaf0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5aaf0-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="5aaf0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5aaf0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aaf0-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aaf0-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaf0-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="5aaf0-109">Type: **string**</span></span>

<span data-ttu-id="5aaf0-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="5aaf0-111">*ExternalKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5aaf0-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aaf0-112">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5aaf0-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="5aaf0-113">Matrice di byte che specifica la chiave esterna a 256 bit che può essere utilizzata per sbloccare il volume corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aaf0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5aaf0-114">Return value</span></span>

<span data-ttu-id="5aaf0-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5aaf0-115">Type: **uint32**</span></span>

<span data-ttu-id="5aaf0-116">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5aaf0-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5aaf0-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="5aaf0-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5aaf0-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5aaf0-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf0-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="5aaf0-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="5aaf0-121"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf0-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="5aaf0-122">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="5aaf0-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf0-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="5aaf0-124">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "chiave esterna", "TPM, pin e chiave di avvio" oppure "TPM e chiave di avvio".</span><span class="sxs-lookup"><span data-stu-id="5aaf0-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="5aaf0-125"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf0-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="5aaf0-126">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="5aaf0-127">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="5aaf0-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5aaf0-128">Remarks</span></span>

<span data-ttu-id="5aaf0-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5aaf0-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5aaf0-130">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5aaf0-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5aaf0-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5aaf0-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5aaf0-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aaf0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5aaf0-133">Requirements</span></span>



| <span data-ttu-id="5aaf0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aaf0-134">Requirement</span></span> | <span data-ttu-id="5aaf0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5aaf0-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aaf0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5aaf0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5aaf0-137">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="5aaf0-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5aaf0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5aaf0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5aaf0-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5aaf0-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5aaf0-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5aaf0-140">Namespace</span></span><br/>                | <span data-ttu-id="5aaf0-141">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5aaf0-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5aaf0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5aaf0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aaf0-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aaf0-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aaf0-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5aaf0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aaf0-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5aaf0-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
