---
description: Il metodo disattivato della \_ classe TPM Win32 indica se il dispositivo è attivato.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Metodo disattivato della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232928"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="28885-103">Metodo disattivato della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="28885-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="28885-104">Il metodo **disattivato** della classe [**\_ TPM Win32**](win32-tpm.md) indica se il dispositivo è attivato.</span><span class="sxs-lookup"><span data-stu-id="28885-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="28885-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28885-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="28885-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28885-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28885-107">*Disattivato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28885-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28885-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="28885-108">Type: **boolean**</span></span>

<span data-ttu-id="28885-109">Se **true**, il dispositivo viene attivato.</span><span class="sxs-lookup"><span data-stu-id="28885-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28885-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28885-110">Return value</span></span>

<span data-ttu-id="28885-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28885-111">Type: **uint32**</span></span>

<span data-ttu-id="28885-112">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="28885-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="28885-113">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="28885-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="28885-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="28885-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="28885-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28885-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="28885-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="28885-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="28885-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="28885-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28885-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="28885-118">Remarks</span></span>

<span data-ttu-id="28885-119">La disattivazione è simile a disabilitata, ma sono possibili modifiche allo stato operativo.</span><span class="sxs-lookup"><span data-stu-id="28885-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="28885-120">In base alla specifica Trusted Computing Group (TCG) v 1.2 sono disponibili solo i comandi seguenti quando il dispositivo è in uno stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="28885-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="28885-121">\_CONTINUESELFTEST TPM</span><span class="sxs-lookup"><span data-stu-id="28885-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="28885-122">\_DSAP TPM</span><span class="sxs-lookup"><span data-stu-id="28885-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="28885-123">\_FLUSHSPECIFIC TPM</span><span class="sxs-lookup"><span data-stu-id="28885-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="28885-124">Getfunzionalità TPM \_</span><span class="sxs-lookup"><span data-stu-id="28885-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="28885-125">\_GETTESTRESULT TPM</span><span class="sxs-lookup"><span data-stu-id="28885-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="28885-126">\_Init TPM</span><span class="sxs-lookup"><span data-stu-id="28885-126">TPM\_Init</span></span>
-   <span data-ttu-id="28885-127">\_OIAP TPM</span><span class="sxs-lookup"><span data-stu-id="28885-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="28885-128">\_OSAP TPM</span><span class="sxs-lookup"><span data-stu-id="28885-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="28885-129">\_OWNERSETDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="28885-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="28885-130">\_Reimpostazione PCR TPM \_</span><span class="sxs-lookup"><span data-stu-id="28885-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="28885-131">\_PHYSICALDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="28885-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="28885-132">\_PHYSICALENABLE TPM</span><span class="sxs-lookup"><span data-stu-id="28885-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="28885-133">\_PHYSICALSETDEACTIVATED TPM</span><span class="sxs-lookup"><span data-stu-id="28885-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="28885-134">\_Ripristino TPM</span><span class="sxs-lookup"><span data-stu-id="28885-134">TPM\_Reset</span></span>
-   <span data-ttu-id="28885-135">\_SAVESTATE TPM</span><span class="sxs-lookup"><span data-stu-id="28885-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="28885-136">\_SELFTESTFULL TPM</span><span class="sxs-lookup"><span data-stu-id="28885-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="28885-137">Funzionalità del TPM \_</span><span class="sxs-lookup"><span data-stu-id="28885-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="28885-138">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="28885-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="28885-139">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="28885-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="28885-140">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="28885-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="28885-141">\_Avvio TPM</span><span class="sxs-lookup"><span data-stu-id="28885-141">TPM\_Startup</span></span>
-   <span data-ttu-id="28885-142">\_TAKEOWNERSHIP TPM</span><span class="sxs-lookup"><span data-stu-id="28885-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="28885-143">\_Handle di terminazione TPM \_</span><span class="sxs-lookup"><span data-stu-id="28885-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="28885-144">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="28885-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="28885-145">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="28885-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="28885-146">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="28885-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="28885-147">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="28885-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28885-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28885-148">Requirements</span></span>



| <span data-ttu-id="28885-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="28885-149">Requirement</span></span> | <span data-ttu-id="28885-150">Valore</span><span class="sxs-lookup"><span data-stu-id="28885-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="28885-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28885-151">Minimum supported client</span></span><br/> | <span data-ttu-id="28885-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28885-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="28885-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28885-153">Minimum supported server</span></span><br/> | <span data-ttu-id="28885-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28885-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="28885-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28885-155">Namespace</span></span><br/>                | <span data-ttu-id="28885-156">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="28885-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="28885-157">MOF</span><span class="sxs-lookup"><span data-stu-id="28885-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28885-158"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28885-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="28885-159">DLL</span><span class="sxs-lookup"><span data-stu-id="28885-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28885-160"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="28885-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28885-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28885-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28885-162">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="28885-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
