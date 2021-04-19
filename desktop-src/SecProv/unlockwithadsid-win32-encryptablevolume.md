---
description: Usa il Active Directory stringa dell'ID di sicurezza (SID) fornita per ottenere la chiave derivata e sbloccare il volume crittografato.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Metodo UnlockWithAdSid della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317688"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8ce4d-103">Metodo UnlockWithAdSid della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="8ce4d-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8ce4d-104">Il metodo **UnlockWithAdSid** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la stringa SID (Security Identifier) fornita Active Directory per ottenere la chiave derivata e sbloccare il volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="8ce4d-105">Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "</span><span class="sxs-lookup"><span data-stu-id="8ce4d-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8ce4d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ce4d-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="8ce4d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ce4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce4d-108">*SidString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ce4d-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ce4d-109">Stringa che contiene il SID Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce4d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ce4d-110">Return value</span></span>

<span data-ttu-id="8ce4d-111">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8ce4d-112">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ce4d-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="8ce4d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ce4d-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8ce4d-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce4d-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8ce4d-115">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ce4d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ce4d-116">Remarks</span></span>

<span data-ttu-id="8ce4d-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8ce4d-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8ce4d-118">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8ce4d-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8ce4d-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8ce4d-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8ce4d-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce4d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ce4d-121">Requirements</span></span>



| <span data-ttu-id="8ce4d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ce4d-122">Requirement</span></span> | <span data-ttu-id="8ce4d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8ce4d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce4d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ce4d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8ce4d-125">Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="8ce4d-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ce4d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ce4d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8ce4d-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8ce4d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ce4d-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8ce4d-128">Namespace</span></span><br/>                | <span data-ttu-id="8ce4d-129">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="8ce4d-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8ce4d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="8ce4d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ce4d-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ce4d-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce4d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ce4d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce4d-133">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="8ce4d-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
