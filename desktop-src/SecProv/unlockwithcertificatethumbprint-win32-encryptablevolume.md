---
description: Usa l'identificazione personale del certificato fornita per ottenere la chiave derivata e sbloccare il volume crittografato.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Metodo UnlockWithCertificateThumbprint della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750826"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8cb7b-103">Metodo UnlockWithCertificateThumbprint della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="8cb7b-103">UnlockWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8cb7b-104">Il metodo **UnlockWithCertificateThumbprint** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa l'identificazione personale del [*certificato*](../secgloss/c-gly.md) fornita per ottenere la chiave derivata e sbloccare il volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-104">The **UnlockWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) thumbprint to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="8cb7b-105">Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "</span><span class="sxs-lookup"><span data-stu-id="8cb7b-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8cb7b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8cb7b-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="8cb7b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cb7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb7b-108">*CertThumbprint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cb7b-108">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb7b-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="8cb7b-109">Type: **string**</span></span>

<span data-ttu-id="8cb7b-110">Viene accettato un valore di identificazione personale pari a 0, che comporta la ricerca dell'archivio locale per il certificato appropriato.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-110">A thumbprint value of 0 is accepted and results in a search of the local store for the appropriate certificate.</span></span> <span data-ttu-id="8cb7b-111">Se viene trovato un singolo certificato BitLocker, la ricerca ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-111">If a single BitLocker certificate is found, the search is successful.</span></span> <span data-ttu-id="8cb7b-112">Se non viene trovato nessuno o più di un certificato, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-112">If none or more than one certificate is found, the method fails.</span></span>

</dd> <dt>

<span data-ttu-id="8cb7b-113">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cb7b-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb7b-114">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="8cb7b-114">Type: **string**</span></span>

<span data-ttu-id="8cb7b-115">Stringa di identificazione personale specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-115">A user-specified personal identification string.</span></span> <span data-ttu-id="8cb7b-116">Questa stringa deve essere composta da una sequenza di 4 a 20 cifre.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="8cb7b-117">Questa stringa viene usata per autenticare automaticamente il [*provider di archiviazione chiavi*](../secgloss/k-gly.md) (KSP) se usato con una [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8cb7b-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb7b-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cb7b-118">Return value</span></span>

<span data-ttu-id="8cb7b-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8cb7b-119">Type: **uint32**</span></span>

<span data-ttu-id="8cb7b-120">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8cb7b-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cb7b-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="8cb7b-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cb7b-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cb7b-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="8cb7b-124">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="8cb7b-125"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="8cb7b-126">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="8cb7b-127">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="8cb7b-128"><dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="8cb7b-129">Non è possibile sbloccare il volume utilizzando le informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-129">The volume cannot be unlocked by using the provided information.</span></span> <br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="8cb7b-130"><dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="8cb7b-131">La protezione con chiave specificata non esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="8cb7b-132">È necessario immettere un'altra protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-132">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="8cb7b-133"><dt>**FVE \_ Autenticazione di E \_ PRIVATEKEY \_ \_ non riuscita**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-133"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="8cb7b-134">Non è stato possibile autorizzare la [*chiave privata*](../secgloss/p-gly.md) associata al certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-134">The [*private key*](../secgloss/p-gly.md) associated with the specified certificate could not be authorized.</span></span> <span data-ttu-id="8cb7b-135">L'autorizzazione della chiave privata non è stata specificata o l'autorizzazione fornita non è valida.</span><span class="sxs-lookup"><span data-stu-id="8cb7b-135">The private key authorization was either not provided or the provided authorization was not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8cb7b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cb7b-136">Requirements</span></span>



| <span data-ttu-id="8cb7b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb7b-137">Requirement</span></span> | <span data-ttu-id="8cb7b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8cb7b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb7b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cb7b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb7b-140">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="8cb7b-140">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8cb7b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cb7b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb7b-142">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cb7b-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cb7b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8cb7b-143">Namespace</span></span><br/>                | <span data-ttu-id="8cb7b-144">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="8cb7b-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8cb7b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8cb7b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8cb7b-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8cb7b-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb7b-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cb7b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb7b-148">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="8cb7b-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
