---
description: Rappresenta un'associazione tra un sistema virtuale e i dati di impostazione dello snapshot che è stato applicato più di recente al sistema virtuale.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Classe Msvm_LastAppliedSnapshot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311797"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="89e2c-103">\_Classe MSVM LastAppliedSnapshot</span><span class="sxs-lookup"><span data-stu-id="89e2c-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="89e2c-104">Rappresenta un'associazione tra un sistema virtuale e i dati di impostazione dello snapshot che è stato applicato più di recente al sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="89e2c-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="89e2c-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="89e2c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e2c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89e2c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="89e2c-107">Members</span><span class="sxs-lookup"><span data-stu-id="89e2c-107">Members</span></span>

<span data-ttu-id="89e2c-108">La **classe \_ LastAppliedSnapshot di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="89e2c-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="89e2c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89e2c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89e2c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89e2c-110">Properties</span></span>

<span data-ttu-id="89e2c-111">La **classe \_ LastAppliedSnapshot di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="89e2c-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89e2c-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="89e2c-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e2c-113">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="89e2c-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="89e2c-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89e2c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89e2c-115">Qualificatori: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="89e2c-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="89e2c-116">Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot del sistema virtuale che è stato applicato per ultimo al sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="89e2c-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="89e2c-117">Questa proprietà viene ereditata **dalla \_ dipendenza CIM**.</span><span class="sxs-lookup"><span data-stu-id="89e2c-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="89e2c-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="89e2c-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e2c-119">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="89e2c-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="89e2c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89e2c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89e2c-121">Qualificatori: **override**, **min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="89e2c-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="89e2c-122">Riferimento a un'istanza della classe [**\_ ComputerSystem MSVM**](msvm-computersystem.md) che rappresenta il sistema virtuale su cui è stato applicato più di recente lo snapshot del sistema virtuale rappresentato dalla proprietà **precedente** .</span><span class="sxs-lookup"><span data-stu-id="89e2c-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="89e2c-123">Questa proprietà viene ereditata **dalla \_ dipendenza CIM**.</span><span class="sxs-lookup"><span data-stu-id="89e2c-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89e2c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89e2c-124">Requirements</span></span>



| <span data-ttu-id="89e2c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e2c-125">Requirement</span></span> | <span data-ttu-id="89e2c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="89e2c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89e2c-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89e2c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89e2c-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89e2c-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="89e2c-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89e2c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89e2c-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="89e2c-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89e2c-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89e2c-131">Namespace</span></span><br/>                | <span data-ttu-id="89e2c-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="89e2c-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89e2c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="89e2c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89e2c-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89e2c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89e2c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="89e2c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e2c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89e2c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




