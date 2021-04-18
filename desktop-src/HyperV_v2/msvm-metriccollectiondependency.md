---
description: Rappresenta l'associazione tra due definizioni delle metriche o due valori di metrica.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Classe Msvm_MetricCollectionDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318340"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="0f141-103">\_Classe MSVM MetricCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="0f141-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="0f141-104">Rappresenta l'associazione tra due definizioni delle metriche o due valori di metrica.</span><span class="sxs-lookup"><span data-stu-id="0f141-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="0f141-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0f141-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f141-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f141-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0f141-107">Members</span><span class="sxs-lookup"><span data-stu-id="0f141-107">Members</span></span>

<span data-ttu-id="0f141-108">La **classe \_ MetricCollectionDependency di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0f141-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0f141-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f141-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f141-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f141-110">Properties</span></span>

<span data-ttu-id="0f141-111">La **classe \_ MetricCollectionDependency di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0f141-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f141-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0f141-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f141-113">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0f141-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0f141-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f141-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f141-115">Riferimento a un'istanza della classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta la definizione o il valore della metrica indipendente.</span><span class="sxs-lookup"><span data-stu-id="0f141-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="0f141-116">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="0f141-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="0f141-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="0f141-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f141-118">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="0f141-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="0f141-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f141-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f141-120">Riferimento a un'istanza della classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta la definizione della metrica o il valore della metrica dipendente dall'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="0f141-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="0f141-121">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="0f141-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f141-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f141-122">Requirements</span></span>



| <span data-ttu-id="0f141-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f141-123">Requirement</span></span> | <span data-ttu-id="0f141-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0f141-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f141-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f141-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0f141-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0f141-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f141-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f141-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0f141-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0f141-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f141-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f141-129">Namespace</span></span><br/>                | <span data-ttu-id="0f141-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f141-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f141-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0f141-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f141-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f141-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f141-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0f141-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f141-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f141-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

