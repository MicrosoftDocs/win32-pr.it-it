---
description: La \_ classe Win32 VideoConfiguration non è attiva. Non verrà restituita alcuna istanza perché non è presente alcun provider sottostante.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Classe Win32_VideoConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ad4206cc50953a135b23257526ffb5cdc59b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523194"
---
# <a name="win32_videoconfiguration-class"></a><span data-ttu-id="a4f20-104">Win32 \_ VideoConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="a4f20-104">Win32\_VideoConfiguration class</span></span>

<span data-ttu-id="a4f20-105">La classe **Win32 \_ VideoConfiguration** non è attiva.</span><span class="sxs-lookup"><span data-stu-id="a4f20-105">The **Win32\_VideoConfiguration** class is not active.</span></span> <span data-ttu-id="a4f20-106">Non verrà restituita alcuna istanza perché non è presente alcun provider sottostante.</span><span class="sxs-lookup"><span data-stu-id="a4f20-106">It will not return any instances as there is no provider backing it.</span></span>

<span data-ttu-id="a4f20-107">La classe **Win32 \_ VideoConfiguration** rappresenta una configurazione di un sottosistema video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-107">The **Win32\_VideoConfiguration** class represents a configuration of a video subsystem.</span></span> <span data-ttu-id="a4f20-108">Questa classe è stata deprecata a favore delle proprietà contenute nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)</span><span class="sxs-lookup"><span data-stu-id="a4f20-108">This class has been deprecated in favor of the properties contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes</span></span>

<span data-ttu-id="a4f20-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a4f20-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f20-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4f20-110">Syntax</span></span>

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="a4f20-111">Members</span><span class="sxs-lookup"><span data-stu-id="a4f20-111">Members</span></span>

<span data-ttu-id="a4f20-112">La classe **Win32 \_ VideoConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a4f20-112">The **Win32\_VideoConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="a4f20-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4f20-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4f20-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4f20-114">Properties</span></span>

<span data-ttu-id="a4f20-115">La classe **Win32 \_ VideoConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4f20-115">The **Win32\_VideoConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4f20-116">**ActualColorResolution**</span><span class="sxs-lookup"><span data-stu-id="a4f20-116">**ActualColorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-119">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**unità**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span><span class="sxs-lookup"><span data-stu-id="a4f20-119">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|COLORRES"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per pixel")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-120">Indica la profondità di colore corrente della visualizzazione video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-120">Indicates the current color depth of the video display.</span></span>

<span data-ttu-id="a4f20-121">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-121">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-122">**AdapterChipType**</span><span class="sxs-lookup"><span data-stu-id="a4f20-122">**AdapterChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-125">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| ChipType")</span><span class="sxs-lookup"><span data-stu-id="a4f20-125">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|ChipType")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-126">Contiene il nome del chip dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="a4f20-126">Contains the name of the adapter chip.</span></span>

<span data-ttu-id="a4f20-127">Esempio: S3</span><span class="sxs-lookup"><span data-stu-id="a4f20-127">Example: s3</span></span>

<span data-ttu-id="a4f20-128">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-128">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-129">**AdapterCompatibility**</span><span class="sxs-lookup"><span data-stu-id="a4f20-129">**AdapterCompatibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-132">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4f20-132">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-133">Specifica il nome del produttore dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="a4f20-133">Specifies the name of the manufacturer of the adapter.</span></span> <span data-ttu-id="a4f20-134">Questo nome può essere utilizzato per confrontare la compatibilità del dispositivo con le esigenze del computer.</span><span class="sxs-lookup"><span data-stu-id="a4f20-134">This name can be used to compare the compatibility of this device with the needs of the computer system.</span></span>

<span data-ttu-id="a4f20-135">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-135">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-136">**AdapterDACType**</span><span class="sxs-lookup"><span data-stu-id="a4f20-136">**AdapterDACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-139">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| DACType")</span><span class="sxs-lookup"><span data-stu-id="a4f20-139">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|DACType")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-140">Indica il nome del chip da digitale a analogico (DAC) utilizzato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="a4f20-140">Indicates the name of the digital-to-analog chip (DAC) used in the adapter.</span></span>

