---
description: Rappresenta un'associazione tra un servizio e un elemento gestito che potrebbe essere influenzato dalla relativa esecuzione.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Classe CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307764"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="ca58e-103">CIM \_ ServiceAffectsElement (classe)</span><span class="sxs-lookup"><span data-stu-id="ca58e-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="ca58e-104">Rappresenta un'associazione tra un servizio e un elemento gestito che potrebbe essere influenzato dalla relativa esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ca58e-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca58e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca58e-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="ca58e-106">Members</span><span class="sxs-lookup"><span data-stu-id="ca58e-106">Members</span></span>

<span data-ttu-id="ca58e-107">La classe **CIM \_ ServiceAffectsElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca58e-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ca58e-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca58e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca58e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca58e-109">Properties</span></span>

<span data-ttu-id="ca58e-110">La classe **CIM \_ ServiceAffectsElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca58e-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca58e-111">**Interessato**</span><span class="sxs-lookup"><span data-stu-id="ca58e-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca58e-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="ca58e-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca58e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-114">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca58e-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca58e-115">Elemento gestito interessato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="ca58e-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="ca58e-116">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="ca58e-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca58e-117">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="ca58e-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca58e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca58e-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca58e-120">Il servizio che influisce sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="ca58e-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="ca58e-121">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="ca58e-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca58e-122">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca58e-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca58e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-124">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="ca58e-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ca58e-125">Effetto sull'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="ca58e-125">The effect on the managed element.</span></span> <span data-ttu-id="ca58e-126">Questa matrice corrisponde alla matrice **OtherElementEffectsDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="ca58e-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="ca58e-127">\- Uso esclusivo (2): nessun altro servizio può avere questa associazione all'elemento.</span><span class="sxs-lookup"><span data-stu-id="ca58e-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="ca58e-128">\- Impatto sulle prestazioni (3): deprecato a favore di "consumi", "miglioramento delle prestazioni" o "peggioramento delle prestazioni".</span><span class="sxs-lookup"><span data-stu-id="ca58e-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="ca58e-129">L'esecuzione del servizio può migliorare o peggiorare le prestazioni dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ca58e-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="ca58e-130">Questo può essere un effetto collaterale dell'esecuzione o come una conseguenza prevista dei metodi forniti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="ca58e-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="ca58e-131">\- Integrità elementi (4): deprecato a favore di "consumer", "migliora l'integrità" o "peggiora l'integrità".</span><span class="sxs-lookup"><span data-stu-id="ca58e-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="ca58e-132">L'esecuzione del servizio può migliorare o peggiorare l'integrità dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ca58e-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="ca58e-133">Questo può essere un effetto collaterale dell'esecuzione o come una conseguenza prevista dei metodi forniti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="ca58e-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="ca58e-134">\- Gestisce (5): il servizio gestisce l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ca58e-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="ca58e-135">\- Utilizza (6): l'esecuzione del servizio utilizza parte o tutto l'elemento associato come conseguenza dell'esecuzione del servizio.</span><span class="sxs-lookup"><span data-stu-id="ca58e-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="ca58e-136">Il servizio, ad esempio, può utilizzare cicli CPU, che possono influire sulle prestazioni o l'archiviazione, che può influire sia sulle prestazioni che sull'integrità.</span><span class="sxs-lookup"><span data-stu-id="ca58e-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="ca58e-137">Ad esempio, la mancanza di spazio di archiviazione disponibile può compromettere l'integrità riducendo la possibilità di salvare lo stato.</span><span class="sxs-lookup"><span data-stu-id="ca58e-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="ca58e-138">) "Consumi" può essere utilizzato da solo o insieme ad altri valori, in particolare, "peggiora le prestazioni" e "peggiora l'integrità".</span><span class="sxs-lookup"><span data-stu-id="ca58e-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="ca58e-139">Per riflettere i servizi di allocazione che possono essere forniti da un servizio, è necessario usare "manages" e not "consums".</span><span class="sxs-lookup"><span data-stu-id="ca58e-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="ca58e-140">\- Migliora l'integrità (7): il servizio può migliorare l'integrità dell'elemento associato.</span><span class="sxs-lookup"><span data-stu-id="ca58e-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="ca58e-141">\- Peggiora l'integrità (8): il servizio può influire negativamente sull'integrità dell'elemento associato.</span><span class="sxs-lookup"><span data-stu-id="ca58e-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="ca58e-142">\- Ottimizza le prestazioni (9): il servizio può migliorare le prestazioni dell'elemento associato.</span><span class="sxs-lookup"><span data-stu-id="ca58e-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="ca58e-143">\- Peggiora le prestazioni (10): il servizio può influire negativamente sulle prestazioni dell'elemento associato.</span><span class="sxs-lookup"><span data-stu-id="ca58e-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ca58e-144">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ca58e-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ca58e-145">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ca58e-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="ca58e-146">**Utilizzo esclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="ca58e-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="ca58e-147">**Effetti sulle prestazioni** (3)</span><span class="sxs-lookup"><span data-stu-id="ca58e-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="ca58e-148">**Integrità elementi** (4)</span><span class="sxs-lookup"><span data-stu-id="ca58e-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="ca58e-149">**Gestione** (5)</span><span class="sxs-lookup"><span data-stu-id="ca58e-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="ca58e-150">**Utilizza** (6)</span><span class="sxs-lookup"><span data-stu-id="ca58e-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="ca58e-151">**Migliora l'integrità** (7)</span><span class="sxs-lookup"><span data-stu-id="ca58e-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="ca58e-152">**Peggiora l'integrità** (8)</span><span class="sxs-lookup"><span data-stu-id="ca58e-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="ca58e-153">**Miglioramento delle prestazioni** (9)</span><span class="sxs-lookup"><span data-stu-id="ca58e-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="ca58e-154">**Peggiora le prestazioni** (10)</span><span class="sxs-lookup"><span data-stu-id="ca58e-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ca58e-155">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ca58e-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ca58e-156">**Fornitore riservato** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ca58e-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ca58e-157">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ca58e-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca58e-158">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ca58e-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca58e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca58e-160">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="ca58e-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="ca58e-161">Ogni elemento nella matrice fornisce informazioni aggiuntive per l'elemento corrispondente nella matrice **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="ca58e-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="ca58e-162">Una descrizione è obbligatoria per qualsiasi elemento nella matrice **ElementEffects** impostata su **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="ca58e-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca58e-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca58e-163">Requirements</span></span>



| <span data-ttu-id="ca58e-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca58e-164">Requirement</span></span> | <span data-ttu-id="ca58e-165">Valore</span><span class="sxs-lookup"><span data-stu-id="ca58e-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca58e-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca58e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="ca58e-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ca58e-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ca58e-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca58e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="ca58e-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca58e-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ca58e-170">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca58e-170">Namespace</span></span><br/>                | <span data-ttu-id="ca58e-171">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ca58e-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ca58e-172">MOF</span><span class="sxs-lookup"><span data-stu-id="ca58e-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca58e-173"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca58e-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca58e-174">DLL</span><span class="sxs-lookup"><span data-stu-id="ca58e-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca58e-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca58e-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

