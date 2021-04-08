---
title: Metodo Create della classe Win32_TSGatewayResourceGroup
description: Crea un gruppo di risorse.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048028"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="989ba-106">Metodo Create della classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="989ba-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="989ba-107">Crea un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="989ba-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="989ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="989ba-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="989ba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="989ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="989ba-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="989ba-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="989ba-111">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="989ba-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="989ba-112">*Descrizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="989ba-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="989ba-113">Descrizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="989ba-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="989ba-114">*Risorse* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="989ba-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="989ba-115">Elenco di risorse separate da punto e virgola in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="989ba-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="989ba-116">" \* " Indica tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="989ba-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="989ba-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="989ba-117">Return value</span></span>

<span data-ttu-id="989ba-118">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="989ba-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="989ba-119">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="989ba-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="989ba-120">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="989ba-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="989ba-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="989ba-121">Remarks</span></span>

<span data-ttu-id="989ba-122">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="989ba-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="989ba-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="989ba-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="989ba-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="989ba-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="989ba-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="989ba-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="989ba-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="989ba-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="989ba-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="989ba-127">Requirements</span></span>



| <span data-ttu-id="989ba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="989ba-128">Requirement</span></span> | <span data-ttu-id="989ba-129">Valore</span><span class="sxs-lookup"><span data-stu-id="989ba-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="989ba-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="989ba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="989ba-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="989ba-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="989ba-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="989ba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="989ba-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="989ba-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="989ba-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="989ba-134">Namespace</span></span><br/>                | <span data-ttu-id="989ba-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="989ba-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="989ba-136">MOF</span><span class="sxs-lookup"><span data-stu-id="989ba-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="989ba-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="989ba-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="989ba-138">DLL</span><span class="sxs-lookup"><span data-stu-id="989ba-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="989ba-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="989ba-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="989ba-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="989ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="989ba-141">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="989ba-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

