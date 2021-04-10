---
description: Protegge la chiave di crittografia del volume con una password a 48 cifre formattata in modo specifico.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Metodo ProtectKeyWithNumericalPassword della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883597"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5d614-103">Metodo ProtectKeyWithNumericalPassword della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="5d614-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5d614-104">Il metodo **ProtectKeyWithNumericalPassword** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume con una password a 48 cifre formattata in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="5d614-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="5d614-105">Questa password numerica può essere utilizzata per il recupero dagli errori di autenticazione di altre protezioni con chiave (ad esempio, TPM).</span><span class="sxs-lookup"><span data-stu-id="5d614-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="5d614-106">Viene creata una protezione con chiave di tipo "password numerica" per il volume.</span><span class="sxs-lookup"><span data-stu-id="5d614-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="5d614-107">Usare il metodo [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) per convalidare il formato della password numerica.</span><span class="sxs-lookup"><span data-stu-id="5d614-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d614-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d614-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5d614-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d614-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d614-110">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5d614-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d614-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="5d614-111">Type: **string**</span></span>

<span data-ttu-id="5d614-112">Stringa che specifica un identificatore assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="5d614-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="5d614-113">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="5d614-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="5d614-114">*NumericalPassword* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5d614-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5d614-115">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="5d614-115">Type: **string**</span></span>

<span data-ttu-id="5d614-116">Stringa che specifica la password numerica 48-digit formattata in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="5d614-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="5d614-117">La password numerica deve contenere 48 cifre.</span><span class="sxs-lookup"><span data-stu-id="5d614-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="5d614-118">Queste cifre possono essere divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="5d614-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="5d614-119">Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 720896.</span><span class="sxs-lookup"><span data-stu-id="5d614-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="5d614-120">Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="5d614-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="5d614-121">I gruppi di cifre possono essere separati facoltativamente da uno spazio o un trattino.</span><span class="sxs-lookup"><span data-stu-id="5d614-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="5d614-122">Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oppure "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere anche password numeriche valide.</span><span class="sxs-lookup"><span data-stu-id="5d614-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="5d614-123">Se non viene specificata alcuna password numerica, ne viene generata una in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="5d614-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="5d614-124">Usare il metodo [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) per ottenere la password generata in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="5d614-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="5d614-125">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5d614-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d614-126">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="5d614-126">Type: **string**</span></span>

<span data-ttu-id="5d614-127">Stringa che rappresenta l'identificatore univoco associato alla protezione creata e che può essere utilizzata per gestire la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="5d614-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="5d614-128">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="5d614-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d614-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d614-129">Return value</span></span>

<span data-ttu-id="5d614-130">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d614-130">Type: **uint32**</span></span>

<span data-ttu-id="5d614-131">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5d614-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5d614-132">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d614-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="5d614-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d614-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d614-134"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5d614-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="5d614-135">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5d614-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="5d614-136"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="5d614-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="5d614-137">Il formato del parametro *NumericalPassword* non è valido.</span><span class="sxs-lookup"><span data-stu-id="5d614-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="5d614-138"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5d614-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="5d614-139">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="5d614-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5d614-140"><dt>**FVE \_ E \_ \_ \_ formato della PASSWORD non valido**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="5d614-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="5d614-141">Il formato del parametro *NumericalPassword* non è valido.</span><span class="sxs-lookup"><span data-stu-id="5d614-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5d614-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d614-142">Remarks</span></span>

<span data-ttu-id="5d614-143">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5d614-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5d614-144">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5d614-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5d614-145">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5d614-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5d614-146">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5d614-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d614-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d614-147">Requirements</span></span>



| <span data-ttu-id="5d614-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d614-148">Requirement</span></span> | <span data-ttu-id="5d614-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5d614-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d614-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d614-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5d614-151">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="5d614-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5d614-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d614-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5d614-153">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d614-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d614-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5d614-154">Namespace</span></span><br/>                | <span data-ttu-id="5d614-155">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5d614-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5d614-156">MOF</span><span class="sxs-lookup"><span data-stu-id="5d614-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d614-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d614-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d614-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d614-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d614-159">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5d614-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
