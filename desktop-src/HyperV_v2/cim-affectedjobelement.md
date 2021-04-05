---
description: Rappresenta un'associazione tra un processo e gli \_ oggetti CIM gestiti che potrebbero essere interessati dalla relativa esecuzione.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: Classe CIM_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131215"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="04dbe-103">CIM \_ AffectedJobElement (classe)</span><span class="sxs-lookup"><span data-stu-id="04dbe-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="04dbe-104">Rappresenta un'associazione tra un processo e gli oggetti **CIM \_ gestiti** che potrebbero essere interessati dalla relativa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="04dbe-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="04dbe-105">Potrebbe non essere possibile per il processo descrivere tutti gli elementi interessati.</span><span class="sxs-lookup"><span data-stu-id="04dbe-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="04dbe-106">Lo scopo principale di questa associazione è fornire informazioni quando un processo richiede l'uso esclusivo degli elementi gestiti interessati o quando descrive gli effetti collaterali che possono verificarsi.</span><span class="sxs-lookup"><span data-stu-id="04dbe-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="04dbe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04dbe-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="04dbe-108">Members</span><span class="sxs-lookup"><span data-stu-id="04dbe-108">Members</span></span>

<span data-ttu-id="04dbe-109">La classe **CIM \_ AffectedJobElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="04dbe-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="04dbe-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04dbe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04dbe-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04dbe-111">Properties</span></span>

<span data-ttu-id="04dbe-112">La classe **CIM \_ AffectedJobElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="04dbe-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04dbe-113">**Interessato**</span><span class="sxs-lookup"><span data-stu-id="04dbe-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04dbe-114">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="04dbe-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04dbe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-116">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="04dbe-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="04dbe-117">Elemento gestito interessato dall'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="04dbe-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="04dbe-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="04dbe-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04dbe-119">Tipo di dati **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="04dbe-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04dbe-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-121">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="04dbe-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="04dbe-122">Processo che influisce sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="04dbe-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="04dbe-123">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="04dbe-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04dbe-124">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04dbe-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04dbe-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-126">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="04dbe-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="04dbe-127">Effetto del processo sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="04dbe-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04dbe-128">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="04dbe-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04dbe-129">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="04dbe-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="04dbe-130">**Utilizzo esclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="04dbe-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="04dbe-131">**Effetti sulle prestazioni** (3)</span><span class="sxs-lookup"><span data-stu-id="04dbe-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="04dbe-132">**Integrità elementi** (4)</span><span class="sxs-lookup"><span data-stu-id="04dbe-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="04dbe-133">**Creazione** (5)</span><span class="sxs-lookup"><span data-stu-id="04dbe-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04dbe-134">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="04dbe-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04dbe-135">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="04dbe-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04dbe-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04dbe-137">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="04dbe-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="04dbe-138">Dettagli aggiuntivi per i valori corrispondenti "1" (altro) nella matrice **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="04dbe-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04dbe-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04dbe-139">Requirements</span></span>



| <span data-ttu-id="04dbe-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="04dbe-140">Requirement</span></span> | <span data-ttu-id="04dbe-141">Valore</span><span class="sxs-lookup"><span data-stu-id="04dbe-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04dbe-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04dbe-142">Minimum supported client</span></span><br/> | <span data-ttu-id="04dbe-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04dbe-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="04dbe-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04dbe-144">Minimum supported server</span></span><br/> | <span data-ttu-id="04dbe-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04dbe-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="04dbe-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="04dbe-146">Namespace</span></span><br/>                | <span data-ttu-id="04dbe-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="04dbe-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="04dbe-148">MOF</span><span class="sxs-lookup"><span data-stu-id="04dbe-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04dbe-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04dbe-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04dbe-150">DLL</span><span class="sxs-lookup"><span data-stu-id="04dbe-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04dbe-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04dbe-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

