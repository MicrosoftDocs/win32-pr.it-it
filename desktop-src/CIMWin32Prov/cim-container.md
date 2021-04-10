---
description: La \_ classe contenitore CIM rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore. Un oggetto contenitore deve essere un pacchetto fisico.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: Classe CIM_Container
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966199"
---
# <a name="cim_container-class"></a><span data-ttu-id="10a14-104">\_Classe contenitore CIM</span><span class="sxs-lookup"><span data-stu-id="10a14-104">CIM\_Container class</span></span>

<span data-ttu-id="10a14-105">La **classe \_ contenitore CIM** rappresenta un'associazione tra un elemento contenuto e un elemento fisico contenitore.</span><span class="sxs-lookup"><span data-stu-id="10a14-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="10a14-106">Un oggetto contenitore deve essere un pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="10a14-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10a14-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="10a14-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10a14-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="10a14-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10a14-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="10a14-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="10a14-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="10a14-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a14-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10a14-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="10a14-112">Members</span><span class="sxs-lookup"><span data-stu-id="10a14-112">Members</span></span>

<span data-ttu-id="10a14-113">La **classe \_ contenitore CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="10a14-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="10a14-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10a14-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10a14-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10a14-115">Properties</span></span>

<span data-ttu-id="10a14-116">La **classe \_ contenitore CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="10a14-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10a14-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="10a14-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a14-118">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="10a14-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="10a14-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10a14-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a14-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="10a14-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="10a14-121">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che rappresenta il pacchetto fisico che contiene altri elementi fisici, inclusi gli altri pacchetti.</span><span class="sxs-lookup"><span data-stu-id="10a14-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="10a14-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="10a14-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a14-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="10a14-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10a14-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10a14-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10a14-125">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="10a14-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="10a14-126">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="10a14-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="10a14-127">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="10a14-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="10a14-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="10a14-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10a14-129">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="10a14-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="10a14-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="10a14-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10a14-131">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="10a14-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="10a14-132">Oggetto [**\_ fisico CIM**](cim-physicalelement.md) che descrive l'elemento fisico che è contenuto nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="10a14-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10a14-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="10a14-133">Remarks</span></span>

<span data-ttu-id="10a14-134">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="10a14-134">WMI does not implement this class.</span></span> <span data-ttu-id="10a14-135">Per ulteriori informazioni sulle classi derivate dal **\_ contenitore CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="10a14-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="10a14-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="10a14-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="10a14-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="10a14-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a14-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10a14-138">Requirements</span></span>



| <span data-ttu-id="10a14-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="10a14-139">Requirement</span></span> | <span data-ttu-id="10a14-140">Valore</span><span class="sxs-lookup"><span data-stu-id="10a14-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10a14-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10a14-141">Minimum supported client</span></span><br/> | <span data-ttu-id="10a14-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10a14-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10a14-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10a14-143">Minimum supported server</span></span><br/> | <span data-ttu-id="10a14-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10a14-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10a14-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10a14-145">Namespace</span></span><br/>                | <span data-ttu-id="10a14-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="10a14-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10a14-147">MOF</span><span class="sxs-lookup"><span data-stu-id="10a14-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10a14-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10a14-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10a14-149">DLL</span><span class="sxs-lookup"><span data-stu-id="10a14-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10a14-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10a14-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10a14-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10a14-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10a14-152">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="10a14-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

