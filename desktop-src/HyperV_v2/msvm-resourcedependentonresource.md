---
description: Stabilisce che un' \_ istanza di RESOURCEALLOCATIONSETTINGDATA CIM che rappresenta un'allocazione di risorse dipende da un'altra allocazione di risorse.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Classe Msvm_ResourceDependentOnResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313846"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="841b8-103">\_Classe MSVM ResourceDependentOnResource</span><span class="sxs-lookup"><span data-stu-id="841b8-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="841b8-104">Stabilisce che un'istanza di [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta un'allocazione di risorse dipende da un'altra allocazione di risorse.</span><span class="sxs-lookup"><span data-stu-id="841b8-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="841b8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="841b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="841b8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="841b8-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="841b8-107">Members</span><span class="sxs-lookup"><span data-stu-id="841b8-107">Members</span></span>

<span data-ttu-id="841b8-108">La **classe \_ ResourceDependentOnResource di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="841b8-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="841b8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="841b8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="841b8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="841b8-110">Properties</span></span>

<span data-ttu-id="841b8-111">La **classe \_ ResourceDependentOnResource di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="841b8-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="841b8-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="841b8-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841b8-113">Tipo di dati: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="841b8-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="841b8-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="841b8-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841b8-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="841b8-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="841b8-116">[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta la risorsa indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="841b8-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="841b8-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="841b8-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841b8-118">Tipo di dati: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="841b8-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="841b8-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="841b8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841b8-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="841b8-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="841b8-121">Un [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) che rappresenta la risorsa dipendente dall'attività precedente.</span><span class="sxs-lookup"><span data-stu-id="841b8-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="841b8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="841b8-122">Requirements</span></span>



| <span data-ttu-id="841b8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="841b8-123">Requirement</span></span> | <span data-ttu-id="841b8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="841b8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="841b8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="841b8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="841b8-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="841b8-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="841b8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="841b8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="841b8-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="841b8-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="841b8-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="841b8-129">Namespace</span></span><br/>                | <span data-ttu-id="841b8-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="841b8-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="841b8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="841b8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="841b8-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="841b8-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="841b8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="841b8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="841b8-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="841b8-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="841b8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="841b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841b8-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="841b8-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

