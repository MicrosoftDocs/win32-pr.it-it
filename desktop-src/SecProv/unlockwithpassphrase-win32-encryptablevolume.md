---
description: 'Metodo UnlockWithPassphrase della Win32_EncryptableVolume: usa la passphrase per ottenere la chiave derivata.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Metodo UnlockWithPassphrase della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116459"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8d3ad-103">Metodo UnlockWithPassphrase della classe \_ EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="8d3ad-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8d3ad-104">Il **metodo UnlockWithPassphrase** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="8d3ad-105">Dopo aver calcolato la chiave derivata, la chiave derivata viene usata per sbloccare la chiave master del volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="8d3ad-106">Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato".</span><span class="sxs-lookup"><span data-stu-id="8d3ad-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8d3ad-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d3ad-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="8d3ad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d3ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d3ad-109">*Passphrase* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8d3ad-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d3ad-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="8d3ad-110">Type: **string**</span></span>

<span data-ttu-id="8d3ad-111">Stringa che specifica la passphrase.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d3ad-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d3ad-112">Return value</span></span>

<span data-ttu-id="8d3ad-113">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="8d3ad-113">Type: **uint32**</span></span>

<span data-ttu-id="8d3ad-114">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8d3ad-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d3ad-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="8d3ad-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d3ad-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d3ad-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="8d3ad-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="8d3ad-119"><dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="8d3ad-120">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="8d3ad-121">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="8d3ad-122"><dt>**FVE \_ E \_ FIPS \_ IMPEDISCE LA \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="8d3ad-123">L'impostazione di Criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'uso della passphrase.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="8d3ad-124"><dt>**FVE \_ E \_ CRITERIO \_ LUNGHEZZA \_ PASSPHRASE \_**</dt> NON VALIDA <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="8d3ad-125">La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="8d3ad-126"><dt>**FVE \_ E \_ \_ PASSPHRASE \_ TROPPO \_ SEMPLICE**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="8d3ad-127">La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore nei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="8d3ad-128"><dt>**FVE \_ E \_ AUTENTICAZIONE \_ NON RIUSCITA**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="8d3ad-129">Il volume non può essere sbloccato con le informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="8d3ad-130"><dt>**FVE \_ E \_ PROTECTOR \_ NOT \_ FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="8d3ad-131">La protezione della chiave specificata non esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="8d3ad-132">È necessario immettere un'altra protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="8d3ad-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="8d3ad-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d3ad-133">Requirements</span></span>



| <span data-ttu-id="8d3ad-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d3ad-134">Requirement</span></span> | <span data-ttu-id="8d3ad-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8d3ad-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d3ad-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d3ad-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8d3ad-137">Solo app desktop di Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="8d3ad-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8d3ad-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d3ad-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8d3ad-139">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8d3ad-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d3ad-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d3ad-140">Namespace</span></span><br/>                | <span data-ttu-id="8d3ad-141">Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="8d3ad-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8d3ad-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8d3ad-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d3ad-143"><dt>Win32 \_ encryptablevolume.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d3ad-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d3ad-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d3ad-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d3ad-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="8d3ad-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




