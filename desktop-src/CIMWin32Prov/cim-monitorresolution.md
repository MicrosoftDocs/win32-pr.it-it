---
description: La \_ classe CIM MonitorResolution rappresenta la relazione tra risoluzioni orizzontali e verticali e la frequenza di aggiornamento e la modalità di analisi per un monitor desktop. I valori vengono specificati nell'oggetto controller video.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: Classe CIM_MonitorResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966224"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="0b14b-104">CIM \_ MonitorResolution (classe)</span><span class="sxs-lookup"><span data-stu-id="0b14b-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="0b14b-105">La classe **CIM \_ MonitorResolution** rappresenta la relazione tra risoluzioni orizzontali e verticali e la frequenza di aggiornamento e la modalità di analisi per un monitor desktop.</span><span class="sxs-lookup"><span data-stu-id="0b14b-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="0b14b-106">I valori vengono specificati nell'oggetto controller video.</span><span class="sxs-lookup"><span data-stu-id="0b14b-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b14b-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0b14b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b14b-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b14b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b14b-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0b14b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0b14b-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0b14b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b14b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b14b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="0b14b-112">Members</span><span class="sxs-lookup"><span data-stu-id="0b14b-112">Members</span></span>

<span data-ttu-id="0b14b-113">La classe **CIM \_ MonitorResolution** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0b14b-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="0b14b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b14b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b14b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b14b-115">Properties</span></span>

<span data-ttu-id="0b14b-116">La classe **CIM \_ MonitorResolution** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b14b-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b14b-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0b14b-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b14b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0b14b-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-121">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="0b14b-121">Short textual description of the current object.</span></span>

<span data-ttu-id="0b14b-122">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0b14b-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-123">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0b14b-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b14b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-126">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="0b14b-126">Textual description of the current object.</span></span>

<span data-ttu-id="0b14b-127">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="0b14b-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="0b14b-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b14b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-131">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="0b14b-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-132">Risoluzione orizzontale in pixel del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0b14b-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-133">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="0b14b-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b14b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-136">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,7 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="0b14b-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-137">Frequenza di aggiornamento massima del monitoraggio, in Hertz, quando un intervallo di frequenze è supportato alle risoluzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="0b14b-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-138">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="0b14b-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b14b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-141">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,6 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="0b14b-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-142">Frequenza di aggiornamento minima del monitoraggio, in Hertz, quando un intervallo di frequenze è supportato alle risoluzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="0b14b-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-143">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="0b14b-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b14b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-146">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="0b14b-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-147">Frequenza di aggiornamento del monitoraggio, in Hertz.</span><span class="sxs-lookup"><span data-stu-id="0b14b-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="0b14b-148">Se è supportato un intervallo di frequenze, usare le proprietà **MinRefreshRate** e **MaxRefreshRate** e impostare questa proprietà su 0.</span><span class="sxs-lookup"><span data-stu-id="0b14b-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-149">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="0b14b-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b14b-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-152">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. Risoluzioni di \| monitoraggio DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="0b14b-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-153">Modalità di analisi utilizzata dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="0b14b-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0b14b-154">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="0b14b-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b14b-155">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0b14b-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0b14b-156">**Non supportato** (3)</span><span class="sxs-lookup"><span data-stu-id="0b14b-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="0b14b-157">**Operazione non interlacciata** (4)</span><span class="sxs-lookup"><span data-stu-id="0b14b-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="0b14b-158">**Operazione interlacciata** (5)</span><span class="sxs-lookup"><span data-stu-id="0b14b-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b14b-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="0b14b-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0b14b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-162">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("settingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0b14b-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-163">Funge da parte della chiave per l'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="0b14b-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="0b14b-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="0b14b-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b14b-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b14b-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b14b-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b14b-167">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| monitor risoluzioni \| 002,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixel ")</span><span class="sxs-lookup"><span data-stu-id="0b14b-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="0b14b-168">Risoluzione verticale del monitoraggio in pixel.</span><span class="sxs-lookup"><span data-stu-id="0b14b-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b14b-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b14b-169">Remarks</span></span>

<span data-ttu-id="0b14b-170">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="0b14b-170">WMI does not implement this class.</span></span>

<span data-ttu-id="0b14b-171">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b14b-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b14b-172">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0b14b-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b14b-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b14b-173">Requirements</span></span>



| <span data-ttu-id="0b14b-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b14b-174">Requirement</span></span> | <span data-ttu-id="0b14b-175">Valore</span><span class="sxs-lookup"><span data-stu-id="0b14b-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b14b-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b14b-176">Minimum supported client</span></span><br/> | <span data-ttu-id="0b14b-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b14b-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b14b-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b14b-178">Minimum supported server</span></span><br/> | <span data-ttu-id="0b14b-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b14b-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b14b-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b14b-180">Namespace</span></span><br/>                | <span data-ttu-id="0b14b-181">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0b14b-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b14b-182">MOF</span><span class="sxs-lookup"><span data-stu-id="0b14b-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b14b-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b14b-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b14b-184">DLL</span><span class="sxs-lookup"><span data-stu-id="0b14b-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b14b-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b14b-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b14b-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b14b-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b14b-187">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="0b14b-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

