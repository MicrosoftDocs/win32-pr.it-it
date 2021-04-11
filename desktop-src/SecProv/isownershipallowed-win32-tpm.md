---
description: Il metodo IsOwnershipAllowed della \_ classe TPM Win32 indica se è consentita la possibilità di installare un proprietario per il dispositivo.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Metodo IsOwnershipAllowed della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226005"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="dde5b-103">Metodo IsOwnershipAllowed della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="dde5b-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="dde5b-104">Il metodo **IsOwnershipAllowed** della classe [**\_ TPM Win32**](win32-tpm.md) indica se è consentita la possibilità di installare un proprietario per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dde5b-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde5b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dde5b-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="dde5b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dde5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde5b-107">*IsOwnershipAllowed* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dde5b-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dde5b-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dde5b-108">Type: **boolean**</span></span>

<span data-ttu-id="dde5b-109">Se **true**, è consentita la possibilità di installare un proprietario per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dde5b-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="dde5b-110">Se **false**, il metodo [**TakeOwnership**](takeownership-win32-tpm.md) non riuscirà a installare un proprietario per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dde5b-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="dde5b-111">Questo valore può essere modificato con il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="dde5b-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="dde5b-112">Il valore viene reimpostato su **true** dopo l'esecuzione del metodo [**Clear**](clear-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="dde5b-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde5b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dde5b-113">Return value</span></span>

<span data-ttu-id="dde5b-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dde5b-114">Type: **uint32**</span></span>

<span data-ttu-id="dde5b-115">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="dde5b-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="dde5b-116">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="dde5b-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="dde5b-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="dde5b-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="dde5b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dde5b-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dde5b-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dde5b-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="dde5b-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="dde5b-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dde5b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="dde5b-121">Remarks</span></span>

<span data-ttu-id="dde5b-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dde5b-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dde5b-123">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="dde5b-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dde5b-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="dde5b-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dde5b-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dde5b-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dde5b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dde5b-126">Requirements</span></span>



| <span data-ttu-id="dde5b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde5b-127">Requirement</span></span> | <span data-ttu-id="dde5b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="dde5b-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde5b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dde5b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dde5b-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dde5b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dde5b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dde5b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dde5b-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dde5b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dde5b-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dde5b-133">Namespace</span></span><br/>                | <span data-ttu-id="dde5b-134">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="dde5b-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="dde5b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dde5b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dde5b-136"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dde5b-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="dde5b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dde5b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dde5b-138"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="dde5b-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde5b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dde5b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde5b-140">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="dde5b-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
