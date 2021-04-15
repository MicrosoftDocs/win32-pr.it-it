---
title: Metodo seresources della classe Win32_TSGatewayResourceGroup
description: Imposta la proprietà Resources per questo gruppo di risorse.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo seresources
- Servizi Desktop remoto del metodo seresources, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo seresources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400432"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="2fb20-106">Metodo seresources della \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fb20-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="2fb20-107">Imposta la proprietà **Resources** per questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fb20-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb20-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fb20-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="2fb20-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fb20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb20-110">*Risorse* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2fb20-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb20-111">Elenco di risorse separate da punto e virgola in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2fb20-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="2fb20-112">" \* " Indica tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="2fb20-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb20-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fb20-113">Return value</span></span>

<span data-ttu-id="2fb20-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="2fb20-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2fb20-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="2fb20-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2fb20-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2fb20-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fb20-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fb20-117">Remarks</span></span>

<span data-ttu-id="2fb20-118">Se più risorse si trovano nel parametro *Resources* e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.</span><span class="sxs-lookup"><span data-stu-id="2fb20-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="2fb20-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="2fb20-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2fb20-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2fb20-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2fb20-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2fb20-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2fb20-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2fb20-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2fb20-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2fb20-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb20-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fb20-124">Requirements</span></span>



| <span data-ttu-id="2fb20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb20-125">Requirement</span></span> | <span data-ttu-id="2fb20-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2fb20-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb20-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb20-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2fb20-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2fb20-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb20-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fb20-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2fb20-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fb20-131">Namespace</span></span><br/>                | <span data-ttu-id="2fb20-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2fb20-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2fb20-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2fb20-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fb20-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fb20-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fb20-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2fb20-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb20-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fb20-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2fb20-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fb20-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb20-138">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="2fb20-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

