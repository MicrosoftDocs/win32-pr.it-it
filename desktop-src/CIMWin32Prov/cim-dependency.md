---
description: La \_ classe di dipendenza CIM rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: Classe CIM_Dependency (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748498"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="1c982-103">Classe CIM_Dependency (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1c982-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1c982-104">La classe di **\_ dipendenza CIM** rappresenta un'associazione che stabilisce relazioni di dipendenza tra oggetti.</span><span class="sxs-lookup"><span data-stu-id="1c982-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c982-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1c982-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1c982-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1c982-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1c982-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1c982-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1c982-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1c982-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c982-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c982-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1c982-110">Members</span><span class="sxs-lookup"><span data-stu-id="1c982-110">Members</span></span>

<span data-ttu-id="1c982-111">La classe di **\_ dipendenza CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c982-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="1c982-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c982-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c982-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1c982-113">Properties</span></span>

<span data-ttu-id="1c982-114">La classe di **\_ dipendenza CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c982-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c982-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1c982-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c982-116">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="1c982-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1c982-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c982-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c982-118">Riferimento all'oggetto indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="1c982-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="1c982-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="1c982-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c982-120">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="1c982-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1c982-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1c982-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c982-122">Riferimento all'oggetto che dipende dalla proprietà **precedente** .</span><span class="sxs-lookup"><span data-stu-id="1c982-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c982-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c982-123">Remarks</span></span>

<span data-ttu-id="1c982-124">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="1c982-124">WMI does not implement this class.</span></span> <span data-ttu-id="1c982-125">Per ulteriori informazioni sulle classi derivate dalla **\_ dipendenza CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1c982-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1c982-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1c982-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1c982-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1c982-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c982-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c982-128">Requirements</span></span>



| <span data-ttu-id="1c982-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c982-129">Requirement</span></span> | <span data-ttu-id="1c982-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1c982-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c982-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c982-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1c982-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c982-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c982-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c982-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1c982-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c982-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c982-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c982-135">Namespace</span></span><br/>                | <span data-ttu-id="1c982-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1c982-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c982-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1c982-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c982-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c982-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c982-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1c982-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c982-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c982-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




