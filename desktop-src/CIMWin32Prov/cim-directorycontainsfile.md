---
description: La \_ classe CIM DirectoryContainsFile rappresenta un'associazione tra una directory e i file contenuti all'interno di tale directory.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: Classe CIM_DirectoryContainsFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878046"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="2199b-103">CIM \_ DirectoryContainsFile (classe)</span><span class="sxs-lookup"><span data-stu-id="2199b-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="2199b-104">La classe **CIM \_ DirectoryContainsFile** rappresenta un'associazione tra una directory e i file contenuti all'interno di tale directory.</span><span class="sxs-lookup"><span data-stu-id="2199b-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2199b-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2199b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2199b-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2199b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2199b-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2199b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2199b-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2199b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2199b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2199b-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="2199b-110">Members</span><span class="sxs-lookup"><span data-stu-id="2199b-110">Members</span></span>

<span data-ttu-id="2199b-111">La classe **CIM \_ DirectoryContainsFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2199b-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="2199b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2199b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2199b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2199b-113">Properties</span></span>

<span data-ttu-id="2199b-114">La classe **CIM \_ DirectoryContainsFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2199b-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2199b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2199b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2199b-116">Tipo di dati **: \_ directory CIM**</span><span class="sxs-lookup"><span data-stu-id="2199b-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="2199b-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2199b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2199b-118">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2199b-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2199b-119">Una [**\_ directory CIM**](cim-directory.md) che descrive la directory.</span><span class="sxs-lookup"><span data-stu-id="2199b-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="2199b-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2199b-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2199b-121">Tipo di dati **: \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="2199b-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="2199b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2199b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2199b-123">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2199b-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2199b-124">Un file di [**\_ DataFile CIM**](cim-datafile.md) che descrive i LogicalFile contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="2199b-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2199b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="2199b-125">Remarks</span></span>

<span data-ttu-id="2199b-126">WMI implementa la classe **CIM \_ DirectoryContainsFile** , che è una classe dinamica.</span><span class="sxs-lookup"><span data-stu-id="2199b-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="2199b-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2199b-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2199b-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2199b-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2199b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2199b-129">Requirements</span></span>



| <span data-ttu-id="2199b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2199b-130">Requirement</span></span> | <span data-ttu-id="2199b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2199b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2199b-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2199b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2199b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2199b-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2199b-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2199b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2199b-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2199b-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2199b-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2199b-136">Namespace</span></span><br/>                | <span data-ttu-id="2199b-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2199b-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2199b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2199b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2199b-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2199b-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2199b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2199b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2199b-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2199b-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2199b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2199b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2199b-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="2199b-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

