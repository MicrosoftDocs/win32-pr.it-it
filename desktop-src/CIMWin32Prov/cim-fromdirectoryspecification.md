---
description: L' \_ associazione CIM FromDirectorySpecification identifica la directory di origine per l'azione del file.
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: Classe CIM_FromDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7690514b46d89bdf1aa926438456c49598034700
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304910"
---
# <a name="cim_fromdirectoryspecification-class"></a><span data-ttu-id="38b44-103">CIM \_ FromDirectorySpecification (classe)</span><span class="sxs-lookup"><span data-stu-id="38b44-103">CIM\_FromDirectorySpecification class</span></span>

<span data-ttu-id="38b44-104">L'associazione **CIM \_ FromDirectorySpecification** identifica la directory di origine per l'azione del file.</span><span class="sxs-lookup"><span data-stu-id="38b44-104">The **CIM\_FromDirectorySpecification** association identifies the source directory for the file action.</span></span> <span data-ttu-id="38b44-105">Quando si utilizza questa associazione, il presupposto è che la directory di origine esista già.</span><span class="sxs-lookup"><span data-stu-id="38b44-105">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="38b44-106">Questa associazione non può esistere con un'associazione [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) ; un'azione file può coinvolgere solo una singola directory di origine.</span><span class="sxs-lookup"><span data-stu-id="38b44-106">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38b44-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="38b44-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="38b44-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="38b44-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="38b44-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="38b44-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="38b44-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="38b44-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b44-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38b44-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="38b44-112">Members</span><span class="sxs-lookup"><span data-stu-id="38b44-112">Members</span></span>

<span data-ttu-id="38b44-113">La classe **CIM \_ FromDirectorySpecification** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="38b44-113">The **CIM\_FromDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="38b44-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38b44-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38b44-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38b44-115">Properties</span></span>

<span data-ttu-id="38b44-116">La classe **CIM \_ FromDirectorySpecification** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="38b44-116">The **CIM\_FromDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38b44-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="38b44-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b44-118">Tipo di dati **: \_ Fileaction CIM**</span><span class="sxs-lookup"><span data-stu-id="38b44-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="38b44-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b44-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b44-120">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="38b44-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="38b44-121">Riferimento al nome del file.</span><span class="sxs-lookup"><span data-stu-id="38b44-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="38b44-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="38b44-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b44-123">Tipo di dati: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="38b44-123">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="38b44-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38b44-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38b44-125">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="38b44-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="38b44-126">Riferimento alla directory di origine.</span><span class="sxs-lookup"><span data-stu-id="38b44-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b44-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="38b44-127">Remarks</span></span>

<span data-ttu-id="38b44-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="38b44-128">WMI does not implement this class.</span></span>

<span data-ttu-id="38b44-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="38b44-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="38b44-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="38b44-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b44-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38b44-131">Requirements</span></span>



| <span data-ttu-id="38b44-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b44-132">Requirement</span></span> | <span data-ttu-id="38b44-133">Valore</span><span class="sxs-lookup"><span data-stu-id="38b44-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38b44-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38b44-134">Minimum supported client</span></span><br/> | <span data-ttu-id="38b44-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38b44-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38b44-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38b44-136">Minimum supported server</span></span><br/> | <span data-ttu-id="38b44-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38b44-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38b44-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38b44-138">Namespace</span></span><br/>                | <span data-ttu-id="38b44-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="38b44-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38b44-140">MOF</span><span class="sxs-lookup"><span data-stu-id="38b44-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38b44-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38b44-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38b44-142">DLL</span><span class="sxs-lookup"><span data-stu-id="38b44-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38b44-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38b44-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

