---
description: Rappresenta un'associazione tra un sistema di computer e lo snapshot del sistema virtuale applicato più di recente.
ms.assetid: 722491a3-1c46-4d37-8bd6-7c7d6648a806
title: Classe CIM_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSnapshot
- CIM_LastAppliedSnapshot.Antecedent
- CIM_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 38efa9c5f02cd0ea40d993cc39ba05ac0b6fde3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320043"
---
# <a name="cim_lastappliedsnapshot-class"></a><span data-ttu-id="632e6-103">CIM \_ LastAppliedSnapshot (classe)</span><span class="sxs-lookup"><span data-stu-id="632e6-103">CIM\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="632e6-104">Rappresenta un'associazione tra un sistema di computer e lo snapshot del sistema virtuale applicato più di recente.</span><span class="sxs-lookup"><span data-stu-id="632e6-104">Represents an association between a computer system and its most recently applied virtual system snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="632e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="632e6-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_LastAppliedSnapshot : CIM_Dependency
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="632e6-106">Members</span><span class="sxs-lookup"><span data-stu-id="632e6-106">Members</span></span>

<span data-ttu-id="632e6-107">La classe **CIM \_ LastAppliedSnapshot** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="632e6-107">The **CIM\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="632e6-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="632e6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="632e6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="632e6-109">Properties</span></span>

<span data-ttu-id="632e6-110">La classe **CIM \_ LastAppliedSnapshot** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="632e6-110">The **CIM\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="632e6-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="632e6-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="632e6-112">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="632e6-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="632e6-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="632e6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="632e6-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="632e6-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="632e6-115">Snapshot del sistema virtuale che è stato applicato per ultimo al sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="632e6-115">The virtual system snapshot that was last applied to the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="632e6-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="632e6-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="632e6-117">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="632e6-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="632e6-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="632e6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="632e6-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="632e6-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="632e6-120">Sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="632e6-120">The computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="632e6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="632e6-121">Requirements</span></span>



| <span data-ttu-id="632e6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="632e6-122">Requirement</span></span> | <span data-ttu-id="632e6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="632e6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632e6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="632e6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="632e6-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="632e6-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="632e6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="632e6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="632e6-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="632e6-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="632e6-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="632e6-128">Namespace</span></span><br/>                | <span data-ttu-id="632e6-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="632e6-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="632e6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="632e6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="632e6-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="632e6-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="632e6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="632e6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="632e6-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="632e6-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="632e6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="632e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632e6-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="632e6-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

