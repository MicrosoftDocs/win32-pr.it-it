---
description: Un'associazione tra un'istanza di MSVM \_ VssComponent e un'istanza di MSVM \_ VssService che rappresenta un servizio per l'esecuzione di operazioni sul componente VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Classe Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314328"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="e4841-103">\_Classe MSVM ServiceOfVssComponent</span><span class="sxs-lookup"><span data-stu-id="e4841-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="e4841-104">Un'associazione tra un'istanza di [**MSVM \_ VssComponent**](msvm-vsscomponent.md) e un'istanza di [**MSVM \_ VssService**](msvm-vssservice.md) che rappresenta un servizio per l'esecuzione di operazioni sul componente VSS.</span><span class="sxs-lookup"><span data-stu-id="e4841-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="e4841-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e4841-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4841-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4841-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e4841-107">Members</span><span class="sxs-lookup"><span data-stu-id="e4841-107">Members</span></span>

<span data-ttu-id="e4841-108">La **classe \_ ServiceOfVssComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e4841-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e4841-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4841-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4841-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4841-110">Properties</span></span>

<span data-ttu-id="e4841-111">La **classe \_ ServiceOfVssComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4841-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4841-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e4841-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4841-113">Tipo di dati: **MSVM \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="e4841-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="e4841-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4841-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4841-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e4841-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e4841-116">, [**MSVM \_ VssComponent**](msvm-vsscomponent.md) che rappresenta il componente VSS.</span><span class="sxs-lookup"><span data-stu-id="e4841-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="e4841-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="e4841-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4841-118">Tipo di dati: **MSVM \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="e4841-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="e4841-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e4841-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4841-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. dependent")</span><span class="sxs-lookup"><span data-stu-id="e4841-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e4841-121">Un [**\_ VssService MSVM**](msvm-vssservice.md) che rappresenta il servizio IC VSS.</span><span class="sxs-lookup"><span data-stu-id="e4841-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4841-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4841-122">Requirements</span></span>



| <span data-ttu-id="e4841-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4841-123">Requirement</span></span> | <span data-ttu-id="e4841-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e4841-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4841-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4841-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e4841-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e4841-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e4841-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4841-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e4841-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e4841-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e4841-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4841-129">Namespace</span></span><br/>                | <span data-ttu-id="e4841-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e4841-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e4841-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e4841-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4841-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4841-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4841-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e4841-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4841-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4841-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4841-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4841-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4841-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="e4841-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

