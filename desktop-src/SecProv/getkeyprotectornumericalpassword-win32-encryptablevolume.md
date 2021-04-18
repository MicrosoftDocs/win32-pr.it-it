---
description: Recupera la password numerica per una protezione con chiave specificata.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Metodo GetKeyProtectorNumericalPassword della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306396"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ed5c8-103">Metodo GetKeyProtectorNumericalPassword della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="ed5c8-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ed5c8-104">Il metodo **GetKeyProtectorNumericalPassword** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera la password numerica per una protezione con chiave specificata del tipo appropriato.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="ed5c8-105">L'identificatore della protezione con chiave deve fare riferimento a una protezione con chiave di tipo "password numerica".</span><span class="sxs-lookup"><span data-stu-id="ed5c8-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5c8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed5c8-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="ed5c8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed5c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed5c8-108">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed5c8-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed5c8-109">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="ed5c8-109">Type: **string**</span></span>

<span data-ttu-id="ed5c8-110">Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="ed5c8-111">*NumericalPassword* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed5c8-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed5c8-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="ed5c8-112">Type: **string**</span></span>

<span data-ttu-id="ed5c8-113">Stringa che rappresenta la password che può essere utilizzata per sbloccare il volume corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="ed5c8-114">La password numerica è 48 cifre.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="ed5c8-115">Queste cifre sono divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="ed5c8-116">Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="ed5c8-117">I gruppi di cifre sono separati da un trattino.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="ed5c8-118">Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" è il formato della password restituita.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed5c8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed5c8-119">Return value</span></span>

<span data-ttu-id="ed5c8-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5c8-120">Type: **uint32**</span></span>

<span data-ttu-id="ed5c8-121">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ed5c8-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed5c8-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="ed5c8-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed5c8-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed5c8-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5c8-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="ed5c8-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="ed5c8-126"><dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5c8-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="ed5c8-127">Il volume è bloccato.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="ed5c8-128"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5c8-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="ed5c8-129">Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password".</span><span class="sxs-lookup"><span data-stu-id="ed5c8-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="ed5c8-130"><dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="ed5c8-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="ed5c8-131">Nel volume non è abilitato BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="ed5c8-132">Aggiungere una protezione con chiave per abilitare BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ed5c8-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed5c8-133">Remarks</span></span>

<span data-ttu-id="ed5c8-134">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed5c8-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed5c8-135">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ed5c8-136">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ed5c8-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed5c8-137">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ed5c8-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed5c8-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed5c8-138">Requirements</span></span>



| <span data-ttu-id="ed5c8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed5c8-139">Requirement</span></span> | <span data-ttu-id="ed5c8-140">Valore</span><span class="sxs-lookup"><span data-stu-id="ed5c8-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5c8-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed5c8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ed5c8-142">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="ed5c8-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed5c8-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed5c8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ed5c8-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed5c8-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed5c8-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed5c8-145">Namespace</span></span><br/>                | <span data-ttu-id="ed5c8-146">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ed5c8-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ed5c8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ed5c8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed5c8-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed5c8-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed5c8-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed5c8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5c8-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ed5c8-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
