---
description: Fornisce un collegamento tra l'istanza delle funzionalità del commutere Ethernet e le impostazioni minime, massime, incrementali e predefinite per una risorsa.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Classe Msvm_FeatureSettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307914"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="c8958-103">\_Classe MSVM FeatureSettingsDefineCapabilities</span><span class="sxs-lookup"><span data-stu-id="c8958-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="c8958-104">Fornisce un collegamento tra l'istanza delle funzionalità del commutere Ethernet e le impostazioni minime, massime, incrementali e predefinite per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c8958-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="c8958-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c8958-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8958-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8958-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="c8958-107">Members</span><span class="sxs-lookup"><span data-stu-id="c8958-107">Members</span></span>

<span data-ttu-id="c8958-108">La **classe \_ FeatureSettingsDefineCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c8958-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c8958-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8958-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8958-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8958-110">Properties</span></span>

<span data-ttu-id="c8958-111">La **classe \_ FeatureSettingsDefineCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c8958-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8958-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c8958-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8958-113">Tipo di dati: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="c8958-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c8958-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8958-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8958-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="c8958-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c8958-116">Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) che rappresenta le funzionalità della funzionalità del comcambio Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c8958-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="c8958-117">Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="c8958-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="c8958-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c8958-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8958-119">Tipo di dati: **[ **MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="c8958-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c8958-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8958-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8958-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c8958-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c8958-122">Riferimento a un'istanza della classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) che rappresenta le impostazioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c8958-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="c8958-123">Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="c8958-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="c8958-124">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="c8958-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8958-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8958-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8958-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8958-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8958-127">Specifica se le proprietà non **null** e non chiave di **PartComponent** vengono gestite in modo indipendente o come set correlato.</span><span class="sxs-lookup"><span data-stu-id="c8958-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="c8958-128">Ad esempio, è possibile definire un set indipendente di proprietà massime, ma non esiste alcuna relazione tra ciascuna proprietà.</span><span class="sxs-lookup"><span data-stu-id="c8958-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="c8958-129">D'altra parte, potrebbe essere necessario definire diversi set correlati di proprietà massime quando i valori massimi di ciascuno dipendono da altri.</span><span class="sxs-lookup"><span data-stu-id="c8958-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="c8958-130">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8958-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c8958-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Indipendente** (0)</span><span class="sxs-lookup"><span data-stu-id="c8958-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c8958-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlato** (1)</span><span class="sxs-lookup"><span data-stu-id="c8958-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8958-133">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="c8958-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8958-134">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8958-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8958-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8958-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8958-136">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="c8958-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8958-137">Indica un'ulteriore semantica sull'interpretazione di tutte le proprietà non **null** e non chiave dei dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="c8958-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="c8958-138">I valori riportati di seguito vengono valutati solo in base alle proprietà numeriche non **null**, non chiave, non enumerate e non booleane dei dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="c8958-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="c8958-139">Ogni proprietà del set deve essere paragonabile in modo matematico ad altre istanze della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c8958-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="c8958-140">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8958-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="c8958-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c8958-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="c8958-142">Significato</span><span class="sxs-lookup"><span data-stu-id="c8958-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="c8958-143"><dt>**Punto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="c8958-144">Questa istanza di dati di impostazione fornisce un solo set di valori.</span><span class="sxs-lookup"><span data-stu-id="c8958-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="c8958-145"><dt>**Minimo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="c8958-146">I dati di questa impostazione forniscono valori minimi per le proprietà valutate.</span><span class="sxs-lookup"><span data-stu-id="c8958-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="c8958-147">Se usato con **PropertyPolicy** = "Independent", è necessario specificare solo una di queste impostazioni per particolare istanza dei dati di impostazione per tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c8958-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="c8958-148">A meno che non venga limitato da un valore massimo nello stesso set di proprietà, tutti i valori che si confrontano più in alto rispetto ai valori specificati vengono anche considerati supportati dall'istanza delle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="c8958-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="c8958-149"><dt>**Massimo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="c8958-150">I dati di questa impostazione forniscono valori massimi per le proprietà valutate.</span><span class="sxs-lookup"><span data-stu-id="c8958-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="c8958-151">Se usato con **PropertyPolicy** = "Independent", è necessario specificare solo una di queste impostazioni per particolare istanza dei dati di impostazione per tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c8958-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="c8958-152">A meno che non venga limitato da un valore minimo nello stesso set di proprietà, tutti i valori che si confrontano con valori inferiori a quelli specificati sono considerati supportati anche dall'istanza delle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="c8958-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="c8958-153"><dt>**Incrementi**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="c8958-154">I dati di questa impostazione forniscono valori di incremento per le proprietà valutate.</span><span class="sxs-lookup"><span data-stu-id="c8958-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="c8958-155">Per le funzionalità associate, se una proprietà valutata non dispone attualmente di valori minimi o massimi corrispondenti, la proprietà non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="c8958-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="c8958-156">In caso contrario, per ogni proprietà valutata, il relativo valore (*x*) deve essere compreso tra *MinimumValue* e *MaximumValue*, incluso, e deve avere la proprietà che il risultato di *MaximumValue* meno *x* e il risultato di *x* meno *MinimumValue* sono ciascuno un multiplo Integer dell' *incremento*.</span><span class="sxs-lookup"><span data-stu-id="c8958-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="c8958-157">Se *MinimumValue* o *MaximumValue* non è specificato e l'altro è, il valore mancante deve essere considerato rispettivamente il valore minimo o massimo supportato per il tipo di dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c8958-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="c8958-158">Inoltre, se si specificano sia *MinimumValue* che *MaximumValue* per una proprietà valutata, il risultato di *MaximumValue* meno *MinimumValue* deve essere un multiplo Integer dell' *incremento*.</span><span class="sxs-lookup"><span data-stu-id="c8958-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c8958-159">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="c8958-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8958-160">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8958-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8958-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8958-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8958-162">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="c8958-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c8958-163">Specifica un'ulteriore semantica sull'interpretazione delle proprietà non **null** e non chiave dei dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="c8958-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="c8958-164">Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8958-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="c8958-165">Valore</span><span class="sxs-lookup"><span data-stu-id="c8958-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="c8958-166">Significato</span><span class="sxs-lookup"><span data-stu-id="c8958-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="c8958-167"><dt>**Valore predefinito**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="c8958-168">I valori delle proprietà dei dati delle impostazioni verranno utilizzati come valori predefiniti, quando viene creata una nuova istanza di dati di impostazione per gli elementi le cui funzionalità sono definite dalle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="c8958-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="c8958-169">Per le istanze dei dati di impostazione, per determinate proprietà aventi lo stesso scopo semantico, è necessario specificare al massimo un'istanza di tali dati di impostazione come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c8958-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="c8958-170"><dt>**Ottimale**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="c8958-171">L'istanza dei dati di impostazione rappresenta valori di impostazione ottimali per gli elementi associati alle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="c8958-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="c8958-172">Le istanze di dati di impostazione di più componenti possono essere dichiarate come ottimali.</span><span class="sxs-lookup"><span data-stu-id="c8958-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="c8958-173"><dt>**Media**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="c8958-174">Le proprietà numeriche non **null**, non di tipo Key, non enumerate e non booleane dell'istanza dei dati di impostazione associata rappresentano un punto medio lungo una certa dimensione.</span><span class="sxs-lookup"><span data-stu-id="c8958-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="c8958-175">Per diverse combinazioni di impostazione delle proprietà dei dati, è possibile che più istanze di dati delle impostazioni dei componenti vengano dichiarate come **medie**.</span><span class="sxs-lookup"><span data-stu-id="c8958-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="c8958-176"><dt>**Supportato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="c8958-177">Le proprietà non **null** non chiave dei dati dell'impostazione rappresentano un set di valori di proprietà supportati che non sono altrimenti qualificati.</span><span class="sxs-lookup"><span data-stu-id="c8958-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8958-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8958-178">Requirements</span></span>



| <span data-ttu-id="c8958-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8958-179">Requirement</span></span> | <span data-ttu-id="c8958-180">Valore</span><span class="sxs-lookup"><span data-stu-id="c8958-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8958-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8958-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c8958-182">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c8958-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8958-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8958-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c8958-184">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c8958-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8958-185">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c8958-185">Namespace</span></span><br/>                | <span data-ttu-id="c8958-186">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c8958-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8958-187">MOF</span><span class="sxs-lookup"><span data-stu-id="c8958-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8958-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8958-189">DLL</span><span class="sxs-lookup"><span data-stu-id="c8958-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8958-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8958-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

