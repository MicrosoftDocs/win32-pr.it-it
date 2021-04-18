---
description: Gestisce le funzionalità dell'istanza CIM \_ ResourcePoolConfigurationService per un oggetto CIM \_ ResourcePool.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: Classe CIM_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307780"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="0e39a-103">CIM \_ ResourcePoolConfigurationCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="0e39a-103">CIM\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="0e39a-104">Gestisce le funzionalità dell'istanza [**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) per un oggetto [**CIM \_ ResourcePool**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="0e39a-104">Manages the capabilities of the [**CIM\_ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) instance for a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e39a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e39a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="0e39a-106">Members</span><span class="sxs-lookup"><span data-stu-id="0e39a-106">Members</span></span>

<span data-ttu-id="0e39a-107">La classe **CIM \_ ResourcePoolConfigurationCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e39a-107">The **CIM\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0e39a-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e39a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e39a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e39a-109">Properties</span></span>

<span data-ttu-id="0e39a-110">La classe **CIM \_ ResourcePoolConfigurationCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e39a-110">The **CIM\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e39a-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="0e39a-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39a-112">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e39a-112">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="0e39a-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e39a-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39a-114">Metodi del servizio di configurazione supportati per le operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="0e39a-114">The methods of the configuration service that are supported for asynchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-115">**CreateResourcePool è supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39a-115">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-116">**CreateChild ResourcePool è supportato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39a-116">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-117">**DeleteResourcePool è supportato** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39a-117">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-118">**AddResourcesToResourcePool è supportato** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39a-118">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-119">**RemoveResourcesFromResourcePool è supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="0e39a-119">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-120">**ChangeParentResourcePool è supportato** (7)</span><span class="sxs-lookup"><span data-stu-id="0e39a-120">**ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e39a-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0e39a-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e39a-122">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e39a-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e39a-123">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="0e39a-123">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e39a-124">Tipo di dati: matrice **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e39a-124">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="0e39a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0e39a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e39a-126">Metodi del servizio di configurazione supportati per le operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="0e39a-126">The methods of the configuration service that are supported for synchronous operations.</span></span>

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-127">**CreateResourcePool è supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="0e39a-127">**CreateResourcePool is supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-128">**CreateChild ResourcePool è supportato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e39a-128">**CreateChild ResourcePool is supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-129">**DeleteResourcePool è supportato** (4)</span><span class="sxs-lookup"><span data-stu-id="0e39a-129">**DeleteResourcePool is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-130">**AddResourcesToResourcePool è supportato** (5)</span><span class="sxs-lookup"><span data-stu-id="0e39a-130">**AddResourcesToResourcePool is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-131">**RemoveResourcesFromResourcePool è supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="0e39a-131">**RemoveResourcesFromResourcePool is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="0e39a-132">**CIM \_ ChangeParentResourcePool è supportato** (7)</span><span class="sxs-lookup"><span data-stu-id="0e39a-132">**CIM\_ChangeParentResourcePool is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e39a-133">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0e39a-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e39a-134">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e39a-134">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="0e39a-135"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0e39a-135"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0e39a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e39a-136">Requirements</span></span>



| <span data-ttu-id="0e39a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e39a-137">Requirement</span></span> | <span data-ttu-id="0e39a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="0e39a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e39a-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e39a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0e39a-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0e39a-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0e39a-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e39a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0e39a-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0e39a-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0e39a-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e39a-143">Namespace</span></span><br/>                | <span data-ttu-id="0e39a-144">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e39a-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e39a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="0e39a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e39a-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e39a-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e39a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0e39a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e39a-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e39a-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e39a-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e39a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e39a-150">**\_Funzionalità CIM**</span><span class="sxs-lookup"><span data-stu-id="0e39a-150">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

 




