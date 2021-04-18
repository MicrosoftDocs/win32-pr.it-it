---
description: Consente al proprietario del TPM di disabilitare o sospendere il TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Metodo Disable della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306406"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="b17a8-103">Metodo Disable della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="b17a8-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b17a8-104">Il metodo **Disable** della classe [**\_ TPM Win32**](win32-tpm.md) consente al proprietario del TPM di disabilitare o sospendere il TPM.</span><span class="sxs-lookup"><span data-stu-id="b17a8-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="b17a8-105">Questo metodo sospende BitLocker se la chiamata a può causare la richiesta del ripristino BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b17a8-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="b17a8-106">BitLocker verrà ripreso automaticamente dopo il provisioning del TPM.</span><span class="sxs-lookup"><span data-stu-id="b17a8-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b17a8-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="b17a8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b17a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17a8-109">*OwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b17a8-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b17a8-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="b17a8-110">Type: **string**</span></span>

<span data-ttu-id="b17a8-111">Stringa che identifica il proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="b17a8-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="b17a8-112">Questa stringa deve essere una stringa con codifica Base64 che contiene esattamente 20 byte di dati binari.</span><span class="sxs-lookup"><span data-stu-id="b17a8-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="b17a8-113">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="b17a8-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="b17a8-114">Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="b17a8-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b17a8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b17a8-115">Return value</span></span>

<span data-ttu-id="b17a8-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b17a8-116">Type: **uint32**</span></span>

<span data-ttu-id="b17a8-117">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="b17a8-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b17a8-118">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="b17a8-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="b17a8-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b17a8-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="b17a8-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b17a8-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b17a8-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="b17a8-122">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b17a8-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="b17a8-123"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="b17a8-124">Il valore di autorizzazione del proprietario specificato non è in grado di eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b17a8-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="b17a8-125"><dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="b17a8-126">Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="b17a8-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="b17a8-127">Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="b17a8-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b17a8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="b17a8-128">Remarks</span></span>

<span data-ttu-id="b17a8-129">Per disabilitare il TPM senza avere il valore di autorizzazione del proprietario del TPM, usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="b17a8-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="b17a8-130">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b17a8-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b17a8-131">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b17a8-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b17a8-132">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b17a8-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b17a8-133">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b17a8-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b17a8-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b17a8-134">Requirements</span></span>



| <span data-ttu-id="b17a8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17a8-135">Requirement</span></span> | <span data-ttu-id="b17a8-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b17a8-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b17a8-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b17a8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b17a8-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b17a8-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b17a8-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b17a8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b17a8-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b17a8-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b17a8-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b17a8-141">Namespace</span></span><br/>                | <span data-ttu-id="b17a8-142">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="b17a8-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b17a8-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b17a8-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b17a8-144"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b17a8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b17a8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17a8-146"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="b17a8-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17a8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b17a8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17a8-148">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="b17a8-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="b17a8-149">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="b17a8-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
