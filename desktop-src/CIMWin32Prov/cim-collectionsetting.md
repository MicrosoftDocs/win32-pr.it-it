---
description: La \_ classe CIM CollectionSetting rappresenta l'associazione tra un \_ CollectionOfMSEs CIM e la classe di impostazione definita.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: Classe CIM_CollectionSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877985"
---
# <a name="cim_collectionsetting-class"></a><span data-ttu-id="9a08f-103">CIM \_ CollectionSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="9a08f-103">CIM\_CollectionSetting class</span></span>

<span data-ttu-id="9a08f-104">La classe **CIM \_ CollectionSetting** rappresenta l'associazione tra un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) e la classe di impostazione definita.</span><span class="sxs-lookup"><span data-stu-id="9a08f-104">The **CIM\_CollectionSetting** class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a08f-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9a08f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9a08f-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9a08f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9a08f-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9a08f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9a08f-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9a08f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a08f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a08f-109">Syntax</span></span>

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="9a08f-110">Members</span><span class="sxs-lookup"><span data-stu-id="9a08f-110">Members</span></span>

<span data-ttu-id="9a08f-111">La classe **CIM \_ CollectionSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9a08f-111">The **CIM\_CollectionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="9a08f-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9a08f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a08f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9a08f-113">Properties</span></span>

<span data-ttu-id="9a08f-114">La classe **CIM \_ CollectionSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9a08f-114">The **CIM\_CollectionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a08f-115">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="9a08f-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a08f-116">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="9a08f-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="9a08f-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9a08f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a08f-118">Riferimento alla classe [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="9a08f-118">Reference to the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9a08f-119">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="9a08f-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a08f-120">Tipo di dati **: \_ impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="9a08f-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="9a08f-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9a08f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a08f-122">Riferimento all'oggetto **Setting** associato alla proprietà della **raccolta** .</span><span class="sxs-lookup"><span data-stu-id="9a08f-122">Reference to the **Setting** object associated with the **Collection** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a08f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a08f-123">Remarks</span></span>

<span data-ttu-id="9a08f-124">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9a08f-124">WMI does not implement this class.</span></span> <span data-ttu-id="9a08f-125">Per ulteriori informazioni sulle classi WMI derivate da **CIM \_ CollectionSetting**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9a08f-125">For more information about WMI classes derived from **CIM\_CollectionSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9a08f-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9a08f-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9a08f-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9a08f-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a08f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a08f-128">Requirements</span></span>



| <span data-ttu-id="9a08f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a08f-129">Requirement</span></span> | <span data-ttu-id="9a08f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9a08f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a08f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a08f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9a08f-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a08f-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a08f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a08f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9a08f-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a08f-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a08f-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a08f-135">Namespace</span></span><br/>                | <span data-ttu-id="9a08f-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9a08f-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a08f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9a08f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a08f-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a08f-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a08f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9a08f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a08f-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a08f-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




