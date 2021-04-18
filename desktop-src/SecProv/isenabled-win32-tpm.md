---
description: Il Metodo IsEnabled della \_ classe TPM Win32 indica se il dispositivo è abilitato. Questo valore può essere modificato dai metodi Enable e Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Metodo IsEnabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306388"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="4be45-104">Metodo IsEnabled della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="4be45-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="4be45-105">Il metodo **IsEnabled** della classe [**\_ TPM Win32**](win32-tpm.md) indica se il dispositivo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4be45-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="4be45-106">Questo valore può essere modificato dai metodi [**Enable**](enable-win32-tpm.md) e [**Disable**](disable-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="4be45-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be45-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4be45-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4be45-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4be45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be45-109">*IsEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4be45-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4be45-110">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4be45-110">Type: **boolean**</span></span>

<span data-ttu-id="4be45-111">Se **true**, il dispositivo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4be45-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be45-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4be45-112">Return value</span></span>

<span data-ttu-id="4be45-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4be45-113">Type: **uint32**</span></span>

<span data-ttu-id="4be45-114">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="4be45-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="4be45-115">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="4be45-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="4be45-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4be45-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4be45-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4be45-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4be45-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4be45-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4be45-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="4be45-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4be45-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4be45-120">Remarks</span></span>

<span data-ttu-id="4be45-121">In base alla specifica Trusted Computing Group (TCG) v 1.2 sono disponibili solo i comandi seguenti quando il dispositivo è in uno stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="4be45-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="4be45-122">\_CONTINUESELFTEST TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="4be45-123">\_DSAP TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="4be45-124">\_FLUSHSPECIFIC TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="4be45-125">Getfunzionalità TPM \_</span><span class="sxs-lookup"><span data-stu-id="4be45-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="4be45-126">\_GETTESTRESULT TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="4be45-127">\_Init TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-127">TPM\_Init</span></span>
-   <span data-ttu-id="4be45-128">\_OIAP TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="4be45-129">\_OSAP TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="4be45-130">\_OWNERSETDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="4be45-131">\_Reimpostazione PCR TPM \_</span><span class="sxs-lookup"><span data-stu-id="4be45-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="4be45-132">\_PHYSICALDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="4be45-133">\_PHYSICALENABLE TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="4be45-134">\_PHYSICALSETDEACTIVATED TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="4be45-135">\_Ripristino TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-135">TPM\_Reset</span></span>
-   <span data-ttu-id="4be45-136">\_SAVESTATE TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="4be45-137">\_SELFTESTFULL TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="4be45-138">Funzionalità del TPM \_</span><span class="sxs-lookup"><span data-stu-id="4be45-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="4be45-139">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="4be45-140">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="4be45-141">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="4be45-142">\_Avvio TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-142">TPM\_Startup</span></span>
-   <span data-ttu-id="4be45-143">\_TAKEOWNERSHIP TPM</span><span class="sxs-lookup"><span data-stu-id="4be45-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="4be45-144">\_Handle di terminazione TPM \_</span><span class="sxs-lookup"><span data-stu-id="4be45-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="4be45-145">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4be45-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4be45-146">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4be45-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4be45-147">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4be45-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4be45-148">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4be45-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4be45-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4be45-149">Requirements</span></span>



| <span data-ttu-id="4be45-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be45-150">Requirement</span></span> | <span data-ttu-id="4be45-151">Valore</span><span class="sxs-lookup"><span data-stu-id="4be45-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4be45-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4be45-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4be45-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4be45-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4be45-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4be45-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4be45-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4be45-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4be45-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4be45-156">Namespace</span></span><br/>                | <span data-ttu-id="4be45-157">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="4be45-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="4be45-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4be45-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4be45-159"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4be45-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="4be45-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4be45-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4be45-161"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="4be45-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be45-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4be45-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be45-163">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="4be45-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="4be45-164">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="4be45-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="4be45-165">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="4be45-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 
