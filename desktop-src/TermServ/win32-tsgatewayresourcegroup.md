---
title: Classe Win32_TSGatewayResourceGroup
description: Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi computer) a una singola entità.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto
- Classe Win32_TSGatewayResourceGroup Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301503"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="c83b7-105">Win32 \_ TSGatewayResourceGroup (classe)</span><span class="sxs-lookup"><span data-stu-id="c83b7-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="c83b7-106">Descrive un gruppo di risorse, che esegue il mapping di un set di risorse (nomi computer) a una singola entità.</span><span class="sxs-lookup"><span data-stu-id="c83b7-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83b7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c83b7-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="c83b7-108">Members</span><span class="sxs-lookup"><span data-stu-id="c83b7-108">Members</span></span>

<span data-ttu-id="c83b7-109">La classe **Win32 \_ TSGatewayResourceGroup** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c83b7-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="c83b7-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c83b7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c83b7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c83b7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c83b7-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c83b7-112">Methods</span></span>

<span data-ttu-id="c83b7-113">La classe **Win32 \_ TSGatewayResourceGroup** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c83b7-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="c83b7-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="c83b7-114">Method</span></span>                                                                  | <span data-ttu-id="c83b7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c83b7-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c83b7-116">**AddResources**</span><span class="sxs-lookup"><span data-stu-id="c83b7-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="c83b7-117">Aggiunge risorse alla proprietà **Resources** per questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="c83b7-118">**Creare**</span><span class="sxs-lookup"><span data-stu-id="c83b7-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="c83b7-119">Crea un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="c83b7-120">**Delete**</span><span class="sxs-lookup"><span data-stu-id="c83b7-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="c83b7-121">Elimina questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="c83b7-122">**RemoveResources**</span><span class="sxs-lookup"><span data-stu-id="c83b7-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="c83b7-123">Elimina le risorse dalla proprietà **Resources** per questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="c83b7-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="c83b7-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="c83b7-125">Imposta la proprietà **Description** per questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="c83b7-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="c83b7-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="c83b7-127">Imposta la proprietà del **nome** per questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="c83b7-128">**SetResources**</span><span class="sxs-lookup"><span data-stu-id="c83b7-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="c83b7-129">Imposta la proprietà **Resources** per questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="c83b7-130">**Aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="c83b7-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="c83b7-131">Aggiorna questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="c83b7-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c83b7-132">Properties</span></span>

<span data-ttu-id="c83b7-133">La classe **Win32 \_ TSGatewayResourceGroup** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c83b7-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c83b7-134">**AssociatedRAPs**</span><span class="sxs-lookup"><span data-stu-id="c83b7-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83b7-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c83b7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83b7-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c83b7-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c83b7-137">Elenco delimitato da punti e virgola dei criteri di autorizzazione delle risorse Servizi Desktop remoto associati a questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="c83b7-138">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c83b7-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83b7-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c83b7-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83b7-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c83b7-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c83b7-141">Descrizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-141">Description of the resource group.</span></span> <span data-ttu-id="c83b7-142">Questa proprietà può essere modificata con il metodo [**sedescription**](setdescription-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c83b7-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c83b7-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c83b7-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83b7-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c83b7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83b7-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c83b7-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83b7-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c83b7-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c83b7-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-147">Name of the resource group.</span></span> <span data-ttu-id="c83b7-148">Questa proprietà può essere modificata con il metodo [**Sename**](setname-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c83b7-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c83b7-149">**Risorse**</span><span class="sxs-lookup"><span data-stu-id="c83b7-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83b7-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c83b7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83b7-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c83b7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c83b7-152">Elenco di risorse separate da punto e virgola in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="c83b7-153">" \* " Indica tutte le risorse.</span><span class="sxs-lookup"><span data-stu-id="c83b7-153">An "\*" means all resources.</span></span> <span data-ttu-id="c83b7-154">Questa proprietà può essere modificata con i metodi [**Seresources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)e [**Update**](update-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="c83b7-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c83b7-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="c83b7-155">Remarks</span></span>

<span data-ttu-id="c83b7-156">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="c83b7-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="c83b7-157">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c83b7-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c83b7-158">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c83b7-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c83b7-159">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c83b7-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c83b7-160">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c83b7-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c83b7-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c83b7-161">Requirements</span></span>



| <span data-ttu-id="c83b7-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83b7-162">Requirement</span></span> | <span data-ttu-id="c83b7-163">Valore</span><span class="sxs-lookup"><span data-stu-id="c83b7-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83b7-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83b7-164">Minimum supported client</span></span><br/> | <span data-ttu-id="c83b7-165">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c83b7-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c83b7-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83b7-166">Minimum supported server</span></span><br/> | <span data-ttu-id="c83b7-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c83b7-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c83b7-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c83b7-168">Namespace</span></span><br/>                | <span data-ttu-id="c83b7-169">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c83b7-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c83b7-170">MOF</span><span class="sxs-lookup"><span data-stu-id="c83b7-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c83b7-171"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c83b7-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c83b7-172">DLL</span><span class="sxs-lookup"><span data-stu-id="c83b7-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c83b7-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c83b7-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c83b7-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c83b7-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83b7-175">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b7-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="c83b7-176">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b7-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="c83b7-177">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b7-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="c83b7-178">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b7-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="c83b7-179">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b7-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="c83b7-180">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="c83b7-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

