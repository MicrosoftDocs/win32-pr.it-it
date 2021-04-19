---
description: L' \_ associazione CIM filestorage collega i file System e i file logici risolti tramite l'file System.
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: Classe CIM_FileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304912"
---
# <a name="cim_filestorage-class"></a><span data-ttu-id="bb46f-103">\_Classe CIM filestorage</span><span class="sxs-lookup"><span data-stu-id="bb46f-103">CIM\_FileStorage class</span></span>

<span data-ttu-id="bb46f-104">L'associazione **CIM \_ filestorage** collega i file System e i file logici risolti tramite l'file System.</span><span class="sxs-lookup"><span data-stu-id="bb46f-104">The **CIM\_FileStorage** association links the file system and the logical files addressed through the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb46f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="bb46f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bb46f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bb46f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bb46f-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bb46f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bb46f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="bb46f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb46f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb46f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="bb46f-110">Members</span><span class="sxs-lookup"><span data-stu-id="bb46f-110">Members</span></span>

<span data-ttu-id="bb46f-111">La classe **CIM \_ filestorage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bb46f-111">The **CIM\_FileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="bb46f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb46f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb46f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb46f-113">Properties</span></span>

<span data-ttu-id="bb46f-114">La classe **CIM \_ filestorage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb46f-114">The **CIM\_FileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb46f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bb46f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46f-116">Tipo di dati **: \_ file System CIM**</span><span class="sxs-lookup"><span data-stu-id="bb46f-116">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="bb46f-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb46f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb46f-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="bb46f-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="bb46f-119">Un [**\_ file System CIM**](cim-filesystem.md) che descrive la file System.</span><span class="sxs-lookup"><span data-stu-id="bb46f-119">A [**CIM\_FileSystem**](cim-filesystem.md) describing the file system.</span></span>

</dd> <dt>

<span data-ttu-id="bb46f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bb46f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb46f-121">Tipo di dati: **CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="bb46f-121">Data type: **CIM\_LogicalFile**</span></span>
</dt> <dt>

<span data-ttu-id="bb46f-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb46f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb46f-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bb46f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bb46f-124">[**\_ LogicalFile CIM**](cim-logicalfile.md) che descrive il file logico archiviato nel contesto del file System.</span><span class="sxs-lookup"><span data-stu-id="bb46f-124">A [**CIM\_LogicalFile**](cim-logicalfile.md) describing the logical file stored in the context of the file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb46f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb46f-125">Remarks</span></span>

<span data-ttu-id="bb46f-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="bb46f-126">WMI does not implement this class.</span></span>

<span data-ttu-id="bb46f-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="bb46f-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bb46f-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="bb46f-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb46f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb46f-129">Requirements</span></span>



| <span data-ttu-id="bb46f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb46f-130">Requirement</span></span> | <span data-ttu-id="bb46f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bb46f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb46f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb46f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bb46f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb46f-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb46f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb46f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bb46f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb46f-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb46f-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb46f-136">Namespace</span></span><br/>                | <span data-ttu-id="bb46f-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bb46f-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb46f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="bb46f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb46f-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb46f-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb46f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bb46f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb46f-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb46f-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb46f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb46f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb46f-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="bb46f-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

