---
description: Rappresenta un'associazione tra le proprietà di un' \_ istanza CIM SettingData e un' \_ istanza di funzionalità CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: Classe CIM_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314838"
---
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="17e85-103">CIM \_ SettingsDefineCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="17e85-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="17e85-104">Rappresenta un'associazione tra le proprietà di un'istanza [**CIM \_ SettingData**](cim-settingdata.md) e un'istanza di [**\_ funzionalità CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="17e85-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e85-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17e85-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a><span data-ttu-id="17e85-106">Members</span><span class="sxs-lookup"><span data-stu-id="17e85-106">Members</span></span>

<span data-ttu-id="17e85-107">La classe **CIM \_ SettingsDefineCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="17e85-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="17e85-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17e85-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17e85-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17e85-109">Properties</span></span>

<span data-ttu-id="17e85-110">La classe **CIM \_ SettingsDefineCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="17e85-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17e85-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="17e85-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e85-112">Tipo di dati **: \_ funzionalità CIM**</span><span class="sxs-lookup"><span data-stu-id="17e85-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="17e85-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17e85-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e85-114">Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="17e85-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="17e85-115">Riferimento all'istanza di [**\_ funzionalità CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="17e85-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="17e85-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="17e85-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e85-117">Tipo di dati: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="17e85-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="17e85-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17e85-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e85-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="17e85-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="17e85-120">Riferimento all'istanza di [**CIM \_ SettingData**](cim-settingdata.md) usata per definire l'istanza [**di \_ funzionalità CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="17e85-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="17e85-121">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="17e85-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e85-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17e85-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17e85-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17e85-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e85-124">Qualificatori: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="17e85-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="17e85-125">Indica se le proprietà non null e non chiave dell'istanza [**\_ SettingData CIM**](cim-settingdata.md) associata vengono gestite in modo indipendente o come set correlato.</span><span class="sxs-lookup"><span data-stu-id="17e85-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="17e85-126">Ad esempio, un set indipendente di proprietà massime può essere definito quando non esiste alcuna relazione tra ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="17e85-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="17e85-127">Al contrario, potrebbe essere necessario definire diversi set correlati di proprietà massime quando i valori massimi di ciascuno dipendono da altri.</span><span class="sxs-lookup"><span data-stu-id="17e85-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="17e85-128">**Indipendente** (0)</span><span class="sxs-lookup"><span data-stu-id="17e85-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="17e85-129">**Correlato** (1)</span><span class="sxs-lookup"><span data-stu-id="17e85-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="17e85-130">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="17e85-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17e85-131">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="17e85-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e85-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17e85-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17e85-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17e85-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e85-134">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRole**")</span><span class="sxs-lookup"><span data-stu-id="17e85-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="17e85-135">Indica il tipo di intervallo di valori utilizzato dalle proprietà delle proprietà non null e non chiave dell'istanza [**\_ SettingData CIM**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="17e85-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="17e85-136">**Punto** (0)</span><span class="sxs-lookup"><span data-stu-id="17e85-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="17e85-137">**Minime** (1)</span><span class="sxs-lookup"><span data-stu-id="17e85-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="17e85-138">**Valori massimi** (2)</span><span class="sxs-lookup"><span data-stu-id="17e85-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="17e85-139">**Incrementi** (3)</span><span class="sxs-lookup"><span data-stu-id="17e85-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="17e85-140">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="17e85-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17e85-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="17e85-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17e85-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17e85-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17e85-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17e85-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17e85-144">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="17e85-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="17e85-145">Semantica aggiuntiva per l'interpretazione delle proprietà non null e non chiave dell'istanza di [**\_ SettingData CIM**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="17e85-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="17e85-146">"Default" indica che i valori delle proprietà dell'istanza di SettingData del componente verranno usati come valori predefiniti, quando viene creata una nuova istanza di SettingData per gli elementi le cui funzionalità sono definite dall'istanza delle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="17e85-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="17e85-147">Nelle istanze di SettingData, per determinate proprietà aventi lo stesso scopo semantico, è necessario specificare al massimo una tale istanza di SettingData come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="17e85-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="17e85-148">"Optimal" indica che l'istanza di SettingData rappresenta i valori delle impostazioni ottimali per gli elementi associati all'istanza delle funzionalità associate.</span><span class="sxs-lookup"><span data-stu-id="17e85-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="17e85-149">Più istanze di SettingData del componente possono essere dichiarate come ottimali. " Mean "indica che le proprietà numeriche non null, non chiave, non enumerate, non booleane dell'istanza di SettingData associata rappresentano un punto medio lungo una certa dimensione.</span><span class="sxs-lookup"><span data-stu-id="17e85-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="17e85-150">Per diverse combinazioni di proprietà SettingData, è possibile che più istanze di SettingData del componente siano dichiarate come "Mean".</span><span class="sxs-lookup"><span data-stu-id="17e85-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="17e85-151">"Supported" indica che le proprietà non null e non chiave dell'istanza di SettingData del componente rappresentano un set di valori di proprietà supportati che non sono altrimenti qualificati.</span><span class="sxs-lookup"><span data-stu-id="17e85-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="17e85-152">**Valore predefinito** (0)</span><span class="sxs-lookup"><span data-stu-id="17e85-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="17e85-153">**Ottimale** (1)</span><span class="sxs-lookup"><span data-stu-id="17e85-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="17e85-154">**Media** (2)</span><span class="sxs-lookup"><span data-stu-id="17e85-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="17e85-155">**Supportato** (3)</span><span class="sxs-lookup"><span data-stu-id="17e85-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="17e85-156">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="17e85-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="17e85-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="17e85-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="17e85-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17e85-158">Requirements</span></span>



| <span data-ttu-id="17e85-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e85-159">Requirement</span></span> | <span data-ttu-id="17e85-160">Valore</span><span class="sxs-lookup"><span data-stu-id="17e85-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e85-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17e85-161">Minimum supported client</span></span><br/> | <span data-ttu-id="17e85-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="17e85-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="17e85-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17e85-163">Minimum supported server</span></span><br/> | <span data-ttu-id="17e85-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17e85-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="17e85-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17e85-165">Namespace</span></span><br/>                | <span data-ttu-id="17e85-166">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="17e85-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="17e85-167">MOF</span><span class="sxs-lookup"><span data-stu-id="17e85-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17e85-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17e85-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17e85-169">DLL</span><span class="sxs-lookup"><span data-stu-id="17e85-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17e85-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17e85-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17e85-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17e85-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e85-172">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="17e85-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

