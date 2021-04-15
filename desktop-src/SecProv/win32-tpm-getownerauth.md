---
description: Ottiene le informazioni di autorizzazione del proprietario per un TPM se ne è disponibile uno nel registro di sistema.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Metodo Win32_Tpm:: GetOwnerAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525668"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="da726-103">\_Metodo Win32 TPM:: GetOwnerAuth</span><span class="sxs-lookup"><span data-stu-id="da726-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="da726-104">Ottiene le informazioni di autorizzazione del proprietario per un TPM se ne è disponibile uno nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="da726-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="da726-105">Se un TPM è di proprietà o ne è stato effettuato il provisioning in Windows 8 con le impostazioni predefinite, le informazioni di autorizzazione del proprietario del TPM vengono archiviate nel registro di sistema e sono disponibili per l'uso da parte di questo metodo</span><span class="sxs-lookup"><span data-stu-id="da726-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="da726-106">Questo metodo è accessibile solo agli amministratori locali.</span><span class="sxs-lookup"><span data-stu-id="da726-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="da726-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da726-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="da726-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="da726-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da726-109">*OwnerAuth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da726-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da726-110">Informazioni di autorizzazione del proprietario per un TPM, se disponibile nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="da726-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da726-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da726-111">Return value</span></span>

<span data-ttu-id="da726-112">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="da726-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="da726-113">I codici restituiti comuni sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="da726-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="da726-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="da726-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="da726-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da726-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="da726-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="da726-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="da726-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="da726-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="da726-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="da726-118">Remarks</span></span>

<span data-ttu-id="da726-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="da726-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da726-120">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="da726-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="da726-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="da726-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da726-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="da726-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da726-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da726-123">Requirements</span></span>



| <span data-ttu-id="da726-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="da726-124">Requirement</span></span> | <span data-ttu-id="da726-125">Valore</span><span class="sxs-lookup"><span data-stu-id="da726-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="da726-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da726-126">Minimum supported client</span></span><br/> | <span data-ttu-id="da726-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="da726-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da726-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da726-128">Minimum supported server</span></span><br/> | <span data-ttu-id="da726-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="da726-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="da726-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da726-130">Namespace</span></span><br/>                | <span data-ttu-id="da726-131">\\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="da726-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="da726-132">MOF</span><span class="sxs-lookup"><span data-stu-id="da726-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da726-133"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da726-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="da726-134">DLL</span><span class="sxs-lookup"><span data-stu-id="da726-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da726-135"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="da726-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da726-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da726-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da726-137">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="da726-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
