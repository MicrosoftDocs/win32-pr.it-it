---
description: Esegue un test automatico del TPM e restituisce il risultato.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Metodo SelfTest della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306375"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="f32fa-103">Metodo SelfTest della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="f32fa-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="f32fa-104">Il metodo **SELFTEST** della classe [**\_ TPM Win32**](win32-tpm.md) esegue un test automatico del TPM e restituisce il risultato.</span><span class="sxs-lookup"><span data-stu-id="f32fa-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="f32fa-105">Un self-test TPM viene eseguito automaticamente all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="f32fa-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="f32fa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f32fa-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="f32fa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f32fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f32fa-108">*SelfTestResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f32fa-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f32fa-109">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f32fa-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="f32fa-110">Matrice di byte che contiene il risultato di test automatico.</span><span class="sxs-lookup"><span data-stu-id="f32fa-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="f32fa-111">Il formato di questo parametro è specifico del produttore.</span><span class="sxs-lookup"><span data-stu-id="f32fa-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f32fa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f32fa-112">Return value</span></span>

<span data-ttu-id="f32fa-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f32fa-113">Type: **uint32**</span></span>

<span data-ttu-id="f32fa-114">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="f32fa-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="f32fa-115">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="f32fa-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="f32fa-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f32fa-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f32fa-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f32fa-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="f32fa-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f32fa-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f32fa-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f32fa-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f32fa-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f32fa-120">Remarks</span></span>

<span data-ttu-id="f32fa-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f32fa-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f32fa-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f32fa-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f32fa-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f32fa-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f32fa-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f32fa-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f32fa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f32fa-125">Requirements</span></span>



| <span data-ttu-id="f32fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32fa-126">Requirement</span></span> | <span data-ttu-id="f32fa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f32fa-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32fa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f32fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f32fa-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f32fa-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f32fa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f32fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f32fa-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f32fa-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f32fa-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f32fa-132">Namespace</span></span><br/>                | <span data-ttu-id="f32fa-133">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="f32fa-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="f32fa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f32fa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f32fa-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f32fa-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f32fa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f32fa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f32fa-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f32fa-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32fa-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f32fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32fa-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="f32fa-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