<span data-ttu-id="a4f20-141">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-141">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-142">**AdapterDescription**</span><span class="sxs-lookup"><span data-stu-id="a4f20-142">**AdapterDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-145">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4f20-145">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-146">Contiene una descrizione o un nome descrittivo della scheda video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-146">Contains a description or descriptive name of the video adapter.</span></span>

<span data-ttu-id="a4f20-147">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-147">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-148">**AdapterRAM**</span><span class="sxs-lookup"><span data-stu-id="a4f20-148">**AdapterRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-151">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ info \| VideoMemory"), [**unità**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a4f20-151">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Info\|VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-152">Indica le dimensioni della memoria della scheda video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-152">Indicates the memory size of the video adapter.</span></span>

<span data-ttu-id="a4f20-153">Esempio: 16777216</span><span class="sxs-lookup"><span data-stu-id="a4f20-153">Example: 16777216</span></span>

<span data-ttu-id="a4f20-154">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-154">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-155">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="a4f20-155">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-158">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \\ \\ DisplayController \\ \\ 0 \\ \\ Identifier")</span><span class="sxs-lookup"><span data-stu-id="a4f20-158">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\DisplayController\\\\0\\\\Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-159">Indica il tipo di scheda video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-159">Indicates the type of video adapter.</span></span>

<span data-ttu-id="a4f20-160">Set di caratteri: alfanumerico</span><span class="sxs-lookup"><span data-stu-id="a4f20-160">Character Set: Alphanumeric</span></span>

<span data-ttu-id="a4f20-161">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-161">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-162">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="a4f20-162">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-165">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="a4f20-165">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-166">Indica il numero effettivo di bit per pixel che rappresenta la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a4f20-166">Indicates the actual number of bits per pixel representing the display.</span></span> <span data-ttu-id="a4f20-167">Questo può essere ridimensionato in base all'impostazione video corrente (rappresentata dalla proprietà ActualColorResolution) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a4f20-167">This may be scaled to the current video setting (represented by the ActualColorResolution property) of the user.</span></span>

<span data-ttu-id="a4f20-168">Esempio: 8</span><span class="sxs-lookup"><span data-stu-id="a4f20-168">Example: 8</span></span>

<span data-ttu-id="a4f20-169">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-169">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-170">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a4f20-170">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-173">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="a4f20-173">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-174">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="a4f20-174">Short textual description of the current object.</span></span>

<span data-ttu-id="a4f20-175">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-175">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-176">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="a4f20-176">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-179">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| Planes")</span><span class="sxs-lookup"><span data-stu-id="a4f20-179">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-180">Indica il numero corrente di piani di colore utilizzati nella visualizzazione video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-180">Indicates the current number of color planes used in the video display.</span></span> <span data-ttu-id="a4f20-181">Un piano colori rappresenta un altro modo per rappresentare i colori del pixel; anziché assegnare un singolo valore RGB a ogni pixel, i piani dei colori separano il grafico in ogni componente del colore principale (blu verde) e li archiviano nei propri piani.</span><span class="sxs-lookup"><span data-stu-id="a4f20-181">A color plane is another way to represent pixel colors; instead of assigning a single RGB value to each a pixel, color planes separate the graphic into each of the primary color components (red green blue), and store them in their own planes.</span></span> <span data-ttu-id="a4f20-182">In questo modo è possibile ottenere una profondità di colore maggiore nei sistemi video a 8 e 16 bit.</span><span class="sxs-lookup"><span data-stu-id="a4f20-182">This allows for greater color depths on 8 and 16 bit video systems.</span></span> <span data-ttu-id="a4f20-183">I sistemi grafici presenti hanno bitwidth dimensioni sufficienti per archiviare le informazioni relative alla profondità dei colori, rendendo necessario solo un piano di colore.</span><span class="sxs-lookup"><span data-stu-id="a4f20-183">Present graphics systems have the bitwidth large enough to store color depth information, making only one color plane necessary.</span></span>

