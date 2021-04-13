---
title: Metodo AddComputerGroupNames della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Aggiunge i nomi dei gruppi di computer specificati alla proprietà ComputerGroupNames.
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddComputerGroupNames
- Metodo AddComputerGroupNames Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo AddComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120211"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a7df2-106">Metodo AddComputerGroupNames della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="a7df2-106">AddComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a7df2-107">Aggiunge i nomi dei gruppi di computer specificati alla proprietà **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a7df2-107">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7df2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7df2-108">Syntax</span></span>


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="a7df2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7df2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7df2-110">*ComputerGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7df2-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7df2-111">Elenco delimitato da punti e virgola di nomi di gruppi di computer da aggiungere alla proprietà **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="a7df2-111">Semicolon-separated list of computer group names to add to the **ComputerGroupNames** property.</span></span> <span data-ttu-id="a7df2-112">I nomi dei gruppi di computer devono essere nel formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="a7df2-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7df2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7df2-113">Return value</span></span>

<span data-ttu-id="a7df2-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a7df2-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a7df2-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a7df2-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a7df2-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a7df2-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7df2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7df2-117">Remarks</span></span>

<span data-ttu-id="a7df2-118">Se nel parametro *ComputerGroupNames* sono presenti più nomi di gruppi di computer e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="a7df2-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="a7df2-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="a7df2-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a7df2-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a7df2-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a7df2-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a7df2-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a7df2-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a7df2-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a7df2-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a7df2-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7df2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7df2-124">Requirements</span></span>



| <span data-ttu-id="a7df2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7df2-125">Requirement</span></span> | <span data-ttu-id="a7df2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a7df2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7df2-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7df2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a7df2-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7df2-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a7df2-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7df2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a7df2-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7df2-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a7df2-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7df2-131">Namespace</span></span><br/>                | <span data-ttu-id="a7df2-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a7df2-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a7df2-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a7df2-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7df2-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7df2-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7df2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a7df2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7df2-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7df2-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a7df2-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7df2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7df2-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="a7df2-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

