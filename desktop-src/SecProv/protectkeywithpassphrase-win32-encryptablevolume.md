---
description: Usa la passphrase per ottenere la chiave derivata.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Metodo ProtectKeyWithPassphrase della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306379"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6a4c7-103">Metodo ProtectKeyWithPassphrase della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="6a4c7-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6a4c7-104">Il metodo **ProtectKeyWithPassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="6a4c7-105">Dopo che la chiave derivata è stata calcolata, la chiave derivata viene utilizzata per proteggere la chiave master del volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4c7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a4c7-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6a4c7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a4c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4c7-108">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a4c7-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4c7-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6a4c7-109">Type: **string**</span></span>

<span data-ttu-id="6a4c7-110">Stringa che specifica un identificatore di stringa assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="6a4c7-111">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="6a4c7-112">*Passphrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a4c7-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4c7-113">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6a4c7-113">Type: **string**</span></span>

<span data-ttu-id="6a4c7-114">Stringa che specifica la passphrase.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="6a4c7-115">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a4c7-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4c7-116">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6a4c7-116">Type: **string**</span></span>

<span data-ttu-id="6a4c7-117">Stringa che identifica in modo univoco la protezione con chiave creata.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="6a4c7-118">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4c7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a4c7-119">Return value</span></span>

<span data-ttu-id="6a4c7-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a4c7-120">Type: **uint32**</span></span>

<span data-ttu-id="6a4c7-121">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6a4c7-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a4c7-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="6a4c7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a4c7-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a4c7-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="6a4c7-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="6a4c7-126"><dt>**FVE \_ E \_ non \_ consentito \_ in \_ \_ modalità provvisoria**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="6a4c7-127">Crittografia unità BitLocker può essere utilizzato solo per scopi di ripristino se utilizzato in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="6a4c7-128"><dt>**FVE \_ \_Passphrase dei criteri E \_ \_ non \_ consentita**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="6a4c7-129">Criteri di gruppo non consente la creazione di una passphrase.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="6a4c7-130"><dt>**FVE \_ E \_ FIPS \_ impedisce la \_ passphrase**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="6a4c7-131">L'impostazione di criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'utilizzo della passphrase.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="6a4c7-132"><dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza passphrase non valida**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="6a4c7-133">La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="6a4c7-134"><dt>**FVE \_ \_Passphrase dei criteri E \_ \_ troppo \_ semplice**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="6a4c7-135">La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore in criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="6a4c7-136"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="6a4c7-137">Il volume è già bloccato dal Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="6a4c7-138">È necessario sbloccare l'unità dal pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="6a4c7-139"><dt>**FVE \_ E \_ \_ aggiornamento 2150694948 sovrapposto**</dt> <dt>(0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="6a4c7-140">Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6a4c7-141"><dt>**FVE \_ \_Protezione con chiave E \_ \_ non \_ supportata**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="6a4c7-142">La protezione con chiave non è supportata dalla versione di Crittografia unità BitLocker attualmente nel volume.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="6a4c7-143"><dt>**FVE \_ E la \_ passphrase del volume del sistema operativo \_ non è \_ \_ \_ consentita**</dt> <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="6a4c7-144">Non è possibile aggiungere la passphrase al volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="6a4c7-145"><dt>**FVE \_ La \_ protezione E \_ esiste**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="6a4c7-146">La protezione con chiave specificata esiste già nel volume.</span><span class="sxs-lookup"><span data-stu-id="6a4c7-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="6a4c7-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a4c7-147">Requirements</span></span>



| <span data-ttu-id="6a4c7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4c7-148">Requirement</span></span> | <span data-ttu-id="6a4c7-149">Valore</span><span class="sxs-lookup"><span data-stu-id="6a4c7-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4c7-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a4c7-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4c7-151">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="6a4c7-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a4c7-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a4c7-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4c7-153">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a4c7-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6a4c7-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a4c7-154">Namespace</span></span><br/>                | <span data-ttu-id="6a4c7-155">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6a4c7-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6a4c7-156">MOF</span><span class="sxs-lookup"><span data-stu-id="6a4c7-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a4c7-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a4c7-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4c7-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a4c7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4c7-159">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6a4c7-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




