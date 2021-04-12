---
title: Metodo Update della classe Win32_TSGatewayResourceGroup
description: Aggiorna il gruppo di risorse.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Metodo di aggiornamento Servizi Desktop remoto
- Metodo Update Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a7b1610fc14aa522fa4d8b7caf03fccd7b37375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400674"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="33837-106">Metodo Update della classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33837-106">Update method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="33837-107">Aggiorna il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33837-107">Updates the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="33837-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33837-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="33837-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="33837-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33837-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33837-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33837-111">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33837-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="33837-112">*Descrizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="33837-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33837-113">Descrizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33837-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="33837-114">*Risorse* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="33837-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33837-115">Elenco di risorse separate da punto e virgola in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33837-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="33837-116">" \* " Indica tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="33837-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33837-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33837-117">Return value</span></span>

<span data-ttu-id="33837-118">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="33837-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="33837-119">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="33837-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="33837-120">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="33837-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33837-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="33837-121">Remarks</span></span>

<span data-ttu-id="33837-122">Se più risorse si trovano nel parametro *Resources* e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.</span><span class="sxs-lookup"><span data-stu-id="33837-122">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="33837-123">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="33837-123">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="33837-124">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="33837-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="33837-125">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="33837-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="33837-126">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="33837-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="33837-127">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="33837-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="33837-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33837-128">Requirements</span></span>



| <span data-ttu-id="33837-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="33837-129">Requirement</span></span> | <span data-ttu-id="33837-130">Valore</span><span class="sxs-lookup"><span data-stu-id="33837-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33837-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33837-131">Minimum supported client</span></span><br/> | <span data-ttu-id="33837-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="33837-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="33837-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33837-133">Minimum supported server</span></span><br/> | <span data-ttu-id="33837-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33837-134">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="33837-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33837-135">Namespace</span></span><br/>                | <span data-ttu-id="33837-136">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="33837-136">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="33837-137">MOF</span><span class="sxs-lookup"><span data-stu-id="33837-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33837-138"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33837-138"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="33837-139">DLL</span><span class="sxs-lookup"><span data-stu-id="33837-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33837-140"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33837-140"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="33837-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33837-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33837-142">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="33837-142">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

