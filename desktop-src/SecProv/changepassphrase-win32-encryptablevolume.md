---
description: Usa la nuova passphrase per ottenere una nuova chiave derivata.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Metodo ChangePassphrase della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316119"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="aa44b-103">Metodo ChangePassphrase della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="aa44b-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="aa44b-104">Il metodo **ChangePassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la nuova passphrase per ottenere una nuova chiave derivata.</span><span class="sxs-lookup"><span data-stu-id="aa44b-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="aa44b-105">Dopo aver calcolato la chiave derivata, la nuova chiave derivata viene utilizzata per proteggere la chiave master del volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="aa44b-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa44b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa44b-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="aa44b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa44b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa44b-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa44b-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa44b-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="aa44b-109">Type: **string**</span></span>

<span data-ttu-id="aa44b-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="aa44b-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="aa44b-111">*NewPassphrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa44b-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa44b-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="aa44b-112">Type: **string**</span></span>

<span data-ttu-id="aa44b-113">Stringa aggiornata che specifica la passphrase.</span><span class="sxs-lookup"><span data-stu-id="aa44b-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="aa44b-114">*NewProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aa44b-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa44b-115">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="aa44b-115">Type: **string**</span></span>

<span data-ttu-id="aa44b-116">Identificatore di stringa univoco aggiornato usato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="aa44b-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa44b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa44b-117">Return value</span></span>

<span data-ttu-id="aa44b-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa44b-118">Type: **uint32**</span></span>

<span data-ttu-id="aa44b-119">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="aa44b-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="aa44b-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa44b-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="aa44b-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa44b-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa44b-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="aa44b-123">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="aa44b-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="aa44b-124"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="aa44b-125">Il volume è già bloccato dal Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aa44b-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="aa44b-126">È necessario sbloccare l'unità dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="aa44b-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="aa44b-127"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="aa44b-128">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aa44b-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="aa44b-129">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="aa44b-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="aa44b-130"><dt>**FVE \_ E \_ \_ aggiornamento 2150694948 sovrapposto**</dt> <dt>(0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="aa44b-131">Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="aa44b-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="aa44b-132"><dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="aa44b-133">La protezione con chiave specificata non è del tipo corretto.</span><span class="sxs-lookup"><span data-stu-id="aa44b-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="aa44b-134"><dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza passphrase non valida**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="aa44b-135">La passphrase aggiornata specificata non soddisfa i requisiti di lunghezza minima o massima.</span><span class="sxs-lookup"><span data-stu-id="aa44b-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="aa44b-136"><dt>**FVE \_ \_Passphrase dei criteri E \_ \_ troppo \_ semplice**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="aa44b-137">La passphrase aggiornata non soddisfa i requisiti di complessità impostati dall'amministratore in criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="aa44b-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa44b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa44b-138">Requirements</span></span>



| <span data-ttu-id="aa44b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa44b-139">Requirement</span></span> | <span data-ttu-id="aa44b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="aa44b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa44b-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa44b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aa44b-142">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="aa44b-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aa44b-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa44b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aa44b-144">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa44b-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aa44b-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa44b-145">Namespace</span></span><br/>                | <span data-ttu-id="aa44b-146">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="aa44b-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="aa44b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="aa44b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa44b-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa44b-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa44b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa44b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa44b-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="aa44b-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




