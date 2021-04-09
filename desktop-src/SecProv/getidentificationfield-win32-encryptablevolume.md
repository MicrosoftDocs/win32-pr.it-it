---
description: Restituisce la stringa di identificazione disponibile nei metadati del volume.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Metodo GetIdentificationField della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128754"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9620d-103">Metodo GetIdentificationField della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="9620d-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9620d-104">Il metodo **GetIdentificationField** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) restituisce la stringa di identificazione disponibile nei metadati del volume.</span><span class="sxs-lookup"><span data-stu-id="9620d-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="9620d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9620d-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="9620d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9620d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9620d-107">*IdentificationField* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9620d-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9620d-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="9620d-108">Type: **string**</span></span>

<span data-ttu-id="9620d-109">Stringa che specifica il campo di identificazione assegnato al volume.</span><span class="sxs-lookup"><span data-stu-id="9620d-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9620d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9620d-110">Return value</span></span>

<span data-ttu-id="9620d-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9620d-111">Type: **uint32**</span></span>

<span data-ttu-id="9620d-112">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9620d-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9620d-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="9620d-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="9620d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9620d-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9620d-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9620d-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="9620d-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="9620d-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="9620d-117"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="9620d-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="9620d-118">Questa unità è bloccata da Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9620d-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="9620d-119">È necessario sbloccare questo volume dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="9620d-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="9620d-120"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9620d-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="9620d-121">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9620d-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9620d-122">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9620d-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="9620d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9620d-123">Requirements</span></span>



| <span data-ttu-id="9620d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9620d-124">Requirement</span></span> | <span data-ttu-id="9620d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9620d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9620d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9620d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9620d-127">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="9620d-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9620d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9620d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9620d-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9620d-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9620d-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9620d-130">Namespace</span></span><br/>                | <span data-ttu-id="9620d-131">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="9620d-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9620d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9620d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9620d-133"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9620d-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9620d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9620d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9620d-135">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="9620d-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




