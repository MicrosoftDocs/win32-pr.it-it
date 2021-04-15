---
title: Metodo AddResources della classe Win32_TSGatewayResourceGroup
description: Aggiunge risorse al gruppo di risorse.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddResources
- Metodo AddResources Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo AddResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517463"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="10d4b-106">Metodo AddResources della \_ classe TSGatewayResourceGroup Win32</span><span class="sxs-lookup"><span data-stu-id="10d4b-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="10d4b-107">Aggiunge risorse al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10d4b-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d4b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10d4b-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="10d4b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="10d4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d4b-110">*Risorse* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="10d4b-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d4b-111">Elenco di risorse separate da punto e virgola da aggiungere al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10d4b-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="10d4b-112">" \* " Indica tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="10d4b-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d4b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10d4b-113">Return value</span></span>

<span data-ttu-id="10d4b-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="10d4b-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="10d4b-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="10d4b-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="10d4b-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10d4b-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10d4b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="10d4b-117">Remarks</span></span>

<span data-ttu-id="10d4b-118">Se più risorse si trovano nel parametro *Resources* e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.</span><span class="sxs-lookup"><span data-stu-id="10d4b-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="10d4b-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="10d4b-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="10d4b-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10d4b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10d4b-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="10d4b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10d4b-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="10d4b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10d4b-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10d4b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10d4b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10d4b-124">Requirements</span></span>



| <span data-ttu-id="10d4b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d4b-125">Requirement</span></span> | <span data-ttu-id="10d4b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="10d4b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d4b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10d4b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10d4b-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="10d4b-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="10d4b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10d4b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10d4b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10d4b-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="10d4b-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10d4b-131">Namespace</span></span><br/>                | <span data-ttu-id="10d4b-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="10d4b-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="10d4b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="10d4b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10d4b-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10d4b-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="10d4b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="10d4b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d4b-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d4b-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="10d4b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10d4b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d4b-138">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="10d4b-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

