---
description: 'Metodo ProtectKeyWithPassphrase della classe Win32_EncryptableVolume : usa la passphrase per ottenere la chiave derivata.'
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Metodo ProtectKeyWithPassphrase della Win32_EncryptableVolume classe
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
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098349"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5b3dd-103">Metodo ProtectKeyWithPassphrase della classe \_ EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="5b3dd-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5b3dd-104">Il **metodo ProtectKeyWithPassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="5b3dd-105">Dopo aver calcolato la chiave derivata, la chiave derivata viene usata per proteggere la chiave master del volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3dd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b3dd-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5b3dd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b3dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3dd-108">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5b3dd-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3dd-109">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="5b3dd-109">Type: **string**</span></span>

<span data-ttu-id="5b3dd-110">Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="5b3dd-111">Se questo parametro non viene specificato, viene usato un valore vuoto.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="5b3dd-112">*Passphrase* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5b3dd-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3dd-113">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="5b3dd-113">Type: **string**</span></span>

<span data-ttu-id="5b3dd-114">Stringa che specifica la passphrase.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="5b3dd-115">*VolumeKeyProtectorID* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="5b3dd-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3dd-116">Tipo: **string**</span><span class="sxs-lookup"><span data-stu-id="5b3dd-116">Type: **string**</span></span>

<span data-ttu-id="5b3dd-117">Stringa che identifica in modo univoco la protezione con chiave creata.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="5b3dd-118">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione con chiave viene scritta per metadati di banda.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3dd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b3dd-119">Return value</span></span>

<span data-ttu-id="5b3dd-120">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5b3dd-120">Type: **uint32**</span></span>

<span data-ttu-id="5b3dd-121">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5b3dd-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b3dd-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="5b3dd-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b3dd-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b3dd-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="5b3dd-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="5b3dd-126"><dt>**FVE \_ E \_ NON CONSENTITO IN MODALITÀ \_ \_ \_ \_ PROVVISORIA**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="5b3dd-127">Crittografia unità BitLocker può essere usato solo a scopo di ripristino quando viene usato in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="5b3dd-128"><dt>**FVE \_ \_ \_ PASSPHRASE DEI CRITERI E NON \_ \_ CONSENTITA**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="5b3dd-129">Criteri di gruppo non consente la creazione di una passphrase.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="5b3dd-130"><dt>**FVE \_ E \_ FIPS \_ IMPEDISCE LA \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="5b3dd-131">L'impostazione di Criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'uso della passphrase.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="5b3dd-132"><dt>**FVE \_ E \_ CRITERIO \_ LUNGHEZZA \_ PASSPHRASE \_**</dt> NON VALIDA <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="5b3dd-133">La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="5b3dd-134"><dt>**FVE \_ E \_ \_ PASSPHRASE \_ TROPPO \_ SEMPLICE**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="5b3dd-135">La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore nei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="5b3dd-136"><dt>**FVE \_ E \_ VOLUME \_ BLOCCATO**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="5b3dd-137">Il volume è già bloccato da Crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="5b3dd-138">È necessario sbloccare l'unità Pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="5b3dd-139"><dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="5b3dd-140">Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5b3dd-141"><dt>**FVE \_ E \_ KEY \_ PROTECTOR NOT \_ \_ SUPPORTED**</dt> <dt>2150695017 (0X80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="5b3dd-142">La protezione della chiave non è supportata dalla versione di Crittografia unità BitLocker attualmente nel volume.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="5b3dd-143"><dt>**FVE \_ \_ \_ \_ PASSPHRASE \_ \_ DEL VOLUME**</dt> DEL SISTEMA OPERATIVO NON CONSENTITA <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="5b3dd-144">La passphrase non può essere aggiunta al volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="5b3dd-145"><dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="5b3dd-146">La protezione della chiave specificata esiste già in questo volume.</span><span class="sxs-lookup"><span data-stu-id="5b3dd-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="5b3dd-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b3dd-147">Requirements</span></span>



| <span data-ttu-id="5b3dd-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b3dd-148">Requirement</span></span> | <span data-ttu-id="5b3dd-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5b3dd-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3dd-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b3dd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3dd-151">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="5b3dd-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b3dd-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b3dd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3dd-153">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5b3dd-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5b3dd-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b3dd-154">Namespace</span></span><br/>                | <span data-ttu-id="5b3dd-155">Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5b3dd-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5b3dd-156">MOF</span><span class="sxs-lookup"><span data-stu-id="5b3dd-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b3dd-157"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b3dd-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3dd-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b3dd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3dd-159">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="5b3dd-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




