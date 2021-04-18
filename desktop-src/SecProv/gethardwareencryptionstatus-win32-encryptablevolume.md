---
description: Determina se il volume si trova in un'unità che supporta o può supportare la crittografia hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Metodo GetHardwareEncryptionStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306398"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7306f-103">Metodo GetHardwareEncryptionStatus della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="7306f-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7306f-104">Il metodo **GetHardwareEncryptionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) determina se il volume si trova in un'unità che supporta o può supportare la crittografia hardware.</span><span class="sxs-lookup"><span data-stu-id="7306f-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="7306f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7306f-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="7306f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7306f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7306f-107">*HardwareEncryptionStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7306f-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7306f-108">Specifica se l'unità può supportare la crittografia hardware.</span><span class="sxs-lookup"><span data-stu-id="7306f-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="7306f-109">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7306f-109">This can be one of the following values.</span></span>



| <span data-ttu-id="7306f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7306f-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="7306f-111">Significato</span><span class="sxs-lookup"><span data-stu-id="7306f-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="7306f-112"><dt>**Non supportato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7306f-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="7306f-113">La crittografia hardware non è supportata.</span><span class="sxs-lookup"><span data-stu-id="7306f-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="7306f-114"><dt>**Nessuna protezione**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7306f-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="7306f-115">La crittografia dell'unità non è supportata.</span><span class="sxs-lookup"><span data-stu-id="7306f-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="7306f-116"><dt>**Usa software**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7306f-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7306f-117">Il metodo di crittografia è basato su software.</span><span class="sxs-lookup"><span data-stu-id="7306f-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="7306f-118"><dt>**Usa l'hardware**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7306f-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="7306f-119">L'unità supporta la crittografia hardware.</span><span class="sxs-lookup"><span data-stu-id="7306f-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7306f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7306f-120">Return value</span></span>

<span data-ttu-id="7306f-121">Questa funzione restituisce zero (0) se il volume è compatibile con la crittografia hardware BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7306f-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="7306f-122">In caso contrario, la funzione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="7306f-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="7306f-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="7306f-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7306f-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7306f-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7306f-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7306f-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7306f-126">Il volume è compatibile con la crittografia hardware di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7306f-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7306f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7306f-127">Requirements</span></span>



| <span data-ttu-id="7306f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7306f-128">Requirement</span></span> | <span data-ttu-id="7306f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7306f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7306f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7306f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7306f-131">Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="7306f-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7306f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7306f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7306f-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7306f-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7306f-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7306f-134">Namespace</span></span><br/>                | <span data-ttu-id="7306f-135">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="7306f-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7306f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7306f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7306f-137"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7306f-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7306f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7306f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7306f-139">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="7306f-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




