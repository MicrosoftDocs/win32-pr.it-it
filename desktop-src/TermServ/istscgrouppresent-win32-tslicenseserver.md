---
title: Metodo IsTSCGroupPresent della classe Win32_TSLicenseServer
description: IsTSCGroupPresent non è più disponibile per l'uso a partire da Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsTSCGroupPresent
- Metodo IsTSCGroupPresent Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048141"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="df6cf-106">Metodo IsTSCGroupPresent della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="df6cf-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="df6cf-107">\[**IsTSCGroupPresent** non è più disponibile per l'uso a partire da Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="df6cf-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="df6cf-108">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df6cf-108">This method is not supported.</span></span>

<span data-ttu-id="df6cf-109">**Windows server 2008 R2 e Windows server 2008:** Recupera un valore che indica se il gruppo locale computer Terminal Server esiste nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="df6cf-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6cf-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df6cf-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="df6cf-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="df6cf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6cf-112">*Presente* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df6cf-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6cf-113">Valore booleano che indica se il gruppo locale Terminal Server computer esiste.</span><span class="sxs-lookup"><span data-stu-id="df6cf-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6cf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df6cf-114">Return value</span></span>

<span data-ttu-id="df6cf-115">Restituisce **WBEM \_ E \_ non \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="df6cf-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="df6cf-116">**Windows server 2008 R2 e Windows server 2008:** Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="df6cf-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="df6cf-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="df6cf-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="df6cf-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="df6cf-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df6cf-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="df6cf-119">Remarks</span></span>

<span data-ttu-id="df6cf-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="df6cf-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="df6cf-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="df6cf-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="df6cf-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="df6cf-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="df6cf-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="df6cf-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="df6cf-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="df6cf-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="df6cf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df6cf-125">Requirements</span></span>



| <span data-ttu-id="df6cf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6cf-126">Requirement</span></span> | <span data-ttu-id="df6cf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="df6cf-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="df6cf-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df6cf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df6cf-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df6cf-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="df6cf-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df6cf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df6cf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df6cf-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="df6cf-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="df6cf-132">End of client support</span></span><br/>    | <span data-ttu-id="df6cf-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df6cf-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="df6cf-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="df6cf-134">End of server support</span></span><br/>    | <span data-ttu-id="df6cf-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="df6cf-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="df6cf-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df6cf-136">Namespace</span></span><br/>                | <span data-ttu-id="df6cf-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="df6cf-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="df6cf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="df6cf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df6cf-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df6cf-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="df6cf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="df6cf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df6cf-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df6cf-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6cf-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df6cf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6cf-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="df6cf-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

