---
description: La \_ classe WMI dell'associazione LoadOrderGroupServiceDependencies Win32 mette in relazione un servizio di base e un gruppo di ordini di carico da cui il servizio dipende per avviare l'esecuzione.
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroupServiceDependencies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127482"
---
# <a name="win32_loadordergroupservicedependencies-class"></a><span data-ttu-id="7e4aa-103">Win32 \_ LoadOrderGroupServiceDependencies (classe)</span><span class="sxs-lookup"><span data-stu-id="7e4aa-103">Win32\_LoadOrderGroupServiceDependencies class</span></span>

<span data-ttu-id="7e4aa-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LoadOrderGroupServiceDependencies Win32** mette in relazione un servizio di base e un gruppo di ordini di carico da cui il servizio dipende per avviare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7e4aa-104">The **Win32\_LoadOrderGroupServiceDependencies** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a base service and a load order group that the service depends on to start running.</span></span>

<span data-ttu-id="7e4aa-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7e4aa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7e4aa-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7e4aa-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e4aa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e4aa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7e4aa-108">Members</span><span class="sxs-lookup"><span data-stu-id="7e4aa-108">Members</span></span>

<span data-ttu-id="7e4aa-109">La classe **Win32 \_ LoadOrderGroupServiceDependencies** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7e4aa-109">The **Win32\_LoadOrderGroupServiceDependencies** class has these types of members:</span></span>

-   [<span data-ttu-id="7e4aa-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e4aa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e4aa-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e4aa-111">Properties</span></span>

<span data-ttu-id="7e4aa-112">La classe **Win32 \_ LoadOrderGroupServiceDependencies** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e4aa-112">The **Win32\_LoadOrderGroupServiceDependencies** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e4aa-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7e4aa-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e4aa-114">Tipo di dati: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="7e4aa-114">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="7e4aa-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e4aa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e4aa-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="7e4aa-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="7e4aa-117">Riferimento all'istanza di che rappresenta le proprietà del gruppo dell'ordine di caricamento che deve iniziare prima che il servizio di base dipendente di questa classe possa essere avviato.</span><span class="sxs-lookup"><span data-stu-id="7e4aa-117">Reference to the instance representing the properties of the load order group that must start before the dependent base service of this class can start.</span></span>

</dd> <dt>

<span data-ttu-id="7e4aa-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7e4aa-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e4aa-119">Tipo di dati: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="7e4aa-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="7e4aa-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e4aa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e4aa-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="7e4aa-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="7e4aa-122">Riferimento all'istanza di che rappresenta le proprietà del servizio di base che dipende dal gruppo dell'ordine di caricamento per avviare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7e4aa-122">Reference to the instance representing the properties of the base service that is dependent upon the load order group to start running.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e4aa-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e4aa-123">Remarks</span></span>

<span data-ttu-id="7e4aa-124">La classe **Win32 \_ LoadOrderGroupServiceDependencies** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7e4aa-124">The **Win32\_LoadOrderGroupServiceDependencies** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e4aa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e4aa-125">Requirements</span></span>



| <span data-ttu-id="7e4aa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e4aa-126">Requirement</span></span> | <span data-ttu-id="7e4aa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7e4aa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e4aa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e4aa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e4aa-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e4aa-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e4aa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e4aa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e4aa-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e4aa-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e4aa-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e4aa-132">Namespace</span></span><br/>                | <span data-ttu-id="7e4aa-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7e4aa-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e4aa-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7e4aa-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e4aa-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e4aa-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e4aa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7e4aa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e4aa-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e4aa-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e4aa-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e4aa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e4aa-139">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="7e4aa-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="7e4aa-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e4aa-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