<span data-ttu-id="a4f20-184">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="a4f20-184">Example: 1</span></span>

<span data-ttu-id="a4f20-185">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-185">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-186">**ColorTableEntries**</span><span class="sxs-lookup"><span data-stu-id="a4f20-186">**ColorTableEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-189">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="a4f20-189">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-190">Indica il numero di indici di colore in una tabella dei colori per una visualizzazione video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-190">Indicates the number of color indexes in a color table for a video display.</span></span> <span data-ttu-id="a4f20-191">Questa proprietà viene usata se il dispositivo ha una profondità di colore non superiore a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="a4f20-191">This property is used if the device has a color depth of no more than 8 bits per pixel.</span></span> <span data-ttu-id="a4f20-192">Per i dispositivi con profondità dei colori maggiori, viene restituito-1.</span><span class="sxs-lookup"><span data-stu-id="a4f20-192">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="a4f20-193">Esempio: 256</span><span class="sxs-lookup"><span data-stu-id="a4f20-193">Example: 256</span></span>

<span data-ttu-id="a4f20-194">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-194">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-195">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a4f20-195">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-198">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="a4f20-198">Textual description of the current object.</span></span>

<span data-ttu-id="a4f20-199">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-199">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-200">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="a4f20-200">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-203">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="a4f20-203">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-204">Indica il numero corrente di penne specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4f20-204">Indicates the current number of device-specific pens.</span></span> <span data-ttu-id="a4f20-205">Il valore 0xFFFFFFFF indica che il dispositivo non supporta le penne.</span><span class="sxs-lookup"><span data-stu-id="a4f20-205">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="a4f20-206">Le penne vengono utilizzate per creare linee e theborders di oggetti poligonali.</span><span class="sxs-lookup"><span data-stu-id="a4f20-206">Pens are used to draw lines and theborders of polygonal objects.</span></span>

<span data-ttu-id="a4f20-207">Esempio: 3</span><span class="sxs-lookup"><span data-stu-id="a4f20-207">Example: 3</span></span>

<span data-ttu-id="a4f20-208">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-208">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-209">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="a4f20-209">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-210">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a4f20-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-212">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="a4f20-212">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\AdapterDescription\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-213">Indica la data e l'ora in cui è stato installato il driver video corrente.</span><span class="sxs-lookup"><span data-stu-id="a4f20-213">Indicates the date and time the current video driver was installed.</span></span>

<span data-ttu-id="a4f20-214">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-214">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-215">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="a4f20-215">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-216">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-218">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")</span><span class="sxs-lookup"><span data-stu-id="a4f20-218">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-219">Indica il numero corrente di pixel nella direzione orizzontale (asse X) dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a4f20-219">Indicates the current number of pixels in the horizontal direction (X axis) of the display.</span></span>

<span data-ttu-id="a4f20-220">Esempio: 1024</span><span class="sxs-lookup"><span data-stu-id="a4f20-220">Example: 1024</span></span>

<span data-ttu-id="a4f20-221">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-221">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-222">**InfFilename**</span><span class="sxs-lookup"><span data-stu-id="a4f20-222">**InfFilename**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-225">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="a4f20-225">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-226">Specifica il percorso del file. inf del driver video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-226">Specifies the path to the .inf file of the video driver.</span></span>

<span data-ttu-id="a4f20-227">Esempio: C: \\ Windows \\ system32 \\ drivers</span><span class="sxs-lookup"><span data-stu-id="a4f20-227">Example: C:\\Windows\\System32\\Drivers</span></span>

<span data-ttu-id="a4f20-228">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-228">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-229">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="a4f20-229">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-232">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="a4f20-232">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-233">Indica la sezione del file con estensione inf in cui si trovano le informazioni sul video Win32.</span><span class="sxs-lookup"><span data-stu-id="a4f20-233">Indicates the section of the .inf file where the Win32 video information resides.</span></span>

