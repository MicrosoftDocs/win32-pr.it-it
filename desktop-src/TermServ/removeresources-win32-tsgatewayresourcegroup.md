---
title: Metodo RemoveResources della classe Win32_TSGatewayResourceGroup
description: Rimuove le risorse dal gruppo di risorse.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveResources
- Metodo RemoveResources Servizi Desktop remoto, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, metodo RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400924"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="0b569-106">Metodo RemoveResources della \_ classe TSGatewayResourceGroup Win32</span><span class="sxs-lookup"><span data-stu-id="0b569-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="0b569-107">Rimuove le risorse dal gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b569-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b569-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b569-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="0b569-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b569-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b569-110">*Risorse* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0b569-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b569-111">Elenco di risorse separate da punto e virgola da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0b569-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b569-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b569-112">Return value</span></span>

<span data-ttu-id="0b569-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0b569-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0b569-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0b569-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0b569-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0b569-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b569-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b569-116">Remarks</span></span>

<span data-ttu-id="0b569-117">Se più risorse si trovano nel parametro *Resources* e una delle risorse non può essere elaborata, nessuna delle risorse verrà elaborata.</span><span class="sxs-lookup"><span data-stu-id="0b569-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="0b569-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="0b569-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0b569-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0b569-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0b569-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0b569-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0b569-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0b569-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0b569-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0b569-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b569-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b569-123">Requirements</span></span>



| <span data-ttu-id="0b569-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b569-124">Requirement</span></span> | <span data-ttu-id="0b569-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0b569-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b569-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b569-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b569-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0b569-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0b569-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b569-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b569-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b569-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b569-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b569-130">Namespace</span></span><br/>                | <span data-ttu-id="0b569-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0b569-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0b569-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0b569-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b569-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b569-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b569-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0b569-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b569-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b569-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0b569-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b569-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b569-137">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="0b569-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

