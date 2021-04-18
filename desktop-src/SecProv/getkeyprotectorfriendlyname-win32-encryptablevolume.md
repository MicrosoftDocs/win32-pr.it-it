---
description: Recupera il nome visualizzato utilizzato per identificare una protezione con chiave specificata.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Metodo GetKeyProtectorFriendlyName della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316106"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="752d0-103">Metodo GetKeyProtectorFriendlyName della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="752d0-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="752d0-104">Il metodo **GetKeyProtectorFriendlyName** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Recupera il nome visualizzato utilizzato per identificare una protezione con chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="752d0-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="752d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="752d0-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="752d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="752d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="752d0-107">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="752d0-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752d0-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="752d0-108">Type: **string**</span></span>

<span data-ttu-id="752d0-109">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="752d0-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="752d0-110">*FriendlyName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="752d0-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="752d0-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="752d0-111">Type: **string**</span></span>

<span data-ttu-id="752d0-112">Stringa che contiene il nome specificato dall'utente utilizzato per identificare la protezione con chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="752d0-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="752d0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="752d0-113">Return value</span></span>

<span data-ttu-id="752d0-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="752d0-114">Type: **uint32**</span></span>

<span data-ttu-id="752d0-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="752d0-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="752d0-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="752d0-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="752d0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="752d0-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="752d0-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="752d0-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="752d0-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="752d0-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="752d0-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="752d0-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="752d0-121">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave valida.</span><span class="sxs-lookup"><span data-stu-id="752d0-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="752d0-122"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="752d0-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="752d0-123">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="752d0-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="752d0-124">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="752d0-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="752d0-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="752d0-125">Remarks</span></span>

<span data-ttu-id="752d0-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="752d0-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="752d0-127">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="752d0-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="752d0-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="752d0-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="752d0-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="752d0-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="752d0-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="752d0-130">Requirements</span></span>



| <span data-ttu-id="752d0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="752d0-131">Requirement</span></span> | <span data-ttu-id="752d0-132">Valore</span><span class="sxs-lookup"><span data-stu-id="752d0-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752d0-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="752d0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="752d0-134">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="752d0-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="752d0-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="752d0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="752d0-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="752d0-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="752d0-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="752d0-137">Namespace</span></span><br/>                | <span data-ttu-id="752d0-138">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="752d0-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="752d0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="752d0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="752d0-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="752d0-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="752d0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="752d0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752d0-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="752d0-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