<span data-ttu-id="a4f20-234">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-234">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-235">**InstalledDisplayDrivers**</span><span class="sxs-lookup"><span data-stu-id="a4f20-235">**InstalledDisplayDrivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-238">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| drv")</span><span class="sxs-lookup"><span data-stu-id="a4f20-238">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\\\\Defaule\|drv")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-239">Indica il nome del driver video installato.</span><span class="sxs-lookup"><span data-stu-id="a4f20-239">Indicates the name of the installed video driver.</span></span>

<span data-ttu-id="a4f20-240">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-240">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-241">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="a4f20-241">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-244">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4f20-244">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-245">Indica il nome del produttore del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a4f20-245">Indicates the name of the manufacturer of the display device.</span></span>

<span data-ttu-id="a4f20-246">Esempio: NEC</span><span class="sxs-lookup"><span data-stu-id="a4f20-246">Example: NEC</span></span>

<span data-ttu-id="a4f20-247">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-247">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-248">**Monitoraggio**</span><span class="sxs-lookup"><span data-stu-id="a4f20-248">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-251">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \\ \\ MonitorPeripheral \\ \\ 0 \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="a4f20-251">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\Description\\\\System\\\\MonitorPeripheral\\\\0\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-252">Indica il nome del modello del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a4f20-252">Indicates the model name of the display device.</span></span>

<span data-ttu-id="a4f20-253">Esempio: NEC 5FGp</span><span class="sxs-lookup"><span data-stu-id="a4f20-253">Example: NEC 5FGp</span></span>

<span data-ttu-id="a4f20-254">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-254">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-255">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a4f20-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-258">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a4f20-258">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-259">Contiene un nome identificativo per la classe di configurazione video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-259">Contains an identifying name for the video configuration class.</span></span>

<span data-ttu-id="a4f20-260">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-260">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-261">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="a4f20-261">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-262">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-264">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")</span><span class="sxs-lookup"><span data-stu-id="a4f20-264">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSX")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-265">Indica il numero di pixel per pollice logico lungo l'asse X (direzione orizzontale) dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a4f20-265">Indicates the number of pixels per logical inch along the X axis (horizontal direction) of the display.</span></span>

<span data-ttu-id="a4f20-266">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-266">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-267">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="a4f20-267">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-268">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-270">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")</span><span class="sxs-lookup"><span data-stu-id="a4f20-270">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|LOGPIXELSY")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-271">Indica il numero di pixel per pollice logico lungo l'asse Y (direzione verticale) dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a4f20-271">Indicates the number of pixels per logical inch along the Y axis (vertical direction) of the display.</span></span>

<span data-ttu-id="a4f20-272">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-272">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-273">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a4f20-273">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-274">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-276">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")</span><span class="sxs-lookup"><span data-stu-id="a4f20-276">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VREFRESH")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-277">Indica la frequenza di aggiornamento della configurazione video.</span><span class="sxs-lookup"><span data-stu-id="a4f20-277">Indicates the refresh rate of the video configuration.</span></span> <span data-ttu-id="a4f20-278">Il valore 0 o 1 indica che è in uso una frequenza predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4f20-278">A value of 0 or 1 indicates a default rate is being used.</span></span>

<span data-ttu-id="a4f20-279">Esempio: 72</span><span class="sxs-lookup"><span data-stu-id="a4f20-279">Example: 72</span></span>

<span data-ttu-id="a4f20-280">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-280">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-281">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="a4f20-281">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-282">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-284">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. Interlaced")</span><span class="sxs-lookup"><span data-stu-id="a4f20-284">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\|Device0\|DefaultSettings.Interlaced")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-285">Indica se il dispositivo di visualizzazione è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="a4f20-285">Indicates whether the display device is interlaced.</span></span>

