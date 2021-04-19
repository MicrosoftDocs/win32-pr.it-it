---
description: La \_ classe CIM ElementSetting rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: Classe CIM_ElementSetting (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304920"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a><span data-ttu-id="0db91-103">Classe CIM_ElementSetting (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0db91-103">CIM_ElementSetting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0db91-104">La classe **CIM \_ ElementSetting** rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita.</span><span class="sxs-lookup"><span data-stu-id="0db91-104">The **CIM\_ElementSetting** class represents the association between managed system elements and the setting class defined for them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0db91-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0db91-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0db91-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0db91-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0db91-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0db91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0db91-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0db91-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db91-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0db91-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="0db91-110">Members</span><span class="sxs-lookup"><span data-stu-id="0db91-110">Members</span></span>

<span data-ttu-id="0db91-111">La classe **CIM \_ ElementSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0db91-111">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0db91-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0db91-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0db91-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0db91-113">Properties</span></span>

<span data-ttu-id="0db91-114">La classe **CIM \_ ElementSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0db91-114">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0db91-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="0db91-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0db91-116">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="0db91-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="0db91-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0db91-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0db91-118">Riferimento al ruolo dell'oggetto [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) dell'associazione **CIM \_ ElementSetting** .</span><span class="sxs-lookup"><span data-stu-id="0db91-118">Reference to the role of the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="0db91-119">L'elemento del sistema gestito associato fornisce l'elemento che implementa l'impostazione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0db91-119">The associated managed system element provides the element that implements the element setting.</span></span>

</dd> <dt>

<span data-ttu-id="0db91-120">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="0db91-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0db91-121">Tipo di dati **: \_ impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="0db91-121">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="0db91-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0db91-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0db91-123">Riferimento al ruolo dell'oggetto [**\_ impostazione CIM**](cim-setting.md) dell'associazione **CIM \_ ElementSetting** .</span><span class="sxs-lookup"><span data-stu-id="0db91-123">Reference to the role of the [**CIM\_Setting**](cim-setting.md) object of the **CIM\_ElementSetting** association.</span></span> <span data-ttu-id="0db91-124">L'impostazione associata fornisce l'impostazione che implementa l'impostazione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0db91-124">The associated setting provides the setting that implements the element setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0db91-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="0db91-125">Remarks</span></span>

<span data-ttu-id="0db91-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="0db91-126">WMI does not implement this class.</span></span> <span data-ttu-id="0db91-127">Per le classi derivate da **CIM \_ ElementSetting**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0db91-127">For classes derived from **CIM\_ElementSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0db91-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0db91-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0db91-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0db91-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db91-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0db91-130">Requirements</span></span>



| <span data-ttu-id="0db91-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db91-131">Requirement</span></span> | <span data-ttu-id="0db91-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0db91-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db91-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0db91-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0db91-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0db91-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0db91-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0db91-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0db91-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0db91-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0db91-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0db91-137">Namespace</span></span><br/>                | <span data-ttu-id="0db91-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0db91-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0db91-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0db91-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0db91-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0db91-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0db91-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0db91-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db91-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db91-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




