---
description: Smonta il volume e rimuove la chiave di crittografia del volume dalla memoria di sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Metodo Lock della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878930"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ca1e0-103">Metodo Lock della classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="ca1e0-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ca1e0-104">Il metodo **Lock** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) smonta il volume e rimuove la chiave di crittografia del volume dalla memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="ca1e0-105">Il contenuto del volume rimane inaccessibile finché non viene sbloccato tramite il metodo [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o il metodo [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="ca1e0-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="ca1e0-106">Questo metodo non può essere eseguito correttamente per il volume del sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="ca1e0-107">Se il disco supporta la crittografia hardware, la banda è impostata su "Locked".</span><span class="sxs-lookup"><span data-stu-id="ca1e0-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ca1e0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca1e0-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="ca1e0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca1e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca1e0-110">*ForceDismount* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ca1e0-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca1e0-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ca1e0-111">Type: **boolean**</span></span>

<span data-ttu-id="ca1e0-112">Se **true** , il disco viene smontato forzatamente.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca1e0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca1e0-113">Return value</span></span>

<span data-ttu-id="ca1e0-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca1e0-114">Type: **uint32**</span></span>

<span data-ttu-id="ca1e0-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ca1e0-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca1e0-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="ca1e0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca1e0-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca1e0-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ca1e0-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="ca1e0-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="ca1e0-120"><dt>**E \_ ACCESSO \_ negato**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="ca1e0-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="ca1e0-121">Le applicazioni accedono a questo volume.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-121">Applications are accessing this volume.</span></span> <span data-ttu-id="ca1e0-122">Se tutti gli accessi non sono esclusivi, l'impostazione del parametro *ForceDismount* su true consente di eseguire correttamente il metodo.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ca1e0-123"><dt>**FVE \_ E \_ non \_ crittografato**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="ca1e0-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="ca1e0-124">Il volume è completamente decrittografato e non può essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="ca1e0-125"><dt>**FVE \_ \_Protezione E \_ disabilitata**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="ca1e0-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="ca1e0-126">La chiave di crittografia del volume è disponibile in chiaro sul disco, impedendo il blocco del volume.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="ca1e0-127"><dt>**FVE \_ \_Chiave di ripristino E \_ \_ richiesta**</dt> <dt>2150694946 (0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="ca1e0-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="ca1e0-128">Il volume non dispone di protezioni con chiave di tipo "password numerica" o "chiave esterna" necessarie per sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="ca1e0-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca1e0-129">Remarks</span></span>

<span data-ttu-id="ca1e0-130">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ca1e0-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ca1e0-131">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ca1e0-132">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ca1e0-133">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ca1e0-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca1e0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca1e0-134">Requirements</span></span>



| <span data-ttu-id="ca1e0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca1e0-135">Requirement</span></span> | <span data-ttu-id="ca1e0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ca1e0-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1e0-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca1e0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1e0-138">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="ca1e0-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ca1e0-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca1e0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1e0-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca1e0-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca1e0-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca1e0-141">Namespace</span></span><br/>                | <span data-ttu-id="ca1e0-142">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ca1e0-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ca1e0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ca1e0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca1e0-144"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca1e0-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca1e0-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca1e0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca1e0-146">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ca1e0-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
