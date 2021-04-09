---
description: La \_ classe CIM BootOSFromFS associa il sistema operativo e i file System da cui viene caricato il sistema operativo.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: Classe CIM_BootOSFromFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 993ee7a66ef9f8b0cbb47285e38b78e4fd4dd61b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966210"
---
# <a name="cim_bootosfromfs-class"></a><span data-ttu-id="31d55-103">CIM \_ BootOSFromFS (classe)</span><span class="sxs-lookup"><span data-stu-id="31d55-103">CIM\_BootOSFromFS class</span></span>

<span data-ttu-id="31d55-104">La classe **CIM \_ BootOSFromFS** associa il sistema operativo e i file System da cui viene caricato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31d55-104">The **CIM\_BootOSFromFS** class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="31d55-105">L'associazione è molti-a-molti; un sistema operativo distribuito può dipendere da diversi file System da caricare correttamente e completamente.</span><span class="sxs-lookup"><span data-stu-id="31d55-105">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31d55-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="31d55-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31d55-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31d55-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31d55-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="31d55-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="31d55-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="31d55-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d55-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31d55-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="31d55-111">Members</span><span class="sxs-lookup"><span data-stu-id="31d55-111">Members</span></span>

<span data-ttu-id="31d55-112">La classe **CIM \_ BootOSFromFS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="31d55-112">The **CIM\_BootOSFromFS** class has these types of members:</span></span>

-   [<span data-ttu-id="31d55-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31d55-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31d55-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31d55-114">Properties</span></span>

<span data-ttu-id="31d55-115">La classe **CIM \_ BootOSFromFS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="31d55-115">The **CIM\_BootOSFromFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31d55-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="31d55-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d55-117">Tipo di dati **: \_ file System CIM**</span><span class="sxs-lookup"><span data-stu-id="31d55-117">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="31d55-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31d55-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d55-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="31d55-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="31d55-120">File system da cui viene caricato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31d55-120">The file system from which the operating system is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="31d55-121">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="31d55-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31d55-122">Tipo di dati: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="31d55-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="31d55-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31d55-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31d55-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="31d55-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="31d55-125">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31d55-125">The operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31d55-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="31d55-126">Remarks</span></span>

<span data-ttu-id="31d55-127">La classe **CIM \_ BootOSFromFS** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="31d55-127">The **CIM\_BootOSFromFS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="31d55-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="31d55-128">WMI does not implement this class.</span></span>

<span data-ttu-id="31d55-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="31d55-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31d55-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="31d55-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d55-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31d55-131">Requirements</span></span>



| <span data-ttu-id="31d55-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31d55-132">Requirement</span></span> | <span data-ttu-id="31d55-133">Valore</span><span class="sxs-lookup"><span data-stu-id="31d55-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31d55-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31d55-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31d55-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31d55-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31d55-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31d55-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31d55-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31d55-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31d55-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31d55-138">Namespace</span></span><br/>                | <span data-ttu-id="31d55-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="31d55-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31d55-140">MOF</span><span class="sxs-lookup"><span data-stu-id="31d55-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31d55-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31d55-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31d55-142">DLL</span><span class="sxs-lookup"><span data-stu-id="31d55-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d55-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31d55-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d55-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31d55-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d55-145">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="31d55-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

