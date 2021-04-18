---
description: La \_ classe WMI dell'associazione VideoSettings Win32 mette in correlazione un controller video e le impostazioni video a cui è possibile applicare.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Classe Win32_VideoSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304571"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="d9dc3-103">Win32 \_ VideoSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="d9dc3-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="d9dc3-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ VideoSettings Win32** mette in correlazione un controller video e le impostazioni video a cui è possibile applicare.</span><span class="sxs-lookup"><span data-stu-id="d9dc3-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="d9dc3-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d9dc3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d9dc3-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d9dc3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9dc3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9dc3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="d9dc3-108">Members</span><span class="sxs-lookup"><span data-stu-id="d9dc3-108">Members</span></span>

<span data-ttu-id="d9dc3-109">La classe **Win32 \_ VideoSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d9dc3-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="d9dc3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d9dc3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9dc3-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d9dc3-111">Properties</span></span>

<span data-ttu-id="d9dc3-112">La classe **Win32 \_ VideoSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d9dc3-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9dc3-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="d9dc3-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9dc3-114">Tipo di dati: **Win32 \_ VideoController**</span><span class="sxs-lookup"><span data-stu-id="d9dc3-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="d9dc3-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d9dc3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9dc3-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ VideoController")</span><span class="sxs-lookup"><span data-stu-id="d9dc3-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="d9dc3-117">[**\_ VideoController Win32**](win32-videocontroller.md) che contiene le proprietà del controller video in cui è possibile utilizzare un'impostazione video.</span><span class="sxs-lookup"><span data-stu-id="d9dc3-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="d9dc3-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="d9dc3-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9dc3-119">Tipo di dati: **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="d9dc3-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="d9dc3-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d9dc3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9dc3-121">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")</span><span class="sxs-lookup"><span data-stu-id="d9dc3-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="d9dc3-122">Un [**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) contenente le impostazioni che possono essere applicate al controller video.</span><span class="sxs-lookup"><span data-stu-id="d9dc3-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9dc3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9dc3-123">Remarks</span></span>

<span data-ttu-id="d9dc3-124">La classe **Win32 \_ VideoSettings** è derivata da [**CIM \_ VideoSetting**](cim-videosetting.md).</span><span class="sxs-lookup"><span data-stu-id="d9dc3-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9dc3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9dc3-125">Requirements</span></span>



| <span data-ttu-id="d9dc3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9dc3-126">Requirement</span></span> | <span data-ttu-id="d9dc3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d9dc3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dc3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9dc3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d9dc3-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9dc3-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9dc3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9dc3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d9dc3-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9dc3-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9dc3-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9dc3-132">Namespace</span></span><br/>                | <span data-ttu-id="d9dc3-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d9dc3-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9dc3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d9dc3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9dc3-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9dc3-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9dc3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d9dc3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9dc3-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9dc3-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9dc3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9dc3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9dc3-139">**\_VIDEOSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="d9dc3-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="d9dc3-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d9dc3-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
