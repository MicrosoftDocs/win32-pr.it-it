---
description: La \_ classe CIM ConnectedTo rappresenta un'associazione che indica che due o più connettori fisici sono connessi.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: Classe CIM_ConnectedTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049218"
---
# <a name="cim_connectedto-class"></a><span data-ttu-id="e00e5-103">CIM \_ ConnectedTo (classe)</span><span class="sxs-lookup"><span data-stu-id="e00e5-103">CIM\_ConnectedTo class</span></span>

<span data-ttu-id="e00e5-104">La classe **CIM \_ ConnectedTo** rappresenta un'associazione che indica che due o più connettori fisici sono connessi.</span><span class="sxs-lookup"><span data-stu-id="e00e5-104">The **CIM\_ConnectedTo** class represents an association that indicates that two or more physical connectors are connected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e00e5-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e00e5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e00e5-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e00e5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e00e5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e00e5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e00e5-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e00e5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e00e5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e00e5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e00e5-110">Members</span><span class="sxs-lookup"><span data-stu-id="e00e5-110">Members</span></span>

<span data-ttu-id="e00e5-111">La classe **CIM \_ ConnectedTo** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e00e5-111">The **CIM\_ConnectedTo** class has these types of members:</span></span>

-   [<span data-ttu-id="e00e5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e00e5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e00e5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e00e5-113">Properties</span></span>

<span data-ttu-id="e00e5-114">La classe **CIM \_ ConnectedTo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e00e5-114">The **CIM\_ConnectedTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e00e5-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e00e5-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e00e5-116">Tipo di dati: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="e00e5-116">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="e00e5-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e00e5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e00e5-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="e00e5-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e00e5-119">Un [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) che rappresenta un connettore fisico che funge da un'estremità della connessione.</span><span class="sxs-lookup"><span data-stu-id="e00e5-119">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents a physical connector that serves as one end of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e00e5-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="e00e5-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e00e5-121">Tipo di dati: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="e00e5-121">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="e00e5-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e00e5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e00e5-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="e00e5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e00e5-124">Un [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) che rappresenta un altro connettore fisico che funge da altra estremità della connessione.</span><span class="sxs-lookup"><span data-stu-id="e00e5-124">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that represents another physical connector that serves as the other end of the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e00e5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e00e5-125">Remarks</span></span>

<span data-ttu-id="e00e5-126">La classe **CIM \_ ConnectedTo** viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e00e5-126">The **CIM\_ConnectedTo** class is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e00e5-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="e00e5-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e00e5-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e00e5-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e00e5-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e00e5-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00e5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e00e5-130">Requirements</span></span>



| <span data-ttu-id="e00e5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00e5-131">Requirement</span></span> | <span data-ttu-id="e00e5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e00e5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e00e5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e00e5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e00e5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e00e5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e00e5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e00e5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e00e5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e00e5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e00e5-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e00e5-137">Namespace</span></span><br/>                | <span data-ttu-id="e00e5-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e00e5-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e00e5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e00e5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e00e5-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e00e5-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e00e5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e00e5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e00e5-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e00e5-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00e5-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e00e5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00e5-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="e00e5-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

