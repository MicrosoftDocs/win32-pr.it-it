---
description: L' \_ associazione CIM MediaPresent descrive una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: Classe CIM_MediaPresent (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103885998"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a><span data-ttu-id="6b8b5-103">Classe CIM_MediaPresent (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6b8b5-103">CIM_MediaPresent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6b8b5-104">L'associazione **CIM \_ MediaPresent** descrive una relazione in cui è necessario accedere a un extent di archiviazione tramite un dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-104">The **CIM\_MediaPresent** association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b8b5-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b8b5-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b8b5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b8b5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6b8b5-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8b5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8b5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6b8b5-110">Members</span><span class="sxs-lookup"><span data-stu-id="6b8b5-110">Members</span></span>

<span data-ttu-id="6b8b5-111">La classe **CIM \_ MediaPresent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6b8b5-111">The **CIM\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="6b8b5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b8b5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b8b5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b8b5-113">Properties</span></span>

<span data-ttu-id="6b8b5-114">La classe **CIM \_ MediaPresent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-114">The **CIM\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b8b5-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6b8b5-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b8b5-116">Tipo di dati: **CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="6b8b5-116">Data type: **CIM\_MediaAccessDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6b8b5-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b8b5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b8b5-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="6b8b5-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6b8b5-119">Un [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md) che descrive il dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-119">A [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) that describes the media access device.</span></span>

</dd> <dt>

<span data-ttu-id="6b8b5-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="6b8b5-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b8b5-121">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="6b8b5-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="6b8b5-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b8b5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b8b5-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="6b8b5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6b8b5-124">Un [**\_ StorageExtent CIM**](cim-storageextent.md) che descrive l'ambito di archiviazione A cui si accede tramite il dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-124">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent accessed using the media access device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b8b5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8b5-125">Remarks</span></span>

<span data-ttu-id="6b8b5-126">La classe **CIM \_ MediaPresent** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="6b8b5-126">The **CIM\_MediaPresent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="6b8b5-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-127">WMI does not implement this class.</span></span> <span data-ttu-id="6b8b5-128">Per le classi derivate da **CIM \_ MediaPresent**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b8b5-128">For classes derived from **CIM\_MediaPresent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6b8b5-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b8b5-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6b8b5-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8b5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8b5-131">Requirements</span></span>



| <span data-ttu-id="6b8b5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8b5-132">Requirement</span></span> | <span data-ttu-id="6b8b5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8b5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8b5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8b5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8b5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b8b5-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b8b5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8b5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8b5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b8b5-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b8b5-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b8b5-138">Namespace</span></span><br/>                | <span data-ttu-id="6b8b5-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6b8b5-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b8b5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6b8b5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b8b5-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b8b5-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b8b5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6b8b5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b8b5-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b8b5-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8b5-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8b5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8b5-145">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="6b8b5-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

