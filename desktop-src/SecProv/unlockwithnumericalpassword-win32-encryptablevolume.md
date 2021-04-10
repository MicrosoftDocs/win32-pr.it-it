---
description: Usa una password numerica specificata per accedere al contenuto di un volume di dati.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Metodo UnlockWithNumericalPassword della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878918"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2bcaa-103">Metodo UnlockWithNumericalPassword della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="2bcaa-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2bcaa-104">Il metodo **UnlockWithNumericalPassword** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa una password numerica specificata per accedere al contenuto di un volume di dati.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="2bcaa-105">La chiave di crittografia del volume deve essere stata protetta con una o più protezioni con chiave di tipo "password numerica" (usando il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) per poter sbloccare il volume con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="2bcaa-106">Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "</span><span class="sxs-lookup"><span data-stu-id="2bcaa-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2bcaa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bcaa-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="2bcaa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2bcaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bcaa-109">*NumericalPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2bcaa-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcaa-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-110">Type: **string**</span></span>

<span data-ttu-id="2bcaa-111">Stringa che specifica la password numerica.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="2bcaa-112">La password numerica deve contenere 48 cifre.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="2bcaa-113">Queste cifre possono essere divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="2bcaa-114">Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 65536.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="2bcaa-115">Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="2bcaa-116">I gruppi di cifre possono essere separati facoltativamente da uno spazio o un trattino.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="2bcaa-117">Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oppure "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere anche password numeriche valide.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bcaa-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2bcaa-118">Return value</span></span>

<span data-ttu-id="2bcaa-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-119">Type: **uint32**</span></span>

<span data-ttu-id="2bcaa-120">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="2bcaa-121">Se il volume è già sbloccato e non si verificano altri errori, questo metodo restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="2bcaa-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2bcaa-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="2bcaa-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bcaa-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2bcaa-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="2bcaa-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="2bcaa-126"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="2bcaa-127">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2bcaa-128">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="2bcaa-129"><dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="2bcaa-130">Il volume non dispone di una protezione con chiave di tipo "password numerica".</span><span class="sxs-lookup"><span data-stu-id="2bcaa-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="2bcaa-131">Il formato del parametro *NumericalPassword* è valido, ma non è possibile usare una password numerica per sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="2bcaa-132"><dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="2bcaa-133">Il parametro *NumericalPassword* non è in grado di sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="2bcaa-134">Sono presenti una o più protezioni con chiave di tipo "password numerica", ma il parametro *NumericalPassword* specificato non è in grado di sbloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="2bcaa-135"><dt>**FVE \_ E \_ \_ \_ formato della PASSWORD non valido**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="2bcaa-136">Il formato del parametro *NumericalPassword* non è valido.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2bcaa-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bcaa-137">Remarks</span></span>

<span data-ttu-id="2bcaa-138">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2bcaa-139">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2bcaa-140">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2bcaa-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2bcaa-141">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2bcaa-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bcaa-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bcaa-142">Requirements</span></span>



| <span data-ttu-id="2bcaa-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bcaa-143">Requirement</span></span> | <span data-ttu-id="2bcaa-144">Valore</span><span class="sxs-lookup"><span data-stu-id="2bcaa-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcaa-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bcaa-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2bcaa-146">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="2bcaa-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2bcaa-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bcaa-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2bcaa-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2bcaa-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bcaa-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2bcaa-149">Namespace</span></span><br/>                | <span data-ttu-id="2bcaa-150">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2bcaa-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2bcaa-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2bcaa-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bcaa-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bcaa-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bcaa-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bcaa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcaa-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="2bcaa-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
