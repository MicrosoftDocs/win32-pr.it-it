---
description: L' \_ associazione CIM DirectorySpecificationFile rappresenta la directory che contiene il file specificato facendo riferimento alla \_ classe CIM DirectorySpecification.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: Classe CIM_DirectorySpecificationFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127183"
---
# <a name="cim_directoryspecificationfile-class"></a><span data-ttu-id="9910d-103">CIM \_ DirectorySpecificationFile (classe)</span><span class="sxs-lookup"><span data-stu-id="9910d-103">CIM\_DirectorySpecificationFile class</span></span>

<span data-ttu-id="9910d-104">L'associazione **CIM \_ DirectorySpecificationFile** rappresenta la directory che contiene il file specificato facendo riferimento alla classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="9910d-104">The **CIM\_DirectorySpecificationFile** association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9910d-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9910d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9910d-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9910d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9910d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9910d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9910d-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9910d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9910d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9910d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a><span data-ttu-id="9910d-110">Members</span><span class="sxs-lookup"><span data-stu-id="9910d-110">Members</span></span>

<span data-ttu-id="9910d-111">La classe **CIM \_ DirectorySpecificationFile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9910d-111">The **CIM\_DirectorySpecificationFile** class has these types of members:</span></span>

-   [<span data-ttu-id="9910d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9910d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9910d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9910d-113">Properties</span></span>

<span data-ttu-id="9910d-114">La classe **CIM \_ DirectorySpecificationFile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9910d-114">The **CIM\_DirectorySpecificationFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9910d-115">**DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="9910d-115">**DirectorySpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9910d-116">Tipo di dati: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="9910d-116">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="9910d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9910d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9910d-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="9910d-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9910d-119">Riferimento alla specifica di directory.</span><span class="sxs-lookup"><span data-stu-id="9910d-119">Reference to the directory specification.</span></span>

</dd> <dt>

<span data-ttu-id="9910d-120">**Filespecificazione**</span><span class="sxs-lookup"><span data-stu-id="9910d-120">**FileSpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9910d-121">Tipo di dati **: \_ filespecificazione CIM**</span><span class="sxs-lookup"><span data-stu-id="9910d-121">Data type: **CIM\_FileSpecification**</span></span>
</dt> <dt>

<span data-ttu-id="9910d-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9910d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9910d-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="9910d-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="9910d-124">Riferimento alla specifica del file.</span><span class="sxs-lookup"><span data-stu-id="9910d-124">Reference to the file specification.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9910d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9910d-125">Remarks</span></span>

<span data-ttu-id="9910d-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9910d-126">WMI does not implement this class.</span></span>

<span data-ttu-id="9910d-127">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9910d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9910d-128">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9910d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9910d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9910d-129">Requirements</span></span>



| <span data-ttu-id="9910d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9910d-130">Requirement</span></span> | <span data-ttu-id="9910d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9910d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9910d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9910d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9910d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9910d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9910d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9910d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9910d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9910d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9910d-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9910d-136">Namespace</span></span><br/>                | <span data-ttu-id="9910d-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9910d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9910d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9910d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9910d-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9910d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9910d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9910d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9910d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9910d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

