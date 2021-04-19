---
description: Usa una chiave esterna fornita per accedere al contenuto di un volume di dati.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Metodo UnlockWithExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317683"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="41680-103">Metodo UnlockWithExternalKey della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="41680-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="41680-104">Il metodo **UnlockWithExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa una chiave esterna fornita per accedere al contenuto di un volume di dati.</span><span class="sxs-lookup"><span data-stu-id="41680-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="41680-105">La chiave di crittografia del volume deve essere stata protetta con una o più protezioni con chiave di tipo "chiave esterna" usando il metodo [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per poter sbloccare il volume con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="41680-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="41680-106">Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "</span><span class="sxs-lookup"><span data-stu-id="41680-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="41680-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41680-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="41680-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41680-109">*ExternalKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41680-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41680-110">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="41680-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="41680-111">Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="41680-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="41680-112">Questa chiave può essere ottenuta chiamando il metodo [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="41680-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41680-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41680-113">Return value</span></span>

<span data-ttu-id="41680-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41680-114">Type: **uint32**</span></span>

<span data-ttu-id="41680-115">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="41680-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="41680-116">Se il volume è già sbloccato, questo metodo restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="41680-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="41680-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="41680-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="41680-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41680-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="41680-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="41680-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="41680-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="41680-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="41680-121"><dt>**Errore \_ NON \_**</dt> è stato trovato <dt>alcun valore specificato (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="41680-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="41680-122">Il volume non dispone di una protezione con chiave di tipo "chiave esterna".</span><span class="sxs-lookup"><span data-stu-id="41680-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="41680-123"><dt>**Errore \_ La \_ password**</dt> non è valida. <dt>nessun valore specificato (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="41680-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="41680-124">Sono presenti una o più protezioni con chiave di tipo "chiave esterna", ma il parametro *ExternalKey* specificato non è in grado di sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="41680-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="41680-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="41680-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="41680-126">Il parametro *ExternalKey* non è una matrice di dimensioni 4.</span><span class="sxs-lookup"><span data-stu-id="41680-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="41680-127"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="41680-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="41680-128">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="41680-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="41680-129">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="41680-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="41680-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="41680-130">Remarks</span></span>

<span data-ttu-id="41680-131">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="41680-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="41680-132">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="41680-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="41680-133">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="41680-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="41680-134">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="41680-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41680-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41680-135">Requirements</span></span>



| <span data-ttu-id="41680-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="41680-136">Requirement</span></span> | <span data-ttu-id="41680-137">Valore</span><span class="sxs-lookup"><span data-stu-id="41680-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41680-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41680-138">Minimum supported client</span></span><br/> | <span data-ttu-id="41680-139">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="41680-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="41680-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41680-140">Minimum supported server</span></span><br/> | <span data-ttu-id="41680-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41680-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41680-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="41680-142">Namespace</span></span><br/>                | <span data-ttu-id="41680-143">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="41680-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="41680-144">MOF</span><span class="sxs-lookup"><span data-stu-id="41680-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41680-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41680-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41680-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41680-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41680-147">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="41680-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
