---
description: La \_ classe WMI dell'associazione LogicalProgramGroupDirectory Win32 mette in relazione i gruppi di programmi logici (raggruppamenti nel menu Start) e le directory dei file in cui sono archiviati.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304472"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a><span data-ttu-id="6d9e1-103">Win32 \_ LogicalProgramGroupDirectory (classe)</span><span class="sxs-lookup"><span data-stu-id="6d9e1-103">Win32\_LogicalProgramGroupDirectory class</span></span>

<span data-ttu-id="6d9e1-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LogicalProgramGroupDirectory Win32** mette in relazione i gruppi di programmi logici (raggruppamenti nel menu **Start** ) e le directory dei file in cui sono archiviati.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-104">The **Win32\_LogicalProgramGroupDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical program groups (groupings in the **Start** menu) and the file directories in which they are stored.</span></span>

<span data-ttu-id="6d9e1-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6d9e1-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d9e1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6d9e1-108">Members</span><span class="sxs-lookup"><span data-stu-id="6d9e1-108">Members</span></span>

<span data-ttu-id="6d9e1-109">La classe **Win32 \_ LogicalProgramGroupDirectory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6d9e1-109">The **Win32\_LogicalProgramGroupDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="6d9e1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d9e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d9e1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d9e1-111">Properties</span></span>

<span data-ttu-id="6d9e1-112">La classe **Win32 \_ LogicalProgramGroupDirectory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-112">The **Win32\_LogicalProgramGroupDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d9e1-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6d9e1-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9e1-114">Tipo di dati: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="6d9e1-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="6d9e1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d9e1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9e1-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="6d9e1-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="6d9e1-117">Riferimento all'istanza che rappresenta il gruppo di programmi logici.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-117">Reference to the instance representing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="6d9e1-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="6d9e1-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d9e1-119">Tipo di dati **: \_ directory Win32**</span><span class="sxs-lookup"><span data-stu-id="6d9e1-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="6d9e1-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d9e1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d9e1-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| directory Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="6d9e1-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="6d9e1-122">Riferimento all'istanza di che rappresenta la directory di file per il gruppo di programmi logici.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-122">Reference to the instance representing the file directory for the logical program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d9e1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d9e1-123">Remarks</span></span>

<span data-ttu-id="6d9e1-124">La classe **Win32 \_ LogicalProgramGroupDirectory** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6d9e1-124">The **Win32\_LogicalProgramGroupDirectory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="6d9e1-125">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="6d9e1-126">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="6d9e1-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="6d9e1-127">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="6d9e1-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9e1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d9e1-128">Requirements</span></span>



| <span data-ttu-id="6d9e1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9e1-129">Requirement</span></span> | <span data-ttu-id="6d9e1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6d9e1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9e1-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d9e1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9e1-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d9e1-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d9e1-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d9e1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9e1-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d9e1-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d9e1-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d9e1-135">Namespace</span></span><br/>                | <span data-ttu-id="6d9e1-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6d9e1-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6d9e1-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6d9e1-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d9e1-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d9e1-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d9e1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6d9e1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9e1-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9e1-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9e1-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d9e1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9e1-142">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="6d9e1-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="6d9e1-143">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d9e1-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

