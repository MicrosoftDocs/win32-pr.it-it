---
description: Il metodo IsSrkAuthCompatible della \_ classe TPM Win32 indica se l'autorizzazione della chiave radice di archiviazione (SRK) è compatibile con il valore previsto da Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Metodo IsSrkAuthCompatible della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883601"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="c298f-103">Metodo IsSrkAuthCompatible della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="c298f-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="c298f-104">Il metodo **IsSrkAuthCompatible** della classe [**\_ TPM Win32**](win32-tpm.md) indica se l'autorizzazione della chiave radice di archiviazione (SRK) è compatibile con il valore previsto da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c298f-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="c298f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c298f-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="c298f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c298f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c298f-107">*IsSrkAuthCompatible* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c298f-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c298f-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c298f-108">Type: **boolean**</span></span>

<span data-ttu-id="c298f-109">Se **true**, il valore di autorizzazione SRK ha un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="c298f-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c298f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c298f-110">Return value</span></span>

<span data-ttu-id="c298f-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c298f-111">Type: **uint32**</span></span>

<span data-ttu-id="c298f-112">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="c298f-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="c298f-113">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="c298f-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="c298f-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c298f-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c298f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c298f-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c298f-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c298f-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c298f-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c298f-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c298f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c298f-118">Remarks</span></span>

<span data-ttu-id="c298f-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c298f-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c298f-120">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c298f-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c298f-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c298f-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c298f-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c298f-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c298f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c298f-123">Requirements</span></span>



| <span data-ttu-id="c298f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c298f-124">Requirement</span></span> | <span data-ttu-id="c298f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c298f-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c298f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c298f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c298f-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c298f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c298f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c298f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c298f-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c298f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c298f-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c298f-130">Namespace</span></span><br/>                | <span data-ttu-id="c298f-131">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="c298f-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="c298f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c298f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c298f-133"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c298f-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="c298f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c298f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c298f-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="c298f-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c298f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c298f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c298f-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="c298f-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
