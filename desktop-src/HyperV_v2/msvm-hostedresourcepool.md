---
description: Rappresenta una specializzazione dell'associazione di componenti di sistema che stabilisce che il pool di risorse è definito nel contesto del sistema.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Classe Msvm_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878714"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="946f9-103">\_Classe MSVM HostedResourcePool</span><span class="sxs-lookup"><span data-stu-id="946f9-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="946f9-104">Rappresenta una specializzazione dell'associazione di componenti di sistema che stabilisce che il pool di risorse è definito nel contesto del sistema.</span><span class="sxs-lookup"><span data-stu-id="946f9-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="946f9-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="946f9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="946f9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="946f9-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="946f9-107">Members</span><span class="sxs-lookup"><span data-stu-id="946f9-107">Members</span></span>

<span data-ttu-id="946f9-108">La **classe \_ HostedResourcePool di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="946f9-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="946f9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="946f9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="946f9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="946f9-110">Properties</span></span>

<span data-ttu-id="946f9-111">La **classe \_ HostedResourcePool di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="946f9-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="946f9-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="946f9-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946f9-113">Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="946f9-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="946f9-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="946f9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946f9-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregato**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="946f9-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="946f9-116">Sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="946f9-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="946f9-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="946f9-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="946f9-118">Tipo di dati: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="946f9-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="946f9-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="946f9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="946f9-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="946f9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="946f9-121">Pool di risorse che è un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="946f9-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="946f9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="946f9-122">Requirements</span></span>



| <span data-ttu-id="946f9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="946f9-123">Requirement</span></span> | <span data-ttu-id="946f9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="946f9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946f9-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="946f9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="946f9-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="946f9-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="946f9-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="946f9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="946f9-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="946f9-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="946f9-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="946f9-129">Namespace</span></span><br/>                | <span data-ttu-id="946f9-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="946f9-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="946f9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="946f9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="946f9-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="946f9-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="946f9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="946f9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="946f9-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="946f9-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

