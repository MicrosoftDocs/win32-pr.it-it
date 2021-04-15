---
title: Metodo SetComputerGroupNames della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà ComputerGroupNames.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetComputerGroupNames
- Metodo SetComputerGroupNames Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400577"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="8873b-106">Metodo SetComputerGroupNames della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="8873b-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="8873b-107">Imposta la proprietà **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="8873b-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8873b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8873b-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="8873b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8873b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8873b-110">*ComputerGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8873b-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8873b-111">Elenco di nomi di gruppi di computer separati da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="8873b-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="8873b-112">Questo valore può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="8873b-112">This value can be empty.</span></span> <span data-ttu-id="8873b-113">I nomi sono nel formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="8873b-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="8873b-114">Se viene specificato un valore, il computer client deve appartenere a uno di questi gruppi di computer affinché l'utente acceda al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="8873b-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8873b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8873b-115">Return value</span></span>

<span data-ttu-id="8873b-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8873b-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8873b-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8873b-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8873b-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8873b-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8873b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8873b-119">Remarks</span></span>

<span data-ttu-id="8873b-120">Se nel parametro *ComputerGroupNames* sono presenti più nomi di gruppi di computer e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="8873b-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="8873b-121">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="8873b-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8873b-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8873b-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8873b-123">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8873b-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8873b-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8873b-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8873b-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8873b-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8873b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8873b-126">Requirements</span></span>



| <span data-ttu-id="8873b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8873b-127">Requirement</span></span> | <span data-ttu-id="8873b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8873b-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8873b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8873b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8873b-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8873b-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8873b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8873b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8873b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8873b-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8873b-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8873b-133">Namespace</span></span><br/>                | <span data-ttu-id="8873b-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8873b-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8873b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8873b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8873b-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8873b-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8873b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8873b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8873b-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8873b-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8873b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8873b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8873b-140">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="8873b-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

