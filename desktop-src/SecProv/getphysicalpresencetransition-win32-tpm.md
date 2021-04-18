---
description: Indica l'azione dell'utente necessaria per eseguire l'operazione di presenza fisica Trusted Platform Module (TPM). Usare il metodo SetPhysicalPresenceRequest per richiedere un'operazione.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Metodo GetPhysicalPresenceTransition della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316102"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="8082d-104">Metodo GetPhysicalPresenceTransition della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="8082d-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8082d-105">Il metodo **GetPhysicalPresenceTransition** della classe [**\_ TPM Win32**](win32-tpm.md) indica l'azione dell'utente necessaria per eseguire l'operazione di presenza fisica Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="8082d-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="8082d-106">Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8082d-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="8082d-107">L'azione richiesta dell'utente è impostata per il computer al momento della fabbricazione.</span><span class="sxs-lookup"><span data-stu-id="8082d-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="8082d-108">In genere è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="8082d-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8082d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8082d-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="8082d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8082d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8082d-111">*Transizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8082d-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8082d-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8082d-112">Type: **uint32**</span></span>

<span data-ttu-id="8082d-113">Valore integer che specifica la transizione necessaria per eseguire un'operazione di presenza fisica del TPM.</span><span class="sxs-lookup"><span data-stu-id="8082d-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="8082d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8082d-114">Value</span></span>                                                                        | <span data-ttu-id="8082d-115">Significato</span><span class="sxs-lookup"><span data-stu-id="8082d-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8082d-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="8082d-117">Non è necessaria alcuna azione dell'utente per eseguire un'operazione di presenza fisica TPM.</span><span class="sxs-lookup"><span data-stu-id="8082d-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="8082d-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8082d-119">Per eseguire un'operazione di presenza fisica TPM, l'utente deve arrestare il computer e quindi riattivarlo utilizzando il pulsante di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="8082d-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="8082d-120">L'utente deve essere fisicamente presente nel computer per accettare o rifiutare la modifica quando richiesto dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="8082d-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="8082d-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8082d-122">Per eseguire un'operazione di presenza fisica TPM, l'utente deve riavviare il computer utilizzando un riavvio a caldo.</span><span class="sxs-lookup"><span data-stu-id="8082d-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="8082d-123">L'utente deve essere fisicamente presente nel computer per accettare o rifiutare la modifica quando richiesto dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="8082d-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="8082d-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8082d-125">L'azione obbligatoria dell'utente è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="8082d-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8082d-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8082d-126">Return value</span></span>

<span data-ttu-id="8082d-127">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8082d-127">Type: **uint32**</span></span>

<span data-ttu-id="8082d-128">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="8082d-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8082d-129">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="8082d-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="8082d-130">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8082d-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="8082d-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8082d-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8082d-132"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="8082d-133">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="8082d-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="8082d-134"><dt>**TPM \_ \_ \_ \_ Errore ACPI di E PPI**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="8082d-135">Si è verificato un errore hardware.</span><span class="sxs-lookup"><span data-stu-id="8082d-135">A hardware failure occurred.</span></span> <span data-ttu-id="8082d-136">Per ulteriori informazioni, consultare il produttore del computer.</span><span class="sxs-lookup"><span data-stu-id="8082d-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8082d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="8082d-137">Remarks</span></span>

<span data-ttu-id="8082d-138">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8082d-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8082d-139">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8082d-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8082d-140">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8082d-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8082d-141">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8082d-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8082d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8082d-142">Requirements</span></span>



| <span data-ttu-id="8082d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8082d-143">Requirement</span></span> | <span data-ttu-id="8082d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="8082d-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8082d-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8082d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8082d-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8082d-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8082d-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8082d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8082d-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8082d-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8082d-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8082d-149">Namespace</span></span><br/>                | <span data-ttu-id="8082d-150">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="8082d-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8082d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="8082d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8082d-152"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8082d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="8082d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8082d-154"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="8082d-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8082d-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8082d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8082d-156">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="8082d-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="8082d-157">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="8082d-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
