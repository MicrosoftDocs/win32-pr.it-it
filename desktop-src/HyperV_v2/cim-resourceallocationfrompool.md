---
description: Rappresenta un'associazione in cui \_ viene allocata un'istanza CIM ResourceAllocationSettingData da un pool di risorse.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: Classe CIM_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968026"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="4b8a3-103">CIM \_ ResourceAllocationFromPool (classe)</span><span class="sxs-lookup"><span data-stu-id="4b8a3-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="4b8a3-104">Rappresenta un'associazione in cui viene allocata un'istanza [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) da un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8a3-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8a3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b8a3-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4b8a3-106">Members</span><span class="sxs-lookup"><span data-stu-id="4b8a3-106">Members</span></span>

<span data-ttu-id="4b8a3-107">La classe **CIM \_ ResourceAllocationFromPool** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b8a3-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="4b8a3-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b8a3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b8a3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b8a3-109">Properties</span></span>

<span data-ttu-id="4b8a3-110">La classe **CIM \_ ResourceAllocationFromPool** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b8a3-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b8a3-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="4b8a3-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b8a3-112">Tipo di dati: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="4b8a3-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="4b8a3-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b8a3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b8a3-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4b8a3-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4b8a3-115">Pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8a3-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="4b8a3-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="4b8a3-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b8a3-117">Tipo di dati: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="4b8a3-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="4b8a3-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b8a3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b8a3-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="4b8a3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4b8a3-120">Dati di allocazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4b8a3-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b8a3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b8a3-121">Requirements</span></span>



| <span data-ttu-id="4b8a3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8a3-122">Requirement</span></span> | <span data-ttu-id="4b8a3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4b8a3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8a3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8a3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8a3-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4b8a3-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4b8a3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8a3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8a3-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b8a3-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4b8a3-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b8a3-128">Namespace</span></span><br/>                | <span data-ttu-id="4b8a3-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b8a3-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b8a3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4b8a3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b8a3-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b8a3-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b8a3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8a3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b8a3-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b8a3-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b8a3-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b8a3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8a3-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="4b8a3-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

