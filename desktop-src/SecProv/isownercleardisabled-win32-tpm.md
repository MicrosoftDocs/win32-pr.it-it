---
description: Il metodo IsOwnerClearDisabled della \_ classe TPM Win32 indica se il proprietario del dispositivo è limitato dalla cancellazione del dispositivo.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Metodo IsOwnerClearDisabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315343"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="ceef3-103">Metodo IsOwnerClearDisabled della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="ceef3-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ceef3-104">Il metodo **IsOwnerClearDisabled** della classe [**\_ TPM Win32**](win32-tpm.md) indica se il proprietario del dispositivo è limitato dalla cancellazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ceef3-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceef3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ceef3-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="ceef3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ceef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceef3-107">*IsOwnerClearDisabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ceef3-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef3-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ceef3-108">Type: **boolean**</span></span>

<span data-ttu-id="ceef3-109">Se **true**, il proprietario del dispositivo non è in grado di cancellare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ceef3-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="ceef3-110">Solo un utente fisicamente presente potrebbe essere in grado di cancellare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ceef3-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="ceef3-111">Se **false**, il proprietario del dispositivo è in grado di cancellare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ceef3-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceef3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ceef3-112">Return value</span></span>

<span data-ttu-id="ceef3-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceef3-113">Type: **uint32**</span></span>

<span data-ttu-id="ceef3-114">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="ceef3-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ceef3-115">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ceef3-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="ceef3-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ceef3-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ceef3-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceef3-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ceef3-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ceef3-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ceef3-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ceef3-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ceef3-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceef3-120">Remarks</span></span>

<span data-ttu-id="ceef3-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ceef3-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ceef3-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ceef3-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ceef3-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ceef3-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ceef3-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ceef3-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ceef3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceef3-125">Requirements</span></span>



| <span data-ttu-id="ceef3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceef3-126">Requirement</span></span> | <span data-ttu-id="ceef3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ceef3-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceef3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceef3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ceef3-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ceef3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ceef3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceef3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ceef3-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ceef3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ceef3-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ceef3-132">Namespace</span></span><br/>                | <span data-ttu-id="ceef3-133">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="ceef3-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ceef3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ceef3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceef3-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceef3-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceef3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ceef3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceef3-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="ceef3-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceef3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceef3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceef3-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ceef3-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
