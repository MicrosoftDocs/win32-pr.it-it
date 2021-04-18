---
description: Rappresenta un'intestazione di un \_ oggetto DISPLAYCONTROLLER CIM.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: Classe CIM_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310561"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="14d37-103">CIM \_ VideoHead (classe)</span><span class="sxs-lookup"><span data-stu-id="14d37-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="14d37-104">Rappresenta un'intestazione di un [**oggetto \_ DisplayController CIM**](cim-displaycontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="14d37-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14d37-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="14d37-106">Members</span><span class="sxs-lookup"><span data-stu-id="14d37-106">Members</span></span>

<span data-ttu-id="14d37-107">La classe **CIM \_ VideoHead** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="14d37-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="14d37-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14d37-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14d37-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14d37-109">Properties</span></span>

<span data-ttu-id="14d37-110">La classe **CIM \_ VideoHead** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="14d37-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14d37-111">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="14d37-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-114">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,12 "), **punito** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="14d37-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-115">Numero di bit utilizzati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="14d37-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-116">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="14d37-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-119">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,11 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution "), **punito** (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="14d37-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-120">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="14d37-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-121">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="14d37-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-122">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="14d37-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-124">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VideoHeadResolution. NumberOfColors")</span><span class="sxs-lookup"><span data-stu-id="14d37-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-125">Il numero di colori supportati nella risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="14d37-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-126">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="14d37-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-127">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-129">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 004,14 ")</span><span class="sxs-lookup"><span data-stu-id="14d37-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-130">Se è in modalità carattere, il numero di colonne per il controller di visualizzazione; in caso contrario, "0".</span><span class="sxs-lookup"><span data-stu-id="14d37-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="14d37-131">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="14d37-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-134">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 004,13 ")</span><span class="sxs-lookup"><span data-stu-id="14d37-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-135">Se è in modalità carattere, il numero di righe per il controller di visualizzazione; in caso contrario, "0".</span><span class="sxs-lookup"><span data-stu-id="14d37-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="14d37-136">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="14d37-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-139">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,15 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. RefreshRate "), **punito** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="14d37-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-140">Frequenza di aggiornamento corrente del controller di visualizzazione, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="14d37-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-141">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="14d37-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14d37-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**OtherCurrentScanMode**, CIM \_ VideoHeadResolution. ScanMode ")</span><span class="sxs-lookup"><span data-stu-id="14d37-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-145">Modalità di analisi corrente del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="14d37-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d37-146">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="14d37-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14d37-147">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="14d37-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="14d37-148">**Non supportato** (2)</span><span class="sxs-lookup"><span data-stu-id="14d37-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="14d37-149">**Operazione non interlacciata** (3)</span><span class="sxs-lookup"><span data-stu-id="14d37-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="14d37-150">**Operazione interlacciata** (4)</span><span class="sxs-lookup"><span data-stu-id="14d37-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14d37-151">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="14d37-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-154">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixel"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,10 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution "), **punito** (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="14d37-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-155">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="14d37-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-156">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="14d37-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-159">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate "), **punito** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="14d37-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-160">Frequenza di aggiornamento massima del controller di visualizzazione, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="14d37-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-161">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="14d37-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d37-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-164">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate "), **punito** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="14d37-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-165">Frequenza di aggiornamento minima del controller di visualizzazione, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="14d37-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="14d37-166">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="14d37-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d37-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="14d37-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d37-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14d37-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d37-169">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoHead**.**CurrentScanMode**, CIM \_ VideoHeadResolution. OtherScanMode ")</span><span class="sxs-lookup"><span data-stu-id="14d37-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="14d37-170">Descrizione della modalità di analisi corrente quando la proprietà **CurrentScanMode** è "1" (other).</span><span class="sxs-lookup"><span data-stu-id="14d37-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14d37-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14d37-171">Requirements</span></span>



| <span data-ttu-id="14d37-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d37-172">Requirement</span></span> | <span data-ttu-id="14d37-173">Valore</span><span class="sxs-lookup"><span data-stu-id="14d37-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d37-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14d37-174">Minimum supported client</span></span><br/> | <span data-ttu-id="14d37-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14d37-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="14d37-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14d37-176">Minimum supported server</span></span><br/> | <span data-ttu-id="14d37-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14d37-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="14d37-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14d37-178">Namespace</span></span><br/>                | <span data-ttu-id="14d37-179">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="14d37-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14d37-180">MOF</span><span class="sxs-lookup"><span data-stu-id="14d37-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14d37-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14d37-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14d37-182">DLL</span><span class="sxs-lookup"><span data-stu-id="14d37-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d37-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14d37-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14d37-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14d37-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d37-185">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="14d37-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

