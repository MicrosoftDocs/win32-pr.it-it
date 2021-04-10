---
description: La \_ classe CIM ProcessThread rappresenta un collegamento tra un processo e i thread in esecuzione nel contesto del processo.
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: Classe CIM_ProcessThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: afc29d1576355eda1f9e3dfd7ed55d2cca399d5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225575"
---
# <a name="cim_processthread-class"></a><span data-ttu-id="971e5-103">CIM \_ ProcessThread (classe)</span><span class="sxs-lookup"><span data-stu-id="971e5-103">CIM\_ProcessThread class</span></span>

<span data-ttu-id="971e5-104">La classe **CIM \_ ProcessThread** rappresenta un collegamento tra un processo e i thread in esecuzione nel contesto del processo.</span><span class="sxs-lookup"><span data-stu-id="971e5-104">The **CIM\_ProcessThread** class represents a link between a process and the threads running in the context of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="971e5-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="971e5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="971e5-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="971e5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="971e5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="971e5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="971e5-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="971e5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="971e5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="971e5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="971e5-110">Members</span><span class="sxs-lookup"><span data-stu-id="971e5-110">Members</span></span>

<span data-ttu-id="971e5-111">La classe **CIM \_ ProcessThread** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="971e5-111">The **CIM\_ProcessThread** class has these types of members:</span></span>

-   [<span data-ttu-id="971e5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="971e5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="971e5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="971e5-113">Properties</span></span>

<span data-ttu-id="971e5-114">La classe **CIM \_ ProcessThread** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="971e5-114">The **CIM\_ProcessThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="971e5-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="971e5-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971e5-116">Tipo di dati **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="971e5-116">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="971e5-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="971e5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="971e5-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="971e5-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="971e5-119">Un [**\_ processo CIM**](cim-process.md) che descrive il processo.</span><span class="sxs-lookup"><span data-stu-id="971e5-119">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="971e5-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="971e5-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971e5-121">Tipo di dati **: \_ thread CIM**</span><span class="sxs-lookup"><span data-stu-id="971e5-121">Data type: **CIM\_Thread**</span></span>
</dt> <dt>

<span data-ttu-id="971e5-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="971e5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="971e5-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="971e5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="971e5-124">[**\_ Thread CIM**](cim-thread.md) che descrive il thread in esecuzione nel contesto del processo.</span><span class="sxs-lookup"><span data-stu-id="971e5-124">A [**CIM\_Thread**](cim-thread.md) that describes the thread running in the context of the process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="971e5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="971e5-125">Remarks</span></span>

<span data-ttu-id="971e5-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="971e5-126">WMI does not implement this class.</span></span>

<span data-ttu-id="971e5-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="971e5-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="971e5-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="971e5-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="971e5-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="971e5-129">Requirements</span></span>



| <span data-ttu-id="971e5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="971e5-130">Requirement</span></span> | <span data-ttu-id="971e5-131">Valore</span><span class="sxs-lookup"><span data-stu-id="971e5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="971e5-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="971e5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="971e5-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="971e5-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="971e5-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="971e5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="971e5-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="971e5-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="971e5-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="971e5-136">Namespace</span></span><br/>                | <span data-ttu-id="971e5-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="971e5-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="971e5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="971e5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="971e5-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="971e5-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="971e5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="971e5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="971e5-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="971e5-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="971e5-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="971e5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971e5-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="971e5-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

