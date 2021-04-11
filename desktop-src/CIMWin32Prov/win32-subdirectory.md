---
description: La \_ classe WMI associazione sottodirectory Win32 mette in relazione una directory (cartella) e una delle rispettive sottodirectory (sottocartelle).
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Classe Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127315"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="fe49f-103">\_Classe della sottodirectory Win32</span><span class="sxs-lookup"><span data-stu-id="fe49f-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="fe49f-104">La [classe WMI](../wmisdk/retrieving-a-class.md) associazione **\_ sottodirectory Win32** mette in relazione una directory (cartella) e una delle rispettive sottodirectory (sottocartelle).</span><span class="sxs-lookup"><span data-stu-id="fe49f-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="fe49f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fe49f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fe49f-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fe49f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe49f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe49f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="fe49f-108">Members</span><span class="sxs-lookup"><span data-stu-id="fe49f-108">Members</span></span>

<span data-ttu-id="fe49f-109">La classe della **\_ sottodirectory Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fe49f-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="fe49f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe49f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe49f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe49f-111">Properties</span></span>

<span data-ttu-id="fe49f-112">La classe della **\_ sottodirectory Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe49f-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe49f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fe49f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe49f-114">Tipo di dati **: \_ directory Win32**</span><span class="sxs-lookup"><span data-stu-id="fe49f-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="fe49f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe49f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe49f-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directory Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="fe49f-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="fe49f-117">Riferimento all'istanza di che rappresenta le proprietà della directory padre (cartella) in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="fe49f-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="fe49f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fe49f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe49f-119">Tipo di dati **: \_ directory Win32**</span><span class="sxs-lookup"><span data-stu-id="fe49f-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="fe49f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fe49f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe49f-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| directory Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="fe49f-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="fe49f-122">Riferimento all'istanza che rappresenta la parte della sottodirectory (sottocartella) dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="fe49f-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe49f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe49f-123">Remarks</span></span>

<span data-ttu-id="fe49f-124">La classe della **\_ sottodirectory Win32** è derivata [**dal \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="fe49f-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="fe49f-125">Per restituire una raccolta di sottocartelle per una cartella, creare una query di associazione che imposta *RESULTROLE* su *PartComponent*.</span><span class="sxs-lookup"><span data-stu-id="fe49f-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="fe49f-126">Ciò indica che tutti gli elementi nella raccolta restituita devono svolgere il ruolo di PartComponent, o sottocartella, dell'oggetto cartella.</span><span class="sxs-lookup"><span data-stu-id="fe49f-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="fe49f-127">Per restituire la cartella padre per una cartella, impostare *RESULTROLE* su *GroupComponent*.</span><span class="sxs-lookup"><span data-stu-id="fe49f-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="fe49f-128">La classe della **\_ sottodirectory Win32** funziona solo a livello di file System immediatamente sopra o immediatamente sotto la cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="fe49f-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="fe49f-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe49f-129">Examples</span></span>

<span data-ttu-id="fe49f-130">Nell'esempio VBScript seguente viene restituito un elenco di tutte le sottocartelle all'interno della cartella C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="fe49f-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="fe49f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe49f-131">Requirements</span></span>



| <span data-ttu-id="fe49f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe49f-132">Requirement</span></span> | <span data-ttu-id="fe49f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="fe49f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe49f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe49f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fe49f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe49f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe49f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe49f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fe49f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe49f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe49f-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe49f-138">Namespace</span></span><br/>                | <span data-ttu-id="fe49f-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fe49f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fe49f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fe49f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe49f-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe49f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe49f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fe49f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe49f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe49f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe49f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe49f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe49f-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="fe49f-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="fe49f-146">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fe49f-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
