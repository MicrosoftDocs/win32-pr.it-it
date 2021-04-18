---
description: Rappresenta un'associazione tra un sistema virtuale e lo snapshot più recente del sistema. Questa associazione può esistere solo se il sistema virtuale è stato creato utilizzando uno snapshot o se è stato creato uno snapshot dal sistema virtuale.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: Classe CIM_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310584"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="06043-104">CIM \_ MostCurrentSnapshotInBranch (classe)</span><span class="sxs-lookup"><span data-stu-id="06043-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="06043-105">Rappresenta un'associazione tra un sistema virtuale e lo snapshot più recente del sistema.</span><span class="sxs-lookup"><span data-stu-id="06043-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="06043-106">Questa associazione può esistere solo se il sistema virtuale è stato creato utilizzando uno snapshot o se è stato creato uno snapshot dal sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="06043-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="06043-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06043-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="06043-108">Members</span><span class="sxs-lookup"><span data-stu-id="06043-108">Members</span></span>

<span data-ttu-id="06043-109">La classe **CIM \_ MostCurrentSnapshotInBranch** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06043-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="06043-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06043-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06043-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06043-111">Properties</span></span>

<span data-ttu-id="06043-112">La classe **CIM \_ MostCurrentSnapshotInBranch** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06043-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06043-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="06043-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06043-114">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="06043-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="06043-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06043-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06043-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="06043-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="06043-117">Riferimento all'istanza di [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="06043-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="06043-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="06043-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06043-119">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="06043-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="06043-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06043-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06043-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="06043-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="06043-122">Riferimento all'istanza di [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) che rappresenta lo snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="06043-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06043-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06043-123">Requirements</span></span>



| <span data-ttu-id="06043-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="06043-124">Requirement</span></span> | <span data-ttu-id="06043-125">Valore</span><span class="sxs-lookup"><span data-stu-id="06043-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06043-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06043-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06043-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06043-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="06043-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06043-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06043-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06043-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="06043-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06043-130">Namespace</span></span><br/>                | <span data-ttu-id="06043-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="06043-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06043-132">MOF</span><span class="sxs-lookup"><span data-stu-id="06043-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06043-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06043-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06043-134">DLL</span><span class="sxs-lookup"><span data-stu-id="06043-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06043-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06043-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06043-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06043-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06043-137">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="06043-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

