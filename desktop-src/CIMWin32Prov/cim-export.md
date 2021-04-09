---
description: La \_ classe di esportazione CIM rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: Classe CIM_Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966162"
---
# <a name="cim_export-class"></a><span data-ttu-id="e2713-103">\_Classe di esportazione CIM</span><span class="sxs-lookup"><span data-stu-id="e2713-103">CIM\_Export class</span></span>

<span data-ttu-id="e2713-104">La classe di **\_ esportazione CIM** rappresenta un'associazione tra un file system locale e le relative directory, che indicano che le directory specificate sono disponibili per il montaggio.</span><span class="sxs-lookup"><span data-stu-id="e2713-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="e2713-105">Quando si esporta un intero file system, la directory deve fare riferimento alla directory più in alto della file system.</span><span class="sxs-lookup"><span data-stu-id="e2713-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2713-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e2713-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2713-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e2713-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2713-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e2713-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e2713-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e2713-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2713-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2713-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="e2713-111">Members</span><span class="sxs-lookup"><span data-stu-id="e2713-111">Members</span></span>

<span data-ttu-id="e2713-112">La classe di **\_ esportazione CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e2713-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="e2713-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2713-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2713-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2713-114">Properties</span></span>

<span data-ttu-id="e2713-115">La classe di **\_ esportazione CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2713-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2713-116">**Directory**</span><span class="sxs-lookup"><span data-stu-id="e2713-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2713-117">Tipo di dati **: \_ directory CIM**</span><span class="sxs-lookup"><span data-stu-id="e2713-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="e2713-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2713-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2713-119">Riferimento alla directory esportata per il montaggio di network file system (NFS).</span><span class="sxs-lookup"><span data-stu-id="e2713-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="e2713-120">**ExportedDirectoryName**</span><span class="sxs-lookup"><span data-stu-id="e2713-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2713-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e2713-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2713-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2713-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2713-123">Nome con cui viene esportata la directory.</span><span class="sxs-lookup"><span data-stu-id="e2713-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="e2713-124">**LocalFS**</span><span class="sxs-lookup"><span data-stu-id="e2713-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2713-125">Tipo di dati: **CIM \_ LocalFileSystem**</span><span class="sxs-lookup"><span data-stu-id="e2713-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e2713-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2713-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2713-127">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e2713-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e2713-128">Riferimento al file system locale.</span><span class="sxs-lookup"><span data-stu-id="e2713-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2713-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2713-129">Remarks</span></span>

<span data-ttu-id="e2713-130">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="e2713-130">WMI does not implement this class.</span></span>

<span data-ttu-id="e2713-131">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e2713-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2713-132">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e2713-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2713-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2713-133">Requirements</span></span>



| <span data-ttu-id="e2713-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2713-134">Requirement</span></span> | <span data-ttu-id="e2713-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e2713-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2713-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2713-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e2713-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2713-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2713-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2713-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e2713-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2713-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2713-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2713-140">Namespace</span></span><br/>                | <span data-ttu-id="e2713-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e2713-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2713-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e2713-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2713-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2713-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2713-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e2713-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2713-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2713-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

