---
description: Indica se il provisioning automatico del TPM è abilitato.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Metodo Win32_Tpm:: IsAutoProvisioningEnabled'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883590"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="df7eb-103">\_Metodo Win32 TPM:: IsAutoProvisioningEnabled</span><span class="sxs-lookup"><span data-stu-id="df7eb-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="df7eb-104">Indica se il provisioning automatico del TPM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="df7eb-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="df7eb-105">Per impostazione predefinita, il provisioning automatico è abilitato per Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="df7eb-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="df7eb-106">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="df7eb-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="df7eb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df7eb-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="df7eb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df7eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df7eb-109">*IsAutoProvisioningEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df7eb-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df7eb-110">Impostare su **true** se il provisioning automatico del TPM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="df7eb-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df7eb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df7eb-111">Return value</span></span>

<span data-ttu-id="df7eb-112">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="df7eb-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="df7eb-113">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="df7eb-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="df7eb-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="df7eb-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="df7eb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df7eb-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="df7eb-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="df7eb-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="df7eb-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="df7eb-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df7eb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="df7eb-118">Remarks</span></span>

<span data-ttu-id="df7eb-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="df7eb-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="df7eb-120">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="df7eb-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="df7eb-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="df7eb-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="df7eb-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="df7eb-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df7eb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df7eb-123">Requirements</span></span>



| <span data-ttu-id="df7eb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="df7eb-124">Requirement</span></span> | <span data-ttu-id="df7eb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="df7eb-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7eb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df7eb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="df7eb-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="df7eb-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df7eb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df7eb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="df7eb-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="df7eb-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="df7eb-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df7eb-130">Namespace</span></span><br/>                | <span data-ttu-id="df7eb-131">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="df7eb-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="df7eb-132">MOF</span><span class="sxs-lookup"><span data-stu-id="df7eb-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df7eb-133"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df7eb-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="df7eb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="df7eb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df7eb-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="df7eb-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df7eb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df7eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df7eb-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="df7eb-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
