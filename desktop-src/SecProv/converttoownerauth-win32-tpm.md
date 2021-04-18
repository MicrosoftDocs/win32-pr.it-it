---
description: Converte un input di passphrase fornito dall'utente in un'autorizzazione proprietaria di 20 byte che può essere utilizzata per interagire con il TPM. Per i metodi come TakeOwnership e ResetAuthLockOut è necessario il valore di autorizzazione del proprietario risultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Metodo ConvertToOwnerAuth della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314672"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="914f6-104">Metodo ConvertToOwnerAuth della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="914f6-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="914f6-105">Il metodo **ConvertToOwnerAuth** della classe [**\_ TPM Win32**](win32-tpm.md) converte un input di passphrase fornito dall'utente in un'autorizzazione proprietaria di 20 byte che può essere utilizzata per interagire con il TPM.</span><span class="sxs-lookup"><span data-stu-id="914f6-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="914f6-106">Per i metodi come [**TakeOwnership**](takeownership-win32-tpm.md) e [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) è necessario il valore di autorizzazione del proprietario risultante.</span><span class="sxs-lookup"><span data-stu-id="914f6-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="914f6-107">Il processo di conversione segue le specifiche del [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span><span class="sxs-lookup"><span data-stu-id="914f6-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="914f6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="914f6-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="914f6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="914f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="914f6-110">*OwnerPassPhrase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="914f6-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="914f6-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="914f6-111">Type: **string**</span></span>

<span data-ttu-id="914f6-112">Stringa da convertire in un valore di autorizzazione del proprietario.</span><span class="sxs-lookup"><span data-stu-id="914f6-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="914f6-113">La stringa può contenere un numero qualsiasi di caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="914f6-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="914f6-114">*OwnerAuth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="914f6-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="914f6-115">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="914f6-115">Type: **string**</span></span>

<span data-ttu-id="914f6-116">Stringa derivata dal parametro *OwnerPassPhrase* .</span><span class="sxs-lookup"><span data-stu-id="914f6-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="914f6-117">Questo valore è un valore binario a 20 byte codificato in una stringa Base64 con terminazione **null** a 28 byte.</span><span class="sxs-lookup"><span data-stu-id="914f6-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="914f6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="914f6-118">Return value</span></span>

<span data-ttu-id="914f6-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="914f6-119">Type: **uint32**</span></span>

<span data-ttu-id="914f6-120">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="914f6-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="914f6-121">Nelle tabelle seguenti sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="914f6-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="914f6-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="914f6-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="914f6-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="914f6-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="914f6-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="914f6-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="914f6-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="914f6-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="914f6-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="914f6-126">Remarks</span></span>

<span data-ttu-id="914f6-127">Una stringa codificata UTF-16LE Unicode viene convertita nel valore di autorizzazione del proprietario del TPM a 20 byte prendendo l'hash SHA-1 della rappresentazione binaria della stringa.</span><span class="sxs-lookup"><span data-stu-id="914f6-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="914f6-128">La terminazione **null** della stringa Unicode non è inclusa nell'hash.</span><span class="sxs-lookup"><span data-stu-id="914f6-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="914f6-129">Nessun salt viene utilizzato nell'hash SHA-1.</span><span class="sxs-lookup"><span data-stu-id="914f6-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="914f6-130">Ad esempio, per convertire la passphrase del proprietario del TPM "1Sample" in un valore di autorizzazione del proprietario del TPM, l'hash SHA-1 viene ricavato dal flusso di byte seguente:</span><span class="sxs-lookup"><span data-stu-id="914f6-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="914f6-131">Per convertire una passphrase di lunghezza zero in un valore di autorizzazione del proprietario, l'hash SHA-1 viene accettato dal flusso di byte **null** .</span><span class="sxs-lookup"><span data-stu-id="914f6-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="914f6-132">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="914f6-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="914f6-133">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="914f6-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="914f6-134">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="914f6-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="914f6-135">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="914f6-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="914f6-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="914f6-136">Requirements</span></span>



| <span data-ttu-id="914f6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="914f6-137">Requirement</span></span> | <span data-ttu-id="914f6-138">Valore</span><span class="sxs-lookup"><span data-stu-id="914f6-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="914f6-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="914f6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="914f6-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="914f6-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="914f6-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="914f6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="914f6-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="914f6-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="914f6-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="914f6-143">Namespace</span></span><br/>                | <span data-ttu-id="914f6-144">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="914f6-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="914f6-145">MOF</span><span class="sxs-lookup"><span data-stu-id="914f6-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="914f6-146"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="914f6-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="914f6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="914f6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="914f6-148"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="914f6-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914f6-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="914f6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="914f6-150">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="914f6-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="914f6-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="914f6-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 
