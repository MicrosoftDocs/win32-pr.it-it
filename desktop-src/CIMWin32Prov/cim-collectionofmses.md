---
description: L' \_ oggetto CIM CollectionOfMSEs consente il raggruppamento di oggetti CIM \_ ManagedSystemElement allo scopo di associare le impostazioni e le configurazioni. È astratto per richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfMSEs (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127110"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="a97a7-104">Classe CIM_CollectionOfMSEs (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a97a7-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a97a7-105">L'oggetto **CIM \_ CollectionOfMSEs** consente il raggruppamento di oggetti [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) allo scopo di associare le impostazioni e le configurazioni.</span><span class="sxs-lookup"><span data-stu-id="a97a7-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="a97a7-106">È astratto per richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a97a7-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="a97a7-107">L' **oggetto \_ CollectionOfMSEs CIM** non porta informazioni sullo stato o sullo stato, ma rappresenta solo un raggruppamento di elementi.</span><span class="sxs-lookup"><span data-stu-id="a97a7-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="a97a7-108">Per questo motivo, non è corretto per i gruppi di sottoclassi con stato/stato da **CIM \_ CollectionOfMSEs**, ad esempio [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (che è correttamente sottoclassato da [**CIM \_ LogicalElement**](cim-logicalelement.md)).</span><span class="sxs-lookup"><span data-stu-id="a97a7-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="a97a7-109">Le raccolte in genere aggregano gli oggetti ' like ' e rappresentano un'ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a97a7-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="a97a7-110">Senza raccolte, è necessario definire singole associazioni CIM [**\_ ElementSetting**](cim-elementsetting.md) e [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) per collegare le impostazioni e gli oggetti di configurazione a singoli [**CIM \_ ManagedSystemElements**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a97a7-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="a97a7-111">È possibile che si verifichino molte duplicazioni nell'assegnazione della stessa impostazione a più oggetti.</span><span class="sxs-lookup"><span data-stu-id="a97a7-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="a97a7-112">Inoltre, l'utilizzo dell'oggetto Collection consente di determinare che l'impostazione e le associazioni di configurazione sono effettivamente le stesse per i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a97a7-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="a97a7-113">Queste informazioni verrebbero altrimenti ottenute definendo la raccolta in modo proprietario, quindi eseguendo una query sulle associazioni **CIM \_ ElementSetting** e **CIM \_ ElementConfiguration** per determinare se il set di raccolta è completamente coperto.</span><span class="sxs-lookup"><span data-stu-id="a97a7-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a97a7-114">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a97a7-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a97a7-115">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a97a7-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a97a7-116">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a97a7-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a97a7-117">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a97a7-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97a7-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a97a7-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="a97a7-119">Members</span><span class="sxs-lookup"><span data-stu-id="a97a7-119">Members</span></span>

<span data-ttu-id="a97a7-120">La classe **CIM \_ CollectionOfMSEs** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a97a7-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="a97a7-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a97a7-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a97a7-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a97a7-122">Properties</span></span>

<span data-ttu-id="a97a7-123">La classe **CIM \_ CollectionOfMSEs** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a97a7-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a97a7-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a97a7-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a97a7-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a97a7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a97a7-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a97a7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a97a7-127">Breve descrizione testuale dell'oggetto CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="a97a7-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="a97a7-128">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="a97a7-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a97a7-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a97a7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a97a7-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a97a7-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a97a7-131">Identificazione dell'oggetto raccolta.</span><span class="sxs-lookup"><span data-stu-id="a97a7-131">Identification of the Collection object.</span></span> <span data-ttu-id="a97a7-132">Quando è sottoclassata, è possibile eseguire l'override della proprietà CollectionID in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a97a7-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="a97a7-133">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a97a7-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a97a7-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a97a7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a97a7-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a97a7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a97a7-136">Descrizione testuale dell'oggetto CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="a97a7-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a97a7-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="a97a7-137">Remarks</span></span>

<span data-ttu-id="a97a7-138">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a97a7-138">WMI does not implement this class.</span></span> <span data-ttu-id="a97a7-139">Vedere [le classi Win32](win32-provider.md) per le classi WMI derivate da **CIM \_ CollectionOfMSEs**.</span><span class="sxs-lookup"><span data-stu-id="a97a7-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="a97a7-140">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a97a7-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a97a7-141">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a97a7-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97a7-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a97a7-142">Requirements</span></span>



| <span data-ttu-id="a97a7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a97a7-143">Requirement</span></span> | <span data-ttu-id="a97a7-144">Valore</span><span class="sxs-lookup"><span data-stu-id="a97a7-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a97a7-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a97a7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a97a7-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a97a7-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a97a7-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a97a7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a97a7-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a97a7-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a97a7-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a97a7-149">Namespace</span></span><br/>                | <span data-ttu-id="a97a7-150">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a97a7-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a97a7-151">MOF</span><span class="sxs-lookup"><span data-stu-id="a97a7-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a97a7-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a97a7-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a97a7-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a97a7-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a97a7-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a97a7-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




