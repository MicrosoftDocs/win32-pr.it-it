---
description: Reimposta il TPM sullo stato predefinito della factory.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Metodo Clear della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232930"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="52034-103">Metodo Clear della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="52034-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="52034-104">Il metodo **Clear** della classe [**\_ TPM Win32**](win32-tpm.md) Reimposta il TPM sullo stato predefinito della factory.</span><span class="sxs-lookup"><span data-stu-id="52034-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="52034-105">Un proprietario del TPM può utilizzare questo metodo per annullare la proprietà del TPM e invalidare i materiali crittografici creati dal proprietario precedente.</span><span class="sxs-lookup"><span data-stu-id="52034-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="52034-106">Questo metodo sospende BitLocker se la chiamata a può causare la richiesta del ripristino BitLocker.</span><span class="sxs-lookup"><span data-stu-id="52034-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="52034-107">BitLocker verrà ripreso automaticamente dopo il provisioning del TPM.</span><span class="sxs-lookup"><span data-stu-id="52034-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="52034-108">Deselezionando il TPM, si perderanno tutte le chiavi TPM create e utilizzate dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="52034-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="52034-109">Se queste chiavi sono state usate per crittografare i dati, assicurarsi di disporre di un altro modo per accedere ai dati prima di cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="52034-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="52034-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52034-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="52034-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="52034-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52034-112">*OwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="52034-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="52034-113">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="52034-113">Type: **string**</span></span>

<span data-ttu-id="52034-114">Stringa che identifica il proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="52034-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="52034-115">Questa stringa deve essere una stringa con codifica Base64 che contiene esattamente 20 byte di dati binari.</span><span class="sxs-lookup"><span data-stu-id="52034-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="52034-116">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="52034-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="52034-117">Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="52034-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52034-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52034-118">Return value</span></span>

<span data-ttu-id="52034-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52034-119">Type: **uint32**</span></span>

<span data-ttu-id="52034-120">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="52034-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="52034-121">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="52034-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="52034-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="52034-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="52034-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52034-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52034-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="52034-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="52034-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="52034-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="52034-126"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="52034-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="52034-127">Il valore di autorizzazione del proprietario specificato non è in grado di eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="52034-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="52034-128"><dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="52034-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="52034-129">Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="52034-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="52034-130">Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="52034-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52034-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="52034-131">Remarks</span></span>

<span data-ttu-id="52034-132">L'esecuzione di questo metodo consente di preparare un computer dotato di TPM per il riciclo.</span><span class="sxs-lookup"><span data-stu-id="52034-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="52034-133">Per cancellare il TPM ma che non dispone più dell'autorizzazione del proprietario del TPM, è necessario l'accesso fisico al computer.</span><span class="sxs-lookup"><span data-stu-id="52034-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="52034-134">Il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) include funzionalità che consentono di cancellare il TPM senza autorizzazione del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="52034-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="52034-135">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52034-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52034-136">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="52034-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="52034-137">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="52034-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52034-138">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="52034-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52034-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52034-139">Requirements</span></span>



| <span data-ttu-id="52034-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="52034-140">Requirement</span></span> | <span data-ttu-id="52034-141">Valore</span><span class="sxs-lookup"><span data-stu-id="52034-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="52034-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52034-142">Minimum supported client</span></span><br/> | <span data-ttu-id="52034-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52034-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="52034-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52034-144">Minimum supported server</span></span><br/> | <span data-ttu-id="52034-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="52034-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="52034-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52034-146">Namespace</span></span><br/>                | <span data-ttu-id="52034-147">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="52034-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="52034-148">MOF</span><span class="sxs-lookup"><span data-stu-id="52034-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52034-149"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52034-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="52034-150">DLL</span><span class="sxs-lookup"><span data-stu-id="52034-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52034-151"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="52034-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52034-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52034-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52034-153">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="52034-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
