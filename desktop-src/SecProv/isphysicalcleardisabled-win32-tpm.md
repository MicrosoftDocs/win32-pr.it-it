---
description: Il metodo IsPhysicalClearDisabled della \_ classe TPM Win32 indica se solo il proprietario del dispositivo potrebbe essere in grado di cancellare il dispositivo.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Metodo IsPhysicalClearDisabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315341"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="8270b-103">Metodo IsPhysicalClearDisabled della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="8270b-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="8270b-104">Il metodo **IsPhysicalClearDisabled** della classe [**\_ TPM Win32**](win32-tpm.md) indica se solo il proprietario del dispositivo potrebbe essere in grado di cancellare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8270b-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8270b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8270b-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="8270b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8270b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8270b-107">*IsPhysicalClearDisabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8270b-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8270b-108">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8270b-108">Type: **boolean**</span></span>

<span data-ttu-id="8270b-109">Se **true**, solo il proprietario del dispositivo è in grado di cancellare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8270b-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8270b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8270b-110">Return value</span></span>

<span data-ttu-id="8270b-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8270b-111">Type: **uint32**</span></span>

<span data-ttu-id="8270b-112">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="8270b-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="8270b-113">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="8270b-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="8270b-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8270b-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="8270b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8270b-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8270b-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8270b-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8270b-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="8270b-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8270b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8270b-118">Remarks</span></span>

<span data-ttu-id="8270b-119">Questo valore viene reimpostato su **false** all'inizio di ogni ciclo di avvio.</span><span class="sxs-lookup"><span data-stu-id="8270b-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="8270b-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8270b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8270b-121">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8270b-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8270b-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8270b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8270b-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8270b-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8270b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8270b-124">Requirements</span></span>



| <span data-ttu-id="8270b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8270b-125">Requirement</span></span> | <span data-ttu-id="8270b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8270b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8270b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8270b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8270b-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8270b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8270b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8270b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8270b-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8270b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8270b-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8270b-131">Namespace</span></span><br/>                | <span data-ttu-id="8270b-132">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="8270b-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="8270b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8270b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8270b-134"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8270b-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="8270b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8270b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8270b-136"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="8270b-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8270b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8270b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8270b-138">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="8270b-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
