---
title: Metodo RemoveTSCGroup della classe Win32_TSLicenseServer
description: RemoveTSCGroup non è più disponibile per l'uso a partire da Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveTSCGroup
- Metodo RemoveTSCGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518994"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="03632-106">Metodo RemoveTSCGroup della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="03632-106">RemoveTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="03632-107">\[**RemoveTSCGroup** non è più disponibile per l'uso a partire da Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="03632-107">\[**RemoveTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="03632-108">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="03632-108">This method is not supported.</span></span>

<span data-ttu-id="03632-109">**Windows server 2008 R2 e Windows server 2008:** Rimuove il gruppo locale computer Terminal Server dal server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="03632-109">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="03632-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03632-110">Syntax</span></span>


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="03632-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="03632-111">Parameters</span></span>

<span data-ttu-id="03632-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="03632-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03632-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03632-113">Return value</span></span>

<span data-ttu-id="03632-114">Restituisce **WBEM \_ E \_ non \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="03632-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="03632-115">**Windows server 2008 R2 e Windows server 2008:** Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="03632-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="03632-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="03632-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="03632-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="03632-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03632-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="03632-118">Remarks</span></span>

<span data-ttu-id="03632-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="03632-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="03632-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="03632-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="03632-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="03632-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="03632-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="03632-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="03632-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="03632-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="03632-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03632-124">Requirements</span></span>



| <span data-ttu-id="03632-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="03632-125">Requirement</span></span> | <span data-ttu-id="03632-126">Valore</span><span class="sxs-lookup"><span data-stu-id="03632-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="03632-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03632-127">Minimum supported client</span></span><br/> | <span data-ttu-id="03632-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="03632-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="03632-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03632-129">Minimum supported server</span></span><br/> | <span data-ttu-id="03632-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03632-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="03632-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="03632-131">End of client support</span></span><br/>    | <span data-ttu-id="03632-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="03632-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="03632-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="03632-133">End of server support</span></span><br/>    | <span data-ttu-id="03632-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03632-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="03632-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03632-135">Namespace</span></span><br/>                | <span data-ttu-id="03632-136">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="03632-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="03632-137">MOF</span><span class="sxs-lookup"><span data-stu-id="03632-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03632-138"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03632-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="03632-139">DLL</span><span class="sxs-lookup"><span data-stu-id="03632-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03632-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03632-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03632-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03632-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03632-142">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="03632-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="03632-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="03632-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

