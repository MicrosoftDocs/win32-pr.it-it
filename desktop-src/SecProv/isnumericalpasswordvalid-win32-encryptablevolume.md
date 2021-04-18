---
description: Indica se la password numerica soddisfa i requisiti di formato speciali per questo valore di autenticazione.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Metodo IsNumericalPasswordValid della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315342"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="74bd5-103">Metodo IsNumericalPasswordValid della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="74bd5-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="74bd5-104">Il metodo **IsNumericalPasswordValid** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se la password numerica soddisfa i requisiti di formato speciali per questo valore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="74bd5-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74bd5-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="74bd5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74bd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74bd5-107">*NumericalPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74bd5-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74bd5-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="74bd5-108">Type: **string**</span></span>

<span data-ttu-id="74bd5-109">Stringa che specifica la password numerica.</span><span class="sxs-lookup"><span data-stu-id="74bd5-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="74bd5-110">La password numerica deve contenere 48 cifre.</span><span class="sxs-lookup"><span data-stu-id="74bd5-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="74bd5-111">Queste cifre possono essere divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="74bd5-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="74bd5-112">Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 720896.</span><span class="sxs-lookup"><span data-stu-id="74bd5-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="74bd5-113">Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="74bd5-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="74bd5-114">I gruppi di cifre possono essere separati facoltativamente da uno spazio o un trattino.</span><span class="sxs-lookup"><span data-stu-id="74bd5-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="74bd5-115">Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oppure "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere anche password numeriche valide.</span><span class="sxs-lookup"><span data-stu-id="74bd5-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="74bd5-116">*IsNumericalPasswordValid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74bd5-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74bd5-117">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74bd5-117">Type: **boolean**</span></span>

<span data-ttu-id="74bd5-118">Valore booleano che è true se la password numerica soddisfa i requisiti di formato speciali per questo valore di autenticazione; in caso contrario, il valore è false.</span><span class="sxs-lookup"><span data-stu-id="74bd5-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74bd5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74bd5-119">Return value</span></span>

<span data-ttu-id="74bd5-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74bd5-120">Type: **uint32**</span></span>

<span data-ttu-id="74bd5-121">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74bd5-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="74bd5-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="74bd5-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="74bd5-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74bd5-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="74bd5-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="74bd5-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="74bd5-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="74bd5-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74bd5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="74bd5-126">Remarks</span></span>

<span data-ttu-id="74bd5-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="74bd5-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="74bd5-128">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="74bd5-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="74bd5-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="74bd5-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="74bd5-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="74bd5-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74bd5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74bd5-131">Requirements</span></span>



| <span data-ttu-id="74bd5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="74bd5-132">Requirement</span></span> | <span data-ttu-id="74bd5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="74bd5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74bd5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74bd5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="74bd5-135">Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="74bd5-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="74bd5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74bd5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="74bd5-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74bd5-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74bd5-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74bd5-138">Namespace</span></span><br/>                | <span data-ttu-id="74bd5-139">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="74bd5-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="74bd5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="74bd5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74bd5-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74bd5-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74bd5-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74bd5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bd5-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="74bd5-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
