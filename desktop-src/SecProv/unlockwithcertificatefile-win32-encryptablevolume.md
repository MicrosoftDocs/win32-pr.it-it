---
description: Usa il file di certificato fornito per ottenere la chiave derivata e sbloccare il volume crittografato.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Metodo UnlockWithCertificateFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317685"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2b6df-103">Metodo UnlockWithCertificateFile della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="2b6df-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2b6df-104">Il metodo **UnlockWithCertificateFile** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa il file di [*certificato*](../secgloss/c-gly.md) fornito per ottenere la chiave derivata e sbloccare il volume crittografato.</span><span class="sxs-lookup"><span data-stu-id="2b6df-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="2b6df-105">Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "</span><span class="sxs-lookup"><span data-stu-id="2b6df-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2b6df-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b6df-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="2b6df-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b6df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6df-108">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b6df-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6df-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="2b6df-109">Type: **string**</span></span>

<span data-ttu-id="2b6df-110">Stringa che specifica il percorso e il nome del file con estensione cer utilizzato per recuperare l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="2b6df-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="2b6df-111">Un certificato di [*crittografia*](../secgloss/e-gly.md) deve essere esportato in formato cer ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) binario con codifica [*x. 509*](../secgloss/x-gly.md) o con codifica base-64 x. 509).</span><span class="sxs-lookup"><span data-stu-id="2b6df-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="2b6df-112">Il certificato di crittografia può essere generato da Microsoft PKI, PKI di terze parti o autofirmato.</span><span class="sxs-lookup"><span data-stu-id="2b6df-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="2b6df-113">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b6df-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6df-114">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="2b6df-114">Type: **string**</span></span>

<span data-ttu-id="2b6df-115">Stringa di identificazione personale specificata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2b6df-115">A user-specified personal identification string.</span></span> <span data-ttu-id="2b6df-116">Questa stringa deve essere composta da una sequenza di 4 a 20 cifre.</span><span class="sxs-lookup"><span data-stu-id="2b6df-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="2b6df-117">Questa stringa viene usata per autenticare automaticamente il [*provider di archiviazione chiavi*](../secgloss/k-gly.md) (KSP) se usato con una [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2b6df-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6df-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b6df-118">Return value</span></span>

<span data-ttu-id="2b6df-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b6df-119">Type: **uint32**</span></span>

<span data-ttu-id="2b6df-120">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2b6df-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2b6df-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b6df-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="2b6df-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b6df-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b6df-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="2b6df-124">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="2b6df-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="2b6df-125"><dt>**Errore \_ Il \_ file \_ non**</dt> è stato trovato <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="2b6df-126">Il sistema non è in grado di archiviare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="2b6df-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="2b6df-127"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="2b6df-128">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2b6df-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2b6df-129">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2b6df-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="2b6df-130"><dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="2b6df-131">Il volume non può essere sbloccato con le informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="2b6df-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="2b6df-132"><dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="2b6df-133">La protezione con chiave specificata non esiste nel volume.</span><span class="sxs-lookup"><span data-stu-id="2b6df-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="2b6df-134">È necessario immettere un'altra protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="2b6df-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="2b6df-135"><dt>**FVE \_ Autenticazione di E \_ PRIVATEKEY \_ \_ non riuscita**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="2b6df-136">Non è stato possibile autorizzare la [*chiave privata*](../secgloss/p-gly.md)associata al certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="2b6df-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="2b6df-137">L'autorizzazione della chiave privata non è stata specificata o l'autorizzazione fornita non è valida.</span><span class="sxs-lookup"><span data-stu-id="2b6df-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b6df-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b6df-138">Requirements</span></span>



| <span data-ttu-id="2b6df-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b6df-139">Requirement</span></span> | <span data-ttu-id="2b6df-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2b6df-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6df-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b6df-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6df-142">Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]</span><span class="sxs-lookup"><span data-stu-id="2b6df-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2b6df-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b6df-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6df-144">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b6df-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2b6df-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b6df-145">Namespace</span></span><br/>                | <span data-ttu-id="2b6df-146">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2b6df-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2b6df-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2b6df-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b6df-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b6df-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6df-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b6df-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6df-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="2b6df-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
