---
description: Disabilita o sospende tutte le protezioni con chiave associate a questo volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Metodo DisableKeyProtectors della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312764"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1c4b5-103">Metodo DisableKeyProtectors della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="1c4b5-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1c4b5-104">Il metodo **DisableKeyProtectors** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Disabilita o sospende tutte le protezioni con chiave associate a questo volume.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c4b5-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="1c4b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c4b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c4b5-107">*DisableCount* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="1c4b5-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4b5-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c4b5-108">Type: **uint32**</span></span>

<span data-ttu-id="1c4b5-109">Integer che specifica il numero di riavvii per i quali verranno disabilitate le protezioni con chiave.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="1c4b5-110">Questo parametro è disponibile solo nei volumi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c4b5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c4b5-111">Return value</span></span>

<span data-ttu-id="1c4b5-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c4b5-112">Type: **uint32**</span></span>

<span data-ttu-id="1c4b5-113">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1c4b5-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c4b5-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="1c4b5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c4b5-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1c4b5-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b5-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="1c4b5-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="1c4b5-118"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b5-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="1c4b5-119">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="1c4b5-120">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="1c4b5-120">Security Considerations</span></span>

<span data-ttu-id="1c4b5-121">Questo metodo espone la chiave di crittografia del volume in chiaro sul disco rigido, disattivando la protezione del volume.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="1c4b5-122">È consigliabile evitare di usare password o chiavi di crittografia in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c4b5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c4b5-123">Remarks</span></span>

<span data-ttu-id="1c4b5-124">È possibile aggiungere nuove protezioni con chiave anche quando le protezioni con chiave sono disabilitate o sospese.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="1c4b5-125">Queste protezioni con chiave rimarranno disabilitate a meno che non venga chiamato [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="1c4b5-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="1c4b5-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c4b5-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c4b5-127">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1c4b5-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1c4b5-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c4b5-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1c4b5-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4b5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c4b5-130">Requirements</span></span>



| <span data-ttu-id="1c4b5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4b5-131">Requirement</span></span> | <span data-ttu-id="1c4b5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1c4b5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4b5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c4b5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1c4b5-134">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1c4b5-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1c4b5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c4b5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1c4b5-136">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c4b5-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c4b5-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c4b5-137">Namespace</span></span><br/>                | <span data-ttu-id="1c4b5-138">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1c4b5-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1c4b5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1c4b5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c4b5-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b5-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c4b5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c4b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4b5-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1c4b5-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="1c4b5-143">**EnableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="1c4b5-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
