---
description: Imposta la stringa dell'identificatore specificata nei metadati del volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Metodo SetIdentificationField della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884834"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e0072-103">Metodo SetIdentificationField della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="e0072-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e0072-104">Il metodo **SetIdentificationField** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) imposta la stringa dell'identificatore specificata nei metadati del volume.</span><span class="sxs-lookup"><span data-stu-id="e0072-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0072-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0072-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="e0072-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0072-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0072-107">*IdentificationField* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e0072-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0072-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="e0072-108">Type: **string**</span></span>

<span data-ttu-id="e0072-109">Stringa che specifica il campo di identificazione assegnato al volume.</span><span class="sxs-lookup"><span data-stu-id="e0072-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="e0072-110">Se la stringa facoltativa non è presente, verranno utilizzati i valori impostati per il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0072-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="e0072-111">Se la stringa è presente e non è vuota, viene utilizzato il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e0072-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="e0072-112">Il parametro *IdentificationField* non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e0072-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0072-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0072-113">Return value</span></span>

<span data-ttu-id="e0072-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0072-114">Type: **uint32**</span></span>

<span data-ttu-id="e0072-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e0072-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e0072-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0072-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="e0072-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0072-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0072-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e0072-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="e0072-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="e0072-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="e0072-120"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="e0072-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="e0072-121">Questa unità è bloccata da Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e0072-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="e0072-122">È necessario sbloccare questo volume dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="e0072-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="e0072-123"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="e0072-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="e0072-124">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e0072-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="e0072-125">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e0072-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="e0072-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0072-126">Requirements</span></span>



| <span data-ttu-id="e0072-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0072-127">Requirement</span></span> | <span data-ttu-id="e0072-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e0072-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0072-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0072-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e0072-130">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="e0072-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0072-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0072-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e0072-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0072-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e0072-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0072-133">Namespace</span></span><br/>                | <span data-ttu-id="e0072-134">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="e0072-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e0072-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e0072-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0072-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0072-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0072-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0072-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0072-138">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="e0072-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




