---
description: Riprende la crittografia o la decrittografia di un volume.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Metodo ResumeConversion della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750834"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b795f-103">Metodo ResumeConversion della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="b795f-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b795f-104">Il metodo **ResumeConversion** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) riprende la crittografia o la decrittografia di un volume.</span><span class="sxs-lookup"><span data-stu-id="b795f-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="b795f-105">Se il disco supporta la crittografia hardware, questa funzione può riprendere solo un'operazione di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="b795f-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="b795f-106">Per ulteriori informazioni, vedere [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="b795f-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b795f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b795f-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="b795f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b795f-108">Parameters</span></span>

<span data-ttu-id="b795f-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b795f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b795f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b795f-110">Return value</span></span>

<span data-ttu-id="b795f-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b795f-111">Type: **uint32**</span></span>

<span data-ttu-id="b795f-112">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b795f-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="b795f-113">Se questo metodo viene utilizzato in un volume completamente crittografato o completamente decrittografato o se la crittografia/decrittografia è già in corso nel volume, viene restituito 0 presumendo che non si verifichino altri errori.</span><span class="sxs-lookup"><span data-stu-id="b795f-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="b795f-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b795f-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="b795f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b795f-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b795f-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b795f-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="b795f-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b795f-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="b795f-118"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b795f-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="b795f-119">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b795f-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="b795f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b795f-120">Remarks</span></span>

<span data-ttu-id="b795f-121">Se questo metodo viene utilizzato in un volume con crittografia/decrittografia sospesa, l'esecuzione di questo metodo fa in modo che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che è in corso la crittografia o la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="b795f-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="b795f-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b795f-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b795f-123">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b795f-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b795f-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b795f-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b795f-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b795f-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b795f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b795f-126">Requirements</span></span>



| <span data-ttu-id="b795f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b795f-127">Requirement</span></span> | <span data-ttu-id="b795f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b795f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b795f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b795f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b795f-130">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="b795f-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b795f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b795f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b795f-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b795f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b795f-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b795f-133">Namespace</span></span><br/>                | <span data-ttu-id="b795f-134">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b795f-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b795f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b795f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b795f-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b795f-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b795f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b795f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b795f-138">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b795f-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
