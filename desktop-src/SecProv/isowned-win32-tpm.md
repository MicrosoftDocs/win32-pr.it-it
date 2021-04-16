---
description: Il metodo di proprietà della \_ classe TPM Win32 indica se il dispositivo dispone di un proprietario. Questo valore viene modificato dal metodo TakeOwnership.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Metodo di proprietà della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525675"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="74f93-104">Metodo di proprietà della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="74f93-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="74f93-105">Il metodo di **Proprietà** della classe [**\_ TPM Win32**](win32-tpm.md) indica se il dispositivo dispone di un proprietario.</span><span class="sxs-lookup"><span data-stu-id="74f93-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="74f93-106">Questo valore viene modificato dal metodo [**TakeOwnership**](takeownership-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="74f93-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f93-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74f93-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="74f93-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="74f93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f93-109">*Proprietario* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74f93-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74f93-110">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74f93-110">Type: **boolean**</span></span>

<span data-ttu-id="74f93-111">Se **true**, il dispositivo ha un proprietario.</span><span class="sxs-lookup"><span data-stu-id="74f93-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f93-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74f93-112">Return value</span></span>

<span data-ttu-id="74f93-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74f93-113">Type: **uint32**</span></span>

<span data-ttu-id="74f93-114">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="74f93-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="74f93-115">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="74f93-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="74f93-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="74f93-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="74f93-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74f93-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="74f93-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="74f93-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="74f93-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="74f93-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74f93-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="74f93-120">Remarks</span></span>

<span data-ttu-id="74f93-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="74f93-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="74f93-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="74f93-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="74f93-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="74f93-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="74f93-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="74f93-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74f93-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74f93-125">Requirements</span></span>



| <span data-ttu-id="74f93-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="74f93-126">Requirement</span></span> | <span data-ttu-id="74f93-127">Valore</span><span class="sxs-lookup"><span data-stu-id="74f93-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f93-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74f93-128">Minimum supported client</span></span><br/> | <span data-ttu-id="74f93-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74f93-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="74f93-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74f93-130">Minimum supported server</span></span><br/> | <span data-ttu-id="74f93-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74f93-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="74f93-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="74f93-132">Namespace</span></span><br/>                | <span data-ttu-id="74f93-133">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="74f93-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="74f93-134">MOF</span><span class="sxs-lookup"><span data-stu-id="74f93-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74f93-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74f93-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="74f93-136">DLL</span><span class="sxs-lookup"><span data-stu-id="74f93-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74f93-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="74f93-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f93-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74f93-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f93-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="74f93-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
