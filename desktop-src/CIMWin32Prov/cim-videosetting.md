---
description: La \_ classe CIM VideoSetting associa l' \_ oggetto impostazione VideoControllerResolution CIM al controller a cui si applica.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: Classe CIM_VideoSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305257"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="6b391-103">CIM \_ VideoSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="6b391-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="6b391-104">La classe **CIM \_ VideoSetting** associa l'oggetto impostazione [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) al controller a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="6b391-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b391-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6b391-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b391-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b391-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b391-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6b391-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b391-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6b391-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b391-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b391-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6b391-110">Members</span><span class="sxs-lookup"><span data-stu-id="6b391-110">Members</span></span>

<span data-ttu-id="6b391-111">La classe **CIM \_ VideoSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6b391-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6b391-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b391-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b391-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b391-113">Properties</span></span>

<span data-ttu-id="6b391-114">La classe **CIM \_ VideoSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6b391-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b391-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="6b391-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b391-116">Tipo di dati: **CIM \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="6b391-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="6b391-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b391-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b391-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento")</span><span class="sxs-lookup"><span data-stu-id="6b391-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="6b391-119">Un [**\_ VideoController CIM**](cim-videocontroller.md) che descrive il controller video.</span><span class="sxs-lookup"><span data-stu-id="6b391-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="6b391-120">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="6b391-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b391-121">Tipo di dati: **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="6b391-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="6b391-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6b391-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b391-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("impostazione")</span><span class="sxs-lookup"><span data-stu-id="6b391-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="6b391-124">Un [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) che descrive le risoluzioni, le frequenze di aggiornamento, la modalità di analisi e il numero di colori che possono essere impostati per il controller.</span><span class="sxs-lookup"><span data-stu-id="6b391-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b391-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b391-125">Remarks</span></span>

<span data-ttu-id="6b391-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6b391-126">WMI does not implement this class.</span></span> <span data-ttu-id="6b391-127">Per le classi WMI derivate da **CIM \_ VideoSetting**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b391-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6b391-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b391-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b391-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6b391-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b391-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b391-130">Requirements</span></span>



| <span data-ttu-id="6b391-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b391-131">Requirement</span></span> | <span data-ttu-id="6b391-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6b391-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b391-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b391-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b391-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b391-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b391-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b391-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b391-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b391-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b391-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b391-137">Namespace</span></span><br/>                | <span data-ttu-id="6b391-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6b391-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b391-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6b391-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b391-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b391-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b391-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6b391-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b391-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b391-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b391-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b391-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b391-144">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="6b391-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

