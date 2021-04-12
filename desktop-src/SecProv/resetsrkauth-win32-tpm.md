---
description: Reimposta il valore di autorizzazione della chiave radice di archiviazione (SRK) in modo che sia compatibile con il sistema operativo.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Metodo ResetSrkAuth della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348911"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="35f9f-103">Metodo ResetSrkAuth della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="35f9f-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="35f9f-104">Il metodo **ResetSrkAuth** della classe [**\_ TPM Win32**](win32-tpm.md) Reimposta il valore di autorizzazione della chiave radice di archiviazione (SRK) in modo che sia compatibile con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="35f9f-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f9f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35f9f-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="35f9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35f9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f9f-107">*OwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="35f9f-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35f9f-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="35f9f-108">Type: **string**</span></span>

<span data-ttu-id="35f9f-109">Stringa che identifica il proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="35f9f-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="35f9f-110">Questa stringa deve essere una stringa con codifica Base64 con terminazione null che contiene esattamente 20 byte di dati binari.</span><span class="sxs-lookup"><span data-stu-id="35f9f-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="35f9f-111">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="35f9f-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="35f9f-112">Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="35f9f-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f9f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35f9f-113">Return value</span></span>

<span data-ttu-id="35f9f-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35f9f-114">Type: **uint32**</span></span>

<span data-ttu-id="35f9f-115">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="35f9f-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="35f9f-116">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="35f9f-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="35f9f-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="35f9f-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="35f9f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35f9f-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35f9f-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="35f9f-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="35f9f-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="35f9f-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="35f9f-121"><dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="35f9f-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="35f9f-122">Il valore di autorizzazione del proprietario specificato non è in grado di soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="35f9f-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="35f9f-123"><dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="35f9f-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="35f9f-124">Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="35f9f-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="35f9f-125">Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="35f9f-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35f9f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="35f9f-126">Remarks</span></span>

<span data-ttu-id="35f9f-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="35f9f-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35f9f-128">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="35f9f-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="35f9f-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="35f9f-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35f9f-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="35f9f-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35f9f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35f9f-131">Requirements</span></span>



| <span data-ttu-id="35f9f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="35f9f-132">Requirement</span></span> | <span data-ttu-id="35f9f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="35f9f-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="35f9f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35f9f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="35f9f-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35f9f-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="35f9f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35f9f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="35f9f-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35f9f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="35f9f-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35f9f-138">Namespace</span></span><br/>                | <span data-ttu-id="35f9f-139">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="35f9f-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="35f9f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="35f9f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35f9f-141"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35f9f-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="35f9f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="35f9f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f9f-143"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="35f9f-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f9f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35f9f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f9f-145">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="35f9f-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
