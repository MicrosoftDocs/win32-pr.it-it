---
description: La \_ classe CIM CardInSlot associa una scheda di adapter al contenitore in cui viene inserita.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: Classe CIM_CardInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878002"
---
# <a name="cim_cardinslot-class"></a><span data-ttu-id="61724-103">CIM \_ CardInSlot (classe)</span><span class="sxs-lookup"><span data-stu-id="61724-103">CIM\_CardInSlot class</span></span>

<span data-ttu-id="61724-104">La classe **CIM \_ CardInSlot** associa una scheda di adapter al contenitore in cui viene inserita.</span><span class="sxs-lookup"><span data-stu-id="61724-104">The **CIM\_CardInSlot** class associates an adapter card with the container into which it is inserted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61724-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="61724-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="61724-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="61724-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="61724-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="61724-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="61724-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="61724-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="61724-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61724-109">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="61724-110">Members</span><span class="sxs-lookup"><span data-stu-id="61724-110">Members</span></span>

<span data-ttu-id="61724-111">La classe **CIM \_ CardInSlot** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="61724-111">The **CIM\_CardInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="61724-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61724-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61724-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61724-113">Properties</span></span>

<span data-ttu-id="61724-114">La classe **CIM \_ CardInSlot** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="61724-114">The **CIM\_CardInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61724-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="61724-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61724-116">Tipo di dati **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="61724-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="61724-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61724-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61724-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="61724-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="61724-119">Uno [**\_ slot CIM**](cim-slot.md) che descrive lo slot in cui viene inserita la scheda.</span><span class="sxs-lookup"><span data-stu-id="61724-119">A [**CIM\_Slot**](cim-slot.md) that describes the slot into which the card is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="61724-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="61724-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61724-121">Tipo di dati **: \_ scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="61724-121">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="61724-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61724-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61724-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="61724-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="61724-124">Una [**\_ scheda CIM**](cim-card.md) che descrive la scheda nello slot.</span><span class="sxs-lookup"><span data-stu-id="61724-124">A [**CIM\_Card**](cim-card.md) that describes the card in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61724-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="61724-125">Remarks</span></span>

<span data-ttu-id="61724-126">La classe **CIM \_ CardInSlot** è derivata da [**CIM \_ PackageInSlot**](cim-packageinslot.md).</span><span class="sxs-lookup"><span data-stu-id="61724-126">The **CIM\_CardInSlot** class is derived from [**CIM\_PackageInSlot**](cim-packageinslot.md).</span></span>

<span data-ttu-id="61724-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="61724-127">WMI does not implement this class.</span></span>

<span data-ttu-id="61724-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="61724-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="61724-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="61724-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="61724-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61724-130">Requirements</span></span>



| <span data-ttu-id="61724-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="61724-131">Requirement</span></span> | <span data-ttu-id="61724-132">Valore</span><span class="sxs-lookup"><span data-stu-id="61724-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61724-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61724-133">Minimum supported client</span></span><br/> | <span data-ttu-id="61724-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61724-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61724-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61724-135">Minimum supported server</span></span><br/> | <span data-ttu-id="61724-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61724-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61724-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="61724-137">Namespace</span></span><br/>                | <span data-ttu-id="61724-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="61724-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="61724-139">MOF</span><span class="sxs-lookup"><span data-stu-id="61724-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61724-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61724-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="61724-141">DLL</span><span class="sxs-lookup"><span data-stu-id="61724-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61724-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61724-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61724-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61724-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61724-144">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="61724-144">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> </dl>

 

