---
description: La \_ classe di associazione CIM CollectedMSEs rappresenta i membri dell'oggetto GROUPING, una classe CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: Classe CIM_CollectedMSEs (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 154436934e8a8fe417215874ddb98e449b854025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483541"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="6b6a9-103">Classe CIM_CollectedMSEs (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6b6a9-103">CIM_CollectedMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6b6a9-104">La classe di associazione **CIM \_ CollectedMSEs** rappresenta i membri dell'oggetto GROUPING, una classe [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="6b6a9-104">The **CIM\_CollectedMSEs** association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b6a9-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b6a9-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b6a9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b6a9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6b6a9-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6a9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b6a9-109">Syntax</span></span>

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="6b6a9-110">Members</span><span class="sxs-lookup"><span data-stu-id="6b6a9-110">Members</span></span>

<span data-ttu-id="6b6a9-111">La classe **CIM \_ CollectedMSEs** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6b6a9-111">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="6b6a9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b6a9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b6a9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b6a9-113">Properties</span></span>

<span data-ttu-id="6b6a9-114">La classe **CIM \_ CollectedMSEs** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-114">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b6a9-115">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="6b6a9-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6a9-116">Tipo di dati: **cm \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="6b6a9-116">Data type: **CM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="6b6a9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b6a9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b6a9-118">Riferimento all'oggetto Grouping o "Bag" che rappresenta la raccolta.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-118">Reference to the grouping or "bag" object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="6b6a9-119">**Membro**</span><span class="sxs-lookup"><span data-stu-id="6b6a9-119">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6a9-120">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="6b6a9-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="6b6a9-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b6a9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b6a9-122">Riferimento a un membro della raccolta.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-122">Reference to a member of the collection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b6a9-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b6a9-123">Remarks</span></span>

<span data-ttu-id="6b6a9-124">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-124">WMI does not implement this class.</span></span> <span data-ttu-id="6b6a9-125">Per ulteriori informazioni sulle classi WMI derivate da **CIM \_ CollectedMSEs**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b6a9-125">For more information about WMI classes derived from **CIM\_CollectedMSEs**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6b6a9-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b6a9-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6b6a9-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6a9-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b6a9-128">Requirements</span></span>



| <span data-ttu-id="6b6a9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b6a9-129">Requirement</span></span> | <span data-ttu-id="6b6a9-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6b6a9-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6a9-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b6a9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6a9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b6a9-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b6a9-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b6a9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6a9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b6a9-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b6a9-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b6a9-135">Namespace</span></span><br/>                | <span data-ttu-id="6b6a9-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6b6a9-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b6a9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6b6a9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b6a9-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b6a9-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b6a9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6b6a9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b6a9-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b6a9-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




