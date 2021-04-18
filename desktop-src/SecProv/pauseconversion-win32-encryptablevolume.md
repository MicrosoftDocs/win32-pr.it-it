---
description: Sospende la crittografia o la decrittografia di un volume.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Metodo PauseConversion della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315340"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6bf30-103">Metodo PauseConversion della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="6bf30-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6bf30-104">Il metodo **PauseConversion** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) sospende la crittografia o la decrittografia di un volume.</span><span class="sxs-lookup"><span data-stu-id="6bf30-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="6bf30-105">Se il disco supporta la crittografia hardware, questa funzione può sospendere un'operazione di cancellazione ma non può sospendere la crittografia basata su hardware.</span><span class="sxs-lookup"><span data-stu-id="6bf30-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6bf30-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bf30-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="6bf30-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bf30-107">Parameters</span></span>

<span data-ttu-id="6bf30-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6bf30-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bf30-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bf30-109">Return value</span></span>

<span data-ttu-id="6bf30-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6bf30-110">Type: **uint32**</span></span>

<span data-ttu-id="6bf30-111">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6bf30-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="6bf30-112">Se questo metodo viene utilizzato in un volume completamente crittografato o completamente decrittografato o se la crittografia/decrittografia è già sospesa nel volume, viene restituito 0 presumendo che non si verifichino altri errori.</span><span class="sxs-lookup"><span data-stu-id="6bf30-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="6bf30-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bf30-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6bf30-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bf30-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6bf30-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6bf30-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6bf30-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="6bf30-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="6bf30-117"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6bf30-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="6bf30-118">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="6bf30-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6bf30-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bf30-119">Remarks</span></span>

<span data-ttu-id="6bf30-120">Se questo metodo viene utilizzato in un volume con crittografia/decrittografia in corso, l'esecuzione di questo metodo fa in modo che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che la crittografia o la decrittografia è sospesa.</span><span class="sxs-lookup"><span data-stu-id="6bf30-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="6bf30-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6bf30-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6bf30-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6bf30-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6bf30-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6bf30-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6bf30-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6bf30-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bf30-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bf30-125">Requirements</span></span>



| <span data-ttu-id="6bf30-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bf30-126">Requirement</span></span> | <span data-ttu-id="6bf30-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6bf30-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf30-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bf30-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf30-129">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="6bf30-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6bf30-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bf30-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf30-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6bf30-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bf30-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6bf30-132">Namespace</span></span><br/>                | <span data-ttu-id="6bf30-133">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6bf30-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6bf30-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6bf30-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bf30-135"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bf30-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bf30-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bf30-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf30-137">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6bf30-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
