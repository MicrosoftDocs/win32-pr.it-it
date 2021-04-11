---
description: Consente al proprietario del TPM di abilitare o riprendere il TPM.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Metodo Enable della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231695"
---
# <a name="enable-method-of-the-win32_tpm-class"></a><span data-ttu-id="3537c-103">Metodo Enable della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="3537c-103">Enable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="3537c-104">Il metodo **Enable** della classe [**\_ TPM Win32**](win32-tpm.md) consente al proprietario del TPM di abilitare o riprendere il TPM.</span><span class="sxs-lookup"><span data-stu-id="3537c-104">The **Enable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to enable or resume the TPM.</span></span>

<span data-ttu-id="3537c-105">Per eseguire questo metodo, il TPM deve avere già un proprietario.</span><span class="sxs-lookup"><span data-stu-id="3537c-105">To run this method, the TPM must already have an owner.</span></span> <span data-ttu-id="3537c-106">Per abilitare un TPM che non dispone già di un proprietario, utilizzare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="3537c-106">To enable a TPM that does not already have an owner, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3537c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3537c-107">Syntax</span></span>


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="3537c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3537c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3537c-109">*OwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3537c-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3537c-110">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="3537c-110">Type: **string**</span></span>

<span data-ttu-id="3537c-111">Stringa che identifica il proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="3537c-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="3537c-112">Questa stringa deve essere una stringa con codifica Base64 che contiene esattamente 20 byte di dati binari.</span><span class="sxs-lookup"><span data-stu-id="3537c-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="3537c-113">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="3537c-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="3537c-114">Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="3537c-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3537c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3537c-115">Return value</span></span>

<span data-ttu-id="3537c-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3537c-116">Type: **uint32**</span></span>

<span data-ttu-id="3537c-117">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="3537c-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="3537c-118">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="3537c-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="3537c-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3537c-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="3537c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3537c-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3537c-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3537c-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="3537c-122">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3537c-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="3537c-123"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="3537c-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="3537c-124">Il valore di autorizzazione del proprietario specificato non è in grado di eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3537c-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="3537c-125"><dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="3537c-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="3537c-126">Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="3537c-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="3537c-127">Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="3537c-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3537c-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="3537c-128">Remarks</span></span>

<span data-ttu-id="3537c-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3537c-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3537c-130">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3537c-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3537c-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3537c-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3537c-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3537c-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3537c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3537c-133">Requirements</span></span>



| <span data-ttu-id="3537c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3537c-134">Requirement</span></span> | <span data-ttu-id="3537c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3537c-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3537c-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3537c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3537c-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3537c-137">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3537c-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3537c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3537c-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3537c-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3537c-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3537c-140">Namespace</span></span><br/>                | <span data-ttu-id="3537c-141">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="3537c-141">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="3537c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3537c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3537c-143"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3537c-143"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="3537c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3537c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3537c-145"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="3537c-145"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3537c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3537c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3537c-147">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="3537c-147">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="3537c-148">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="3537c-148">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
