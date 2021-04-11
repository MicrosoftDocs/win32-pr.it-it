---
description: La \_ classe del percorso CIM rappresenta la posizione e l'indirizzo di un elemento fisico.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: Classe CIM_Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225677"
---
# <a name="cim_location-class"></a><span data-ttu-id="f66ea-103">\_Classe location CIM</span><span class="sxs-lookup"><span data-stu-id="f66ea-103">CIM\_Location class</span></span>

<span data-ttu-id="f66ea-104">La classe del **\_ percorso CIM** rappresenta la posizione e l'indirizzo di un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f66ea-104">The **CIM\_Location** class represents the position and address of a physical element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f66ea-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f66ea-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f66ea-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f66ea-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f66ea-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f66ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f66ea-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f66ea-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f66ea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f66ea-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a><span data-ttu-id="f66ea-110">Members</span><span class="sxs-lookup"><span data-stu-id="f66ea-110">Members</span></span>

<span data-ttu-id="f66ea-111">La classe del **\_ percorso CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f66ea-111">The **CIM\_Location** class has these types of members:</span></span>

-   [<span data-ttu-id="f66ea-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f66ea-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f66ea-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f66ea-113">Properties</span></span>

<span data-ttu-id="f66ea-114">La classe del **\_ percorso CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f66ea-114">The **CIM\_Location** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f66ea-115">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="f66ea-115">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f66ea-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f66ea-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f66ea-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f66ea-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f66ea-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="f66ea-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="f66ea-119">Stringa in formato libero che indica una strada o un altro tipo di indirizzo per la posizione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f66ea-119">Free-form string that indicates a street or other type of address for the physical element's location.</span></span>

</dd> <dt>

<span data-ttu-id="f66ea-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f66ea-120">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f66ea-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f66ea-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f66ea-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f66ea-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f66ea-123">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f66ea-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f66ea-124">Stringa in formato libero che definisce un'etichetta per la posizione ed è parte della chiave per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f66ea-124">Free-form string that defines a label for the location and is part of the key for the object.</span></span>

</dd> <dt>

<span data-ttu-id="f66ea-125">**PhysicalPosition**</span><span class="sxs-lookup"><span data-stu-id="f66ea-125">**PhysicalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f66ea-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f66ea-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f66ea-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f66ea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f66ea-128">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f66ea-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f66ea-129">Stringa in formato libero che indica la posizione di un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="f66ea-129">Free-form string that indicates the placement of a physical element.</span></span> <span data-ttu-id="f66ea-130">Può specificare informazioni sugli slot in una bacheca di hosting, montare il sito in un file CAB o informazioni sulla latitudine e la longitudine.</span><span class="sxs-lookup"><span data-stu-id="f66ea-130">It can specify slot information on a hosting board, mounting site in a cabinet, or latitude and longitude information.</span></span> <span data-ttu-id="f66ea-131">Fa parte della chiave dell'oggetto **\_ percorso CIM** .</span><span class="sxs-lookup"><span data-stu-id="f66ea-131">It is part of the key of the **CIM\_Location** object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f66ea-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f66ea-132">Remarks</span></span>

<span data-ttu-id="f66ea-133">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f66ea-133">WMI does not implement this class.</span></span> <span data-ttu-id="f66ea-134">Per le classi derivate dalla **\_ posizione CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f66ea-134">For classes derived from **CIM\_Location**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f66ea-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f66ea-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f66ea-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f66ea-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f66ea-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f66ea-137">Requirements</span></span>



| <span data-ttu-id="f66ea-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f66ea-138">Requirement</span></span> | <span data-ttu-id="f66ea-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f66ea-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f66ea-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f66ea-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f66ea-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f66ea-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f66ea-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f66ea-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f66ea-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f66ea-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f66ea-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f66ea-144">Namespace</span></span><br/>                | <span data-ttu-id="f66ea-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f66ea-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f66ea-146">MOF</span><span class="sxs-lookup"><span data-stu-id="f66ea-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f66ea-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f66ea-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f66ea-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f66ea-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f66ea-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f66ea-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

