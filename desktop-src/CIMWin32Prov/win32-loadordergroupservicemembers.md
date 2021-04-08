---
description: La \_ classe WMI dell'associazione LoadOrderGroupServiceMembers Win32 mette in correlazione un gruppo di ordini di carico e un servizio di base.
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceMembers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878294"
---
# <a name="win32_loadordergroupservicemembers-class"></a><span data-ttu-id="8c7cf-103">Win32 \_ LoadOrderGroupServiceMembers (classe)</span><span class="sxs-lookup"><span data-stu-id="8c7cf-103">Win32\_LoadOrderGroupServiceMembers class</span></span>

<span data-ttu-id="8c7cf-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LoadOrderGroupServiceMembers Win32** mette in correlazione un gruppo di ordini di carico e un servizio di base.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-104">The **Win32\_LoadOrderGroupServiceMembers** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a load order group and a base service.</span></span>

> [!Note]  
> <span data-ttu-id="8c7cf-105">[**Win32 \_**](win32-systemdriver.md) Gli oggetti SystemDriver sono membri del gruppo di ordini di caricamento.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-105">[**Win32\_SystemDriver**](win32-systemdriver.md) objects are members of that load order group.</span></span> <span data-ttu-id="8c7cf-106">Non tutti i servizi sono membri dei gruppi e non tutti i gruppi dispongono di servizi al loro interno.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-106">Not all services are members of groups, and not all groups have services within them.</span></span>

 

<span data-ttu-id="8c7cf-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8c7cf-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c7cf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c7cf-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8c7cf-110">Members</span><span class="sxs-lookup"><span data-stu-id="8c7cf-110">Members</span></span>

<span data-ttu-id="8c7cf-111">La classe **Win32 \_ LoadOrderGroupServiceMembers** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8c7cf-111">The **Win32\_LoadOrderGroupServiceMembers** class has these types of members:</span></span>

-   [<span data-ttu-id="8c7cf-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c7cf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c7cf-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c7cf-113">Properties</span></span>

<span data-ttu-id="8c7cf-114">La classe **Win32 \_ LoadOrderGroupServiceMembers** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-114">The **Win32\_LoadOrderGroupServiceMembers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c7cf-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8c7cf-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c7cf-116">Tipo di dati: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="8c7cf-116">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="8c7cf-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c7cf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c7cf-118">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="8c7cf-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="8c7cf-119">Riferimento all'istanza che rappresenta le proprietà del gruppo dell'ordine di caricamento associate al servizio di base.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-119">Reference to the instance representing the load order group properties associated with the base service.</span></span>

</dd> <dt>

<span data-ttu-id="8c7cf-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8c7cf-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c7cf-121">Tipo di dati: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="8c7cf-121">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="8c7cf-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c7cf-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c7cf-123">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="8c7cf-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="8c7cf-124">Riferimento all'istanza di che rappresenta il servizio membro di un gruppo di ordine di caricamento.</span><span class="sxs-lookup"><span data-stu-id="8c7cf-124">Reference to the instance representing the service that is a member of a load order group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c7cf-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c7cf-125">Remarks</span></span>

<span data-ttu-id="8c7cf-126">La classe **Win32 \_ LoadOrderGroupServiceMembers** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="8c7cf-126">The **Win32\_LoadOrderGroupServiceMembers** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c7cf-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c7cf-127">Requirements</span></span>



| <span data-ttu-id="8c7cf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c7cf-128">Requirement</span></span> | <span data-ttu-id="8c7cf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8c7cf-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7cf-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c7cf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8c7cf-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c7cf-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c7cf-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c7cf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8c7cf-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c7cf-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c7cf-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c7cf-134">Namespace</span></span><br/>                | <span data-ttu-id="8c7cf-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8c7cf-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c7cf-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8c7cf-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c7cf-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c7cf-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c7cf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8c7cf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c7cf-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c7cf-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c7cf-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c7cf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7cf-141">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="8c7cf-141">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="8c7cf-142">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c7cf-142">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

