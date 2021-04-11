---
description: La \_ classe WMI dell'associazione LogicalProgramGroupItemDataFile Win32 mette in relazione gli elementi del gruppo di programmi del menu Start e i file in cui sono archiviati.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItemDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127718"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="5faa0-103">Win32 \_ LogicalProgramGroupItemDataFile (classe)</span><span class="sxs-lookup"><span data-stu-id="5faa0-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="5faa0-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ LogicalProgramGroupItemDataFile Win32** mette in relazione gli elementi del gruppo di programmi del menu **Start** e i file in cui sono archiviati.</span><span class="sxs-lookup"><span data-stu-id="5faa0-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="5faa0-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5faa0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5faa0-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5faa0-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5faa0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5faa0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5faa0-108">Members</span><span class="sxs-lookup"><span data-stu-id="5faa0-108">Members</span></span>

<span data-ttu-id="5faa0-109">La classe **Win32 \_ LogicalProgramGroupItemDataFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5faa0-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="5faa0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5faa0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5faa0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5faa0-111">Properties</span></span>

<span data-ttu-id="5faa0-112">La classe **Win32 \_ LogicalProgramGroupItemDataFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5faa0-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5faa0-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5faa0-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5faa0-114">Tipo di dati: **Win32 \_ LogicalProgramGroupItem**</span><span class="sxs-lookup"><span data-stu-id="5faa0-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="5faa0-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5faa0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5faa0-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 LogicalProgramGroupItem")</span><span class="sxs-lookup"><span data-stu-id="5faa0-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="5faa0-117">Riferimento all'istanza che rappresenta i raggruppamenti di programmi nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="5faa0-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="5faa0-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5faa0-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5faa0-119">Tipo di dati **: \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="5faa0-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="5faa0-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5faa0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5faa0-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| DataFile CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="5faa0-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="5faa0-122">Riferimento all'istanza di che rappresenta la classe associata al gruppo di programmi.</span><span class="sxs-lookup"><span data-stu-id="5faa0-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5faa0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5faa0-123">Remarks</span></span>

<span data-ttu-id="5faa0-124">La classe **Win32 \_ LogicalProgramGroupItemDataFile** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5faa0-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5faa0-125">Il processo chiamante che usa questa classe deve avere il privilegio **se \_ Restore \_ Name** nel computer in cui risiede il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5faa0-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="5faa0-126">Se ad esempio si enumera questa classe nel computer locale, l'account con cui viene eseguita l'applicazione deve disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="5faa0-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="5faa0-127">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="5faa0-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="5faa0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5faa0-128">Requirements</span></span>



| <span data-ttu-id="5faa0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5faa0-129">Requirement</span></span> | <span data-ttu-id="5faa0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5faa0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5faa0-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5faa0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5faa0-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5faa0-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5faa0-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5faa0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5faa0-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5faa0-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5faa0-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5faa0-135">Namespace</span></span><br/>                | <span data-ttu-id="5faa0-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5faa0-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5faa0-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5faa0-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5faa0-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5faa0-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5faa0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5faa0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5faa0-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5faa0-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5faa0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5faa0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5faa0-142">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5faa0-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="5faa0-143">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5faa0-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