<span data-ttu-id="a4f20-286">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-286">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="a4f20-287">**Non interlacciato** ("non interlacciato")</span><span class="sxs-lookup"><span data-stu-id="a4f20-287">**Non Interlaced** ("Non Interlaced")</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="a4f20-288">**Interlacciato** ("interlacciato")</span><span class="sxs-lookup"><span data-stu-id="a4f20-288">**Interlaced** ("Interlaced")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a4f20-289">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="a4f20-289">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-290">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-292">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unità**](../wmisdk/standard-qualifiers.md) ("millimetri")</span><span class="sxs-lookup"><span data-stu-id="a4f20-292">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-293">Specifica l'altezza della schermata fisica.</span><span class="sxs-lookup"><span data-stu-id="a4f20-293">Specifies the height of the physical screen.</span></span>

<span data-ttu-id="a4f20-294">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-294">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-295">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="a4f20-295">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-296">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-298">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unità**](../wmisdk/standard-qualifiers.md) ("millimetri")</span><span class="sxs-lookup"><span data-stu-id="a4f20-298">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|HORZSIZE"), [**Units**](../wmisdk/standard-qualifiers.md) ("millimeters")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-299">Specifica la larghezza della schermata fisica.</span><span class="sxs-lookup"><span data-stu-id="a4f20-299">Specifies the width of the physical screen.</span></span>

<span data-ttu-id="a4f20-300">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-300">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-301">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="a4f20-301">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4f20-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-304">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a4f20-304">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-305">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="a4f20-305">Identifier by which the current object is known.</span></span>

<span data-ttu-id="a4f20-306">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-306">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-307">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="a4f20-307">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-308">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-310">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")</span><span class="sxs-lookup"><span data-stu-id="a4f20-310">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|SIZEPALETTE")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-311">Indicates il numero corrente di voci di indice dei colori riservate per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="a4f20-311">Iindicates the current number of color index entries reserved for system use.</span></span> <span data-ttu-id="a4f20-312">Questo valore è valido solo per le impostazioni di visualizzazione che usano una tavolozza indicizzata.</span><span class="sxs-lookup"><span data-stu-id="a4f20-312">This value is only valid for display settings that use an indexed palette .</span></span> <span data-ttu-id="a4f20-313">Le tavolozze indicizzate non vengono usate per le profondità dei colori maggiori di 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="a4f20-313">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="a4f20-314">Se la profondità del colore è maggiore di 8 bit per pixel, questo valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="a4f20-314">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="a4f20-315">Esempio: 20</span><span class="sxs-lookup"><span data-stu-id="a4f20-315">Example: 20</span></span>

<span data-ttu-id="a4f20-316">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-316">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f20-317">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="a4f20-317">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4f20-318">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4f20-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4f20-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4f20-320">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")</span><span class="sxs-lookup"><span data-stu-id="a4f20-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES")</span></span>
</dt> </dl>

<span data-ttu-id="a4f20-321">Indica il numero corrente di pixel nella direzione verticale (asse Y) dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a4f20-321">Indicates the current number of pixels in the vertical direction (Y axis) of the display.</span></span>

<span data-ttu-id="a4f20-322">Esempio: 768</span><span class="sxs-lookup"><span data-stu-id="a4f20-322">Example: 768</span></span>

<span data-ttu-id="a4f20-323">Questa proprietà è stata deprecata a favore di una o più proprietà corrispondenti contenute in [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).</span><span class="sxs-lookup"><span data-stu-id="a4f20-323">This property has been deprecated in favor of a corresponding property(s) contained in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md) and//or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4f20-324">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4f20-324">Requirements</span></span>



| <span data-ttu-id="a4f20-325">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f20-325">Requirement</span></span> | <span data-ttu-id="a4f20-326">Valore</span><span class="sxs-lookup"><span data-stu-id="a4f20-326">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f20-327">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4f20-327">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f20-328">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4f20-328">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4f20-329">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4f20-329">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f20-330">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4f20-330">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4f20-331">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4f20-331">Namespace</span></span><br/>                | <span data-ttu-id="a4f20-332">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a4f20-332">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4f20-333">MOF</span><span class="sxs-lookup"><span data-stu-id="a4f20-333">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4f20-334"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4f20-334"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4f20-335">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f20-335">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f20-336"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4f20-336"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f20-337">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4f20-337">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f20-338">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="a4f20-338">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

 
