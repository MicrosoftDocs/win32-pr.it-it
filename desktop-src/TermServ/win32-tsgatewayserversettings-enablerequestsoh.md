---
title: Metodo EnableRequestSOH della classe Win32_TSGatewayServerSettings
description: EnableRequestSOH non è più disponibile.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableRequestSOH
- Metodo EnableRequestSOH Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnableRequestSOH
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302425"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="46127-106">Metodo EnableRequestSOH della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="46127-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="46127-107">\[Il metodo **EnableRequestSOH** non è più disponibile a partire da Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="46127-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="46127-108">Abilita o Disabilita le richieste per un rapporto di integrità (SoH).</span><span class="sxs-lookup"><span data-stu-id="46127-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="46127-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46127-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="46127-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="46127-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46127-111">*RequestSOH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46127-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46127-112">Specificare **true** per abilitare la funzionalità o **false** per disabilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="46127-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46127-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46127-113">Return value</span></span>

<span data-ttu-id="46127-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="46127-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="46127-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="46127-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="46127-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="46127-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46127-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="46127-117">Remarks</span></span>

<span data-ttu-id="46127-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="46127-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="46127-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="46127-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="46127-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="46127-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="46127-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="46127-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="46127-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="46127-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="46127-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46127-123">Requirements</span></span>



| <span data-ttu-id="46127-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="46127-124">Requirement</span></span> | <span data-ttu-id="46127-125">Valore</span><span class="sxs-lookup"><span data-stu-id="46127-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46127-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46127-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46127-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46127-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="46127-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46127-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46127-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46127-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="46127-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="46127-130">End of server support</span></span><br/>    | <span data-ttu-id="46127-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="46127-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="46127-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46127-132">Namespace</span></span><br/>                | <span data-ttu-id="46127-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46127-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="46127-134">MOF</span><span class="sxs-lookup"><span data-stu-id="46127-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46127-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46127-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="46127-136">DLL</span><span class="sxs-lookup"><span data-stu-id="46127-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46127-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46127-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="46127-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46127-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46127-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="46127-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

