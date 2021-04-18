---
description: Recupera il numero di volte in cui BitLocker è stato sospeso.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Metodo GetSuspendCount della classe Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316101"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="531e4-103">Metodo GetSuspendCount della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="531e4-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="531e4-104">Il metodo **GetSuspendCount** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Recupera il numero di riavvii prima che la protezione venga ripresa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="531e4-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="531e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="531e4-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="531e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="531e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="531e4-107">*SuspendCount*</span><span class="sxs-lookup"><span data-stu-id="531e4-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="531e4-108">Valore intero compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="531e4-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="531e4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="531e4-109">Return value</span></span>

<span data-ttu-id="531e4-110">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="531e4-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="531e4-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="531e4-111">Return code</span></span>                                                                                          | <span data-ttu-id="531e4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="531e4-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="531e4-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="531e4-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="531e4-114">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="531e4-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="531e4-115"><dt>**ERRORE \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="531e4-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="531e4-116">Restituito se il volume non è sospeso o non è un volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="531e4-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="531e4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="531e4-117">Remarks</span></span>

<span data-ttu-id="531e4-118">Questo metodo si applica solo al volume del sistema operativo e solo se è effettivamente sospeso al momento.</span><span class="sxs-lookup"><span data-stu-id="531e4-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="531e4-119">Se il volume non è sospeso o non è un volume del sistema operativo, verrà restituito l' **errore \_ non \_ supportato** .</span><span class="sxs-lookup"><span data-stu-id="531e4-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="531e4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="531e4-120">Requirements</span></span>



| <span data-ttu-id="531e4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="531e4-121">Requirement</span></span> | <span data-ttu-id="531e4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="531e4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="531e4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="531e4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="531e4-124">Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="531e4-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="531e4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="531e4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="531e4-126">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="531e4-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="531e4-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="531e4-127">Namespace</span></span><br/>                | <span data-ttu-id="531e4-128">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="531e4-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="531e4-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="531e4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="531e4-130"><dt>Activdbg. h</dt></span><span class="sxs-lookup"><span data-stu-id="531e4-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="531e4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="531e4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="531e4-132"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="531e4-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="531e4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="531e4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531e4-134">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="531e4-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




