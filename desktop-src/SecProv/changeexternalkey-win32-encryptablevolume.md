---
description: Modifica una chiave esterna associata a un volume crittografato.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Metodo ChangeExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316121"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bb6e7-103">Metodo ChangeExternalKey della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="bb6e7-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bb6e7-104">Il metodo **ChangeExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) modifica una chiave esterna associata a un volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb6e7-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="bb6e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb6e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6e7-107">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb6e7-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6e7-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="bb6e7-108">Type: **string**</span></span>

<span data-ttu-id="bb6e7-109">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="bb6e7-110">*NewExternalKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bb6e7-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6e7-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="bb6e7-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="bb6e7-112">Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="bb6e7-113">*NewVolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bb6e7-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb6e7-114">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="bb6e7-114">Type: **string**</span></span>

<span data-ttu-id="bb6e7-115">Identificatore di stringa univoco aggiornato utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6e7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb6e7-116">Return value</span></span>

<span data-ttu-id="bb6e7-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb6e7-117">Type: **uint32**</span></span>

<span data-ttu-id="bb6e7-118">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="bb6e7-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb6e7-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="bb6e7-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb6e7-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb6e7-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="bb6e7-122">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="bb6e7-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="bb6e7-124">Il parametro *NewExternalKey* non è una matrice di dimensioni pari a 32.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="bb6e7-125"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="bb6e7-126">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="bb6e7-127"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="bb6e7-128">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="bb6e7-129">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="bb6e7-130"><dt>**FVE \_ E \_ \_ CDDVD di avvio**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="bb6e7-131">Nel computer è presente un CD/DVD di avvio.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="bb6e7-132">Rimuovere il CD/DVD e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="bb6e7-133"><dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="bb6e7-134">La protezione con chiave specificata non esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="bb6e7-135"><dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="bb6e7-136">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password" o "External Key".</span><span class="sxs-lookup"><span data-stu-id="bb6e7-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="bb6e7-137">Usare il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb6e7-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb6e7-138">Remarks</span></span>

<span data-ttu-id="bb6e7-139">Questo metodo può essere utilizzato per modificare la chiave esterna per qualsiasi protezione con chiave che utilizza una chiave esterna.</span><span class="sxs-lookup"><span data-stu-id="bb6e7-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6e7-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb6e7-140">Requirements</span></span>



| <span data-ttu-id="bb6e7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb6e7-141">Requirement</span></span> | <span data-ttu-id="bb6e7-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bb6e7-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6e7-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb6e7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6e7-144">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="bb6e7-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb6e7-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb6e7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6e7-146">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb6e7-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bb6e7-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb6e7-147">Namespace</span></span><br/>                | <span data-ttu-id="bb6e7-148">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="bb6e7-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bb6e7-149">MOF</span><span class="sxs-lookup"><span data-stu-id="bb6e7-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb6e7-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb6e7-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6e7-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb6e7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6e7-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="bb6e7-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




