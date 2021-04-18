---
description: Ottiene il modulo della parte pubblica della chiave radice di archiviazione TPM.
ms.assetid: 266AE378-8BF2-4F6E-A055-E15D95E218DC
title: 'Metodo Win32_Tpm:: GetSrkPublicKeyModulus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkPublicKeyModulus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6d78abb695f2a9bc9de3887c8128395c2403b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314668"
---
# <a name="win32_tpmgetsrkpublickeymodulus-method"></a><span data-ttu-id="40fb2-103">\_Metodo Win32 TPM:: GetSrkPublicKeyModulus</span><span class="sxs-lookup"><span data-stu-id="40fb2-103">Win32\_Tpm::GetSrkPublicKeyModulus method</span></span>

<span data-ttu-id="40fb2-104">Ottiene il modulo della parte pubblica della chiave radice di archiviazione TPM.</span><span class="sxs-lookup"><span data-stu-id="40fb2-104">Gets the modulus of the public portion of the TPM Storage Root Key.</span></span>

<span data-ttu-id="40fb2-105">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="40fb2-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="40fb2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40fb2-106">Syntax</span></span>


```C++
uint32 GetSrkPublicKeyModulus(
  [out] uint8 SrkPublicKeyModulus
);
```



## <a name="parameters"></a><span data-ttu-id="40fb2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="40fb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40fb2-108">*SrkPublicKeyModulus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-108">*SrkPublicKeyModulus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40fb2-109">Restituisce una matrice di 256 byte contenente il modulo della parte pubblica della chiave radice di archiviazione TPM</span><span class="sxs-lookup"><span data-stu-id="40fb2-109">Returns a 256-byte array containing the modulus of the public portion of the TPM Storage Root Key</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40fb2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40fb2-110">Return value</span></span>

<span data-ttu-id="40fb2-111">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="40fb2-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="40fb2-112">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="40fb2-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="40fb2-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="40fb2-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="40fb2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40fb2-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="40fb2-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="40fb2-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="40fb2-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="40fb2-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40fb2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="40fb2-117">Remarks</span></span>

<span data-ttu-id="40fb2-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="40fb2-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40fb2-119">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="40fb2-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="40fb2-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="40fb2-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40fb2-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="40fb2-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40fb2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40fb2-122">Requirements</span></span>



| <span data-ttu-id="40fb2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="40fb2-123">Requirement</span></span> | <span data-ttu-id="40fb2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="40fb2-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="40fb2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40fb2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="40fb2-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="40fb2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40fb2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="40fb2-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="40fb2-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="40fb2-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40fb2-129">Namespace</span></span><br/>                | <span data-ttu-id="40fb2-130">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="40fb2-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="40fb2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="40fb2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40fb2-132"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40fb2-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="40fb2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="40fb2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40fb2-134"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="40fb2-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40fb2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40fb2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40fb2-136">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="40fb2-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
