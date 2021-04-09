---
description: La \_ relazione CIM DependencyContext associa una \_ classe di dipendenza CIM a uno o più \_ oggetti di configurazione CIM. Le dipendenze di un sistema di computer, ad esempio, possono variare in base alla rete a cui è collegato il sistema.
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: Classe CIM_DependencyContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69319a4f4d228d484da62411060ae3fead90bb79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877914"
---
# <a name="cim_dependencycontext-class"></a><span data-ttu-id="0bab5-104">CIM \_ DependencyContext (classe)</span><span class="sxs-lookup"><span data-stu-id="0bab5-104">CIM\_DependencyContext class</span></span>

<span data-ttu-id="0bab5-105">La relazione **CIM \_ DependencyContext** associa una classe di [**\_ dipendenza CIM**](cim-dependency.md) a uno o più oggetti di [**\_ configurazione CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="0bab5-105">The **CIM\_DependencyContext** relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="0bab5-106">Le dipendenze di un sistema di computer, ad esempio, possono variare in base alla rete a cui è collegato il sistema.</span><span class="sxs-lookup"><span data-stu-id="0bab5-106">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bab5-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0bab5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0bab5-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0bab5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0bab5-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0bab5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0bab5-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0bab5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bab5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bab5-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a><span data-ttu-id="0bab5-112">Members</span><span class="sxs-lookup"><span data-stu-id="0bab5-112">Members</span></span>

<span data-ttu-id="0bab5-113">La classe **CIM \_ DependencyContext** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0bab5-113">The **CIM\_DependencyContext** class has these types of members:</span></span>

-   [<span data-ttu-id="0bab5-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bab5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bab5-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0bab5-115">Properties</span></span>

<span data-ttu-id="0bab5-116">La classe **CIM \_ DependencyContext** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0bab5-116">The **CIM\_DependencyContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bab5-117">**Contesto**</span><span class="sxs-lookup"><span data-stu-id="0bab5-117">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bab5-118">Tipo di dati **: \_ configurazione CIM**</span><span class="sxs-lookup"><span data-stu-id="0bab5-118">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="0bab5-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bab5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bab5-120">Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0bab5-120">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0bab5-121">Riferimento all'oggetto di configurazione che aggrega la dipendenza.</span><span class="sxs-lookup"><span data-stu-id="0bab5-121">Reference to the configuration object that aggregates the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="0bab5-122">**Dipendenza**</span><span class="sxs-lookup"><span data-stu-id="0bab5-122">**Dependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bab5-123">Tipo di dati **: \_ dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="0bab5-123">Data type: **CIM\_Dependency**</span></span>
</dt> <dt>

<span data-ttu-id="0bab5-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0bab5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bab5-125">Riferimento a una dipendenza aggregata.</span><span class="sxs-lookup"><span data-stu-id="0bab5-125">Reference to an aggregated dependency.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bab5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bab5-126">Remarks</span></span>

<span data-ttu-id="0bab5-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="0bab5-127">WMI does not implement this class.</span></span>

<span data-ttu-id="0bab5-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0bab5-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0bab5-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0bab5-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bab5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bab5-130">Requirements</span></span>



| <span data-ttu-id="0bab5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bab5-131">Requirement</span></span> | <span data-ttu-id="0bab5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0bab5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bab5-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bab5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0bab5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bab5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bab5-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bab5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0bab5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bab5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bab5-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0bab5-137">Namespace</span></span><br/>                | <span data-ttu-id="0bab5-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0bab5-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0bab5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0bab5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bab5-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bab5-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bab5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0bab5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bab5-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bab5-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

