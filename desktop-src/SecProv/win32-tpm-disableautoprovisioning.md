---
description: Disabilita il provisioning automatico del TPM se è attualmente abilitato.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D Metodo isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314669"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="ad84f-103">\_TPM Win32::D Metodo isableautoprovisioning</span><span class="sxs-lookup"><span data-stu-id="ad84f-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="ad84f-104">Disabilita il provisioning automatico del TPM se è attualmente abilitato.</span><span class="sxs-lookup"><span data-stu-id="ad84f-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="ad84f-105">L'operazione non ha alcun effetto se il provisioning automatico è già disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ad84f-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="ad84f-106">Per impostazione predefinita, il provisioning automatico è abilitato per Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ad84f-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="ad84f-107">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="ad84f-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad84f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad84f-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="ad84f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad84f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad84f-110">*OnlyForNextBoot* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ad84f-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ad84f-111">Se impostato su **true**, il provisioning automatico è disabilitato solo per l'avvio successivo.</span><span class="sxs-lookup"><span data-stu-id="ad84f-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="ad84f-112">Se è impostato su **false** o non è specificato, il provisioning automatico è disabilitato in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="ad84f-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad84f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad84f-113">Return value</span></span>

<span data-ttu-id="ad84f-114">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ad84f-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="ad84f-115">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ad84f-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="ad84f-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad84f-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ad84f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad84f-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ad84f-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ad84f-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ad84f-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ad84f-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad84f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad84f-120">Remarks</span></span>

<span data-ttu-id="ad84f-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad84f-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad84f-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ad84f-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ad84f-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ad84f-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad84f-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ad84f-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad84f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad84f-125">Requirements</span></span>



| <span data-ttu-id="ad84f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad84f-126">Requirement</span></span> | <span data-ttu-id="ad84f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ad84f-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad84f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad84f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad84f-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ad84f-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ad84f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad84f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad84f-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ad84f-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ad84f-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad84f-132">Namespace</span></span><br/>                | <span data-ttu-id="ad84f-133">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="ad84f-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="ad84f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ad84f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad84f-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad84f-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad84f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ad84f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad84f-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ad84f-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad84f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad84f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad84f-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ad84f-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
