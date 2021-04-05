---
title: Metodo SetResourceGroup della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta il tipo e il nome del gruppo di risorse.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetResourceGroup
- Metodo SetResourceGroup Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo SetResourceGroup
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874137"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="25cb9-106">Metodo SetResourceGroup della \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="25cb9-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="25cb9-107">Imposta il tipo e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25cb9-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="25cb9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25cb9-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="25cb9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="25cb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25cb9-110">*ResourceGroupName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25cb9-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25cb9-111">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25cb9-111">Resource group name.</span></span> <span data-ttu-id="25cb9-112">Questo valore sostituisce la proprietà **ResourceGroupName** esistente.</span><span class="sxs-lookup"><span data-stu-id="25cb9-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="25cb9-113">*ResourceGroupType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25cb9-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25cb9-114">Identifica il tipo del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25cb9-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="25cb9-115">Questo valore sostituisce la proprietà **ResourceGroupType** esistente.</span><span class="sxs-lookup"><span data-stu-id="25cb9-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="25cb9-116">RG</span><span class="sxs-lookup"><span data-stu-id="25cb9-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="25cb9-117">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25cb9-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="25cb9-118">CG</span><span class="sxs-lookup"><span data-stu-id="25cb9-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="25cb9-119">Gruppo di computer, come Archiviato in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="25cb9-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="25cb9-120">TUTTI</span><span class="sxs-lookup"><span data-stu-id="25cb9-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="25cb9-121">Tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="25cb9-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25cb9-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25cb9-122">Return value</span></span>

<span data-ttu-id="25cb9-123">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="25cb9-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="25cb9-124">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="25cb9-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="25cb9-125">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="25cb9-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="25cb9-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="25cb9-126">Remarks</span></span>

<span data-ttu-id="25cb9-127">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="25cb9-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="25cb9-128">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="25cb9-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="25cb9-129">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="25cb9-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="25cb9-130">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="25cb9-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="25cb9-131">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="25cb9-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="25cb9-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25cb9-132">Requirements</span></span>



| <span data-ttu-id="25cb9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="25cb9-133">Requirement</span></span> | <span data-ttu-id="25cb9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="25cb9-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25cb9-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25cb9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="25cb9-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="25cb9-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="25cb9-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25cb9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="25cb9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25cb9-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="25cb9-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="25cb9-139">Namespace</span></span><br/>                | <span data-ttu-id="25cb9-140">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="25cb9-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="25cb9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="25cb9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25cb9-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25cb9-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="25cb9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="25cb9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25cb9-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25cb9-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="25cb9-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25cb9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25cb9-146">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="25cb9-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

