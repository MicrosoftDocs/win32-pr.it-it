---
description: Rappresenta un monitor desktop CRT.
ms.assetid: 26a06320-9fd9-434e-87c8-486e9ca4945c
title: Classe CIM_DesktopMonitor (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab152fc10f3fd404744c293d2368039ffcfdb291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308359"
---
# <a name="cim_desktopmonitor-class-hyper-v-management"></a><span data-ttu-id="8732b-103">Classe CIM_DesktopMonitor (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="8732b-103">CIM_DesktopMonitor class (Hyper-V management)</span></span>

<span data-ttu-id="8732b-104">Rappresenta un monitor desktop CRT.</span><span class="sxs-lookup"><span data-stu-id="8732b-104">Represents a CRT desktop monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8732b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8732b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices")]
class CIM_DesktopMonitor : CIM_Display
{
  uint16 DisplayType;
  uint32 Bandwidth;
  uint32 ScreenHeight;
  uint32 ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="8732b-106">Members</span><span class="sxs-lookup"><span data-stu-id="8732b-106">Members</span></span>

<span data-ttu-id="8732b-107">La classe **CIM \_ DesktopMonitor** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8732b-107">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="8732b-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8732b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8732b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8732b-109">Properties</span></span>

<span data-ttu-id="8732b-110">La classe **CIM \_ DesktopMonitor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8732b-110">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8732b-111">**Larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="8732b-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8732b-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8732b-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8732b-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8732b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8732b-114">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz"), **punito** ("Hertz \* 10 ^ 6")</span><span class="sxs-lookup"><span data-stu-id="8732b-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MegaHertz"), **PUnit** ("hertz \* 10^6")</span></span>
</dt> </dl>

<span data-ttu-id="8732b-115">Larghezza di banda dello schermo, in MHertz.</span><span class="sxs-lookup"><span data-stu-id="8732b-115">The bandwidth of the display, in MHertz.</span></span> <span data-ttu-id="8732b-116">"0" indica Unknown.</span><span class="sxs-lookup"><span data-stu-id="8732b-116">"0" indicates unknown.</span></span>

</dd> <dt>

<span data-ttu-id="8732b-117">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="8732b-117">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8732b-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8732b-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8732b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8732b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8732b-120">Tipo di tipo di visualizzazione del monitor CRT.</span><span class="sxs-lookup"><span data-stu-id="8732b-120">The type of display type of the CRT monitor.</span></span> <span data-ttu-id="8732b-121">Ad esempio, colore MultiScan o monocromatico.</span><span class="sxs-lookup"><span data-stu-id="8732b-121">For example, multiscan color, or monochrome.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8732b-122">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8732b-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8732b-123">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="8732b-123">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="8732b-124">**Colore MultiScan** (2)</span><span class="sxs-lookup"><span data-stu-id="8732b-124">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="8732b-125">**MultiScan monocromatico** (3)</span><span class="sxs-lookup"><span data-stu-id="8732b-125">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="8732b-126">**Colore a frequenza fissa** (4)</span><span class="sxs-lookup"><span data-stu-id="8732b-126">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="8732b-127">**Frequenza fissa monocromatico** (5)</span><span class="sxs-lookup"><span data-stu-id="8732b-127">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8732b-128">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="8732b-128">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8732b-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8732b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8732b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8732b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8732b-131">Altezza logica dello schermo, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8732b-131">The logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="8732b-132">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="8732b-132">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8732b-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8732b-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8732b-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8732b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8732b-135">Larghezza logica dello schermo, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8732b-135">The logical width of the display, in screen coordinates.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8732b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8732b-136">Requirements</span></span>



| <span data-ttu-id="8732b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8732b-137">Requirement</span></span> | <span data-ttu-id="8732b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="8732b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8732b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8732b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8732b-140">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8732b-140">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8732b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8732b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8732b-142">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8732b-142">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8732b-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8732b-143">Namespace</span></span><br/>                | <span data-ttu-id="8732b-144">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8732b-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8732b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="8732b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8732b-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8732b-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8732b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8732b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8732b-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8732b-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8732b-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8732b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8732b-150">**\_Visualizzazione CIM**</span><span class="sxs-lookup"><span data-stu-id="8732b-150">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

