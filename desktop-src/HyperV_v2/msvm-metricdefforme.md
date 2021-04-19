---
description: Definisce l'associazione tra un MSVM \_ BaseMetricDefinition e un oggetto \_ gestito CIM per definire le metriche per quest'ultimo. La definizione delle metriche viene configurata in base al contesto da Managed, motivo per cui la definizione dipende dall'elemento.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Classe Msvm_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311790"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="459d7-104">\_Classe MSVM MetricDefForME</span><span class="sxs-lookup"><span data-stu-id="459d7-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="459d7-105">Definisce l'associazione tra un [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) e un [**oggetto \_ gestito CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) per definire le metriche per quest'ultimo.</span><span class="sxs-lookup"><span data-stu-id="459d7-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="459d7-106">La definizione delle metriche viene configurata in base al contesto da Managed, motivo per cui la definizione dipende dall'elemento.</span><span class="sxs-lookup"><span data-stu-id="459d7-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="459d7-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="459d7-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="459d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="459d7-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="459d7-109">Members</span><span class="sxs-lookup"><span data-stu-id="459d7-109">Members</span></span>

<span data-ttu-id="459d7-110">La **classe \_ MetricDefForME di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="459d7-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="459d7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="459d7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="459d7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="459d7-112">Properties</span></span>

<span data-ttu-id="459d7-113">La **classe \_ MetricDefForME di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="459d7-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="459d7-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="459d7-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459d7-115">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="459d7-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="459d7-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="459d7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="459d7-117">Riferimento a un'istanza della classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta l'elemento gestito che può avere metriche del tipo definito da **dipendente** applicato.</span><span class="sxs-lookup"><span data-stu-id="459d7-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="459d7-118">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="459d7-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="459d7-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="459d7-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459d7-120">Tipo di dati: **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="459d7-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="459d7-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="459d7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="459d7-122">Riferimento a un'istanza della classe [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che rappresenta la definizione della metrica a cui è possibile applicare l'attività **precedente** .</span><span class="sxs-lookup"><span data-stu-id="459d7-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="459d7-123">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="459d7-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="459d7-124">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="459d7-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459d7-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="459d7-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="459d7-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="459d7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="459d7-127">Indica se la metrica definita da **dipendente** viene raccolta per l'attività **precedente**.</span><span class="sxs-lookup"><span data-stu-id="459d7-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="459d7-128">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="459d7-128">This will be one of the following values.</span></span>



| <span data-ttu-id="459d7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="459d7-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="459d7-130">Significato</span><span class="sxs-lookup"><span data-stu-id="459d7-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="459d7-131"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="459d7-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="459d7-132">È in corso la raccolta della metrica.</span><span class="sxs-lookup"><span data-stu-id="459d7-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="459d7-133"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="459d7-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="459d7-134">La metrica non viene raccolta.</span><span class="sxs-lookup"><span data-stu-id="459d7-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="459d7-135"><dt>**Riservato**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="459d7-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="459d7-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="459d7-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="459d7-137">La metrica viene raccolta per alcuni, ma non per tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="459d7-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="459d7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="459d7-138">Requirements</span></span>



| <span data-ttu-id="459d7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="459d7-139">Requirement</span></span> | <span data-ttu-id="459d7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="459d7-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="459d7-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="459d7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="459d7-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="459d7-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="459d7-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="459d7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="459d7-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="459d7-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="459d7-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="459d7-145">Namespace</span></span><br/>                | <span data-ttu-id="459d7-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="459d7-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="459d7-147">MOF</span><span class="sxs-lookup"><span data-stu-id="459d7-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="459d7-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="459d7-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="459d7-149">DLL</span><span class="sxs-lookup"><span data-stu-id="459d7-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="459d7-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="459d7-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

