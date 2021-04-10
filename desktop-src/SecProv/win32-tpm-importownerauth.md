---
description: Importa le informazioni di autorizzazione del proprietario per un TPM già di proprietà nel registro di sistema del sistema operativo.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Metodo Win32_Tpm:: ImportOwnerAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966580"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="5698b-103">\_Metodo Win32 TPM:: ImportOwnerAuth</span><span class="sxs-lookup"><span data-stu-id="5698b-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="5698b-104">Importa le informazioni di autorizzazione del proprietario per un TPM già di proprietà nel registro di sistema del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5698b-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="5698b-105">Questa operazione convaliderà prima di tutto se le informazioni di autorizzazione del proprietario fornite sono corrette.</span><span class="sxs-lookup"><span data-stu-id="5698b-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="5698b-106">Se è corretto, il metodo importa queste informazioni nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5698b-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="5698b-107">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="5698b-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="5698b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5698b-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="5698b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5698b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5698b-110">*OwnerAuth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5698b-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5698b-111">Informazioni di autorizzazione del proprietario valide per il TPM.</span><span class="sxs-lookup"><span data-stu-id="5698b-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5698b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5698b-112">Return value</span></span>

<span data-ttu-id="5698b-113">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5698b-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="5698b-114">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="5698b-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="5698b-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5698b-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5698b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5698b-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5698b-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5698b-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5698b-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5698b-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5698b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5698b-119">Remarks</span></span>

<span data-ttu-id="5698b-120">Questo metodo è particolarmente utile negli scenari in cui il TPM è in uno stato "pronto con funzionalità ridotte" e richiede l'importazione dell'autorizzazione del proprietario in modo che sia completamente pronto o in scenari a doppio avvio in cui uno dei sistemi operativi è proprietario del TPM e le informazioni di autorizzazione del proprietario per TPM non sono disponibili nell'altro sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5698b-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="5698b-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5698b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5698b-122">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5698b-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5698b-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5698b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5698b-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5698b-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5698b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5698b-125">Requirements</span></span>



| <span data-ttu-id="5698b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5698b-126">Requirement</span></span> | <span data-ttu-id="5698b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5698b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5698b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5698b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5698b-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5698b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5698b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5698b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5698b-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5698b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5698b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5698b-132">Namespace</span></span><br/>                | <span data-ttu-id="5698b-133">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="5698b-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="5698b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5698b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5698b-135"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5698b-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5698b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5698b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5698b-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5698b-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5698b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5698b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5698b-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="5698b-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
