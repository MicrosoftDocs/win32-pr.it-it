---
description: La \_ classe WMI DisplayControllerConfiguration Win32 rappresenta le informazioni di configurazione della scheda video di un sistema di computer che esegue Windows.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Classe Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127335"
---
# <a name="win32_displaycontrollerconfiguration-class"></a><span data-ttu-id="e935c-103">Win32 \_ DisplayControllerConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="e935c-103">Win32\_DisplayControllerConfiguration class</span></span>

<span data-ttu-id="e935c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DisplayControllerConfiguration Win32** rappresenta le informazioni di configurazione della scheda video di un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="e935c-104">The **Win32\_DisplayControllerConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the video adapter configuration information of a computer system running Windows.</span></span>

<span data-ttu-id="e935c-105">Questa classe è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="e935c-105">This class is obsolete.</span></span> <span data-ttu-id="e935c-106">Al posto di questa classe, è necessario usare le proprietà nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="e935c-106">In place of this class, you should use the properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), and [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes.</span></span>

<span data-ttu-id="e935c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e935c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e935c-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e935c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e935c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e935c-109">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a><span data-ttu-id="e935c-110">Members</span><span class="sxs-lookup"><span data-stu-id="e935c-110">Members</span></span>

<span data-ttu-id="e935c-111">La classe **Win32 \_ DisplayControllerConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e935c-111">The **Win32\_DisplayControllerConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="e935c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e935c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e935c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e935c-113">Properties</span></span>

<span data-ttu-id="e935c-114">La classe **Win32 \_ DisplayControllerConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e935c-114">The **Win32\_DisplayControllerConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e935c-115">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="e935c-115">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-118">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")</span><span class="sxs-lookup"><span data-stu-id="e935c-118">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|BITSPIXEL")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-119">Il numero di bit utilizzato per rappresentare il colore in questa configurazione o i bit in ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="e935c-119">Either the number of bits used to represent the color in this configuration, or the bits in each pixel.</span></span>

<span data-ttu-id="e935c-120">Esempio: 8</span><span class="sxs-lookup"><span data-stu-id="e935c-120">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="e935c-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e935c-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e935c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e935c-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e935c-125">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="e935c-125">Short textual description of the current object.</span></span>

<span data-ttu-id="e935c-126">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e935c-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e935c-127">**ColorPlanes**</span><span class="sxs-lookup"><span data-stu-id="e935c-127">**ColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-130">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| Planes")</span><span class="sxs-lookup"><span data-stu-id="e935c-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|PLANES")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-131">Numero corrente di piani di colore utilizzati nella configurazione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e935c-131">Current number of color planes used in the display configuration.</span></span> <span data-ttu-id="e935c-132">Un piano colori rappresenta un altro modo per rappresentare i colori pixel.</span><span class="sxs-lookup"><span data-stu-id="e935c-132">A color plane is another way to represent pixel colors.</span></span> <span data-ttu-id="e935c-133">Anziché assegnare un singolo valore RGB a ogni pixel, i piani dei colori separano il grafico in ogni componente del colore primario (rosso, verde, blu) e li archivia nei propri piani.</span><span class="sxs-lookup"><span data-stu-id="e935c-133">Instead of assigning a single RGB value to each pixel, color planes separate the graphic into each of the primary color components (red, green, blue), and stores them in their own planes.</span></span> <span data-ttu-id="e935c-134">Questo consente una maggiore profondità dei colori nei sistemi video a 8 e 16 bit.</span><span class="sxs-lookup"><span data-stu-id="e935c-134">This allows for greater color depths on 8-bit and 16-bit video systems.</span></span> <span data-ttu-id="e935c-135">I sistemi grafici presenti hanno bitwidth dimensioni sufficienti per archiviare le informazioni relative alla profondità dei colori, vale a dire che è necessario solo un piano di colore.</span><span class="sxs-lookup"><span data-stu-id="e935c-135">Present graphics systems have the bitwidth large enough to store color depth information, meaning only one color plane is needed.</span></span>

<span data-ttu-id="e935c-136">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="e935c-136">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="e935c-137">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e935c-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e935c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e935c-140">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="e935c-140">Textual description of the current object.</span></span>

<span data-ttu-id="e935c-141">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e935c-141">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e935c-142">**DeviceEntriesInAColorTable**</span><span class="sxs-lookup"><span data-stu-id="e935c-142">**DeviceEntriesInAColorTable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-145">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")</span><span class="sxs-lookup"><span data-stu-id="e935c-145">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMCOLORS")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-146">Numero di indici colori in una tabella dei colori di un dispositivo di visualizzazione (se il dispositivo ha una profondità di colore di non più di 8 bit per pixel).</span><span class="sxs-lookup"><span data-stu-id="e935c-146">Number of color indexes in a color table of a display device (if the device has a color depth of no more than 8 bits per pixel).</span></span> <span data-ttu-id="e935c-147">Per i dispositivi con profondità dei colori maggiori, viene restituito-1.</span><span class="sxs-lookup"><span data-stu-id="e935c-147">For devices with greater color depths, -1 is returned.</span></span>

<span data-ttu-id="e935c-148">Esempio: 256</span><span class="sxs-lookup"><span data-stu-id="e935c-148">Example: 256</span></span>

</dd> <dt>

<span data-ttu-id="e935c-149">**DeviceSpecificPens**</span><span class="sxs-lookup"><span data-stu-id="e935c-149">**DeviceSpecificPens**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-152">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")</span><span class="sxs-lookup"><span data-stu-id="e935c-152">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMPENS")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-153">Numero corrente di penne specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e935c-153">Current number of device-specific pens.</span></span> <span data-ttu-id="e935c-154">Il valore 0xFFFFFFFF indica che il dispositivo non supporta le penne.</span><span class="sxs-lookup"><span data-stu-id="e935c-154">A value of 0xFFFFFFFF means the device does not support pens.</span></span> <span data-ttu-id="e935c-155">Le penne sono proprietà logiche che possono essere assegnate dal controller di visualizzazione per visualizzare i dispositivi e vengono usate per creare linee, bordi di poligoni e testo.</span><span class="sxs-lookup"><span data-stu-id="e935c-155">Pens are logical properties that can be assigned by the display controller to display devices, and are used to draw lines, borders of polygons, and text.</span></span>

<span data-ttu-id="e935c-156">Esempio: 3</span><span class="sxs-lookup"><span data-stu-id="e935c-156">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="e935c-157">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="e935c-157">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-158">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-160">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="e935c-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-161">Numero corrente di pixel nella direzione orizzontale (asse x) dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e935c-161">Current number of pixels in the horizontal direction (x-axis) of the display.</span></span>

<span data-ttu-id="e935c-162">Esempio: 1024</span><span class="sxs-lookup"><span data-stu-id="e935c-162">Example: 1024</span></span>

</dd> <dt>

<span data-ttu-id="e935c-163">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e935c-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e935c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-166">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e935c-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-167">Nome dell'adapter utilizzato in questa configurazione.</span><span class="sxs-lookup"><span data-stu-id="e935c-167">Name of the adapter used in this configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e935c-168">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="e935c-168">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-169">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e935c-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-171">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="e935c-171">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|HORZRESVREFRESH"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-172">Frequenza di aggiornamento della scheda video.</span><span class="sxs-lookup"><span data-stu-id="e935c-172">Refresh rate of the video adapter.</span></span> <span data-ttu-id="e935c-173">Il valore 0 (zero) o 1 (uno) indica che è in uso una frequenza predefinita.</span><span class="sxs-lookup"><span data-stu-id="e935c-173">A value of 0 (zero) or 1 (one) indicates a default rate is being used.</span></span> <span data-ttu-id="e935c-174">Il valore-1 indica che viene utilizzata una velocità ottimale.</span><span class="sxs-lookup"><span data-stu-id="e935c-174">A value of -1 indicates that an optimal rate is being used.</span></span>

<span data-ttu-id="e935c-175">Esempio: 72</span><span class="sxs-lookup"><span data-stu-id="e935c-175">Example: 72</span></span>

</dd> <dt>

<span data-ttu-id="e935c-176">**ReservedSystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="e935c-176">**ReservedSystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-179">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="e935c-179">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-180">Numero corrente di voci di indice dei colori riservate per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="e935c-180">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="e935c-181">Questo valore è valido solo per le impostazioni di visualizzazione che usano una tavolozza indicizzata.</span><span class="sxs-lookup"><span data-stu-id="e935c-181">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="e935c-182">Le tavolozze indicizzate non vengono usate per le profondità dei colori maggiori di 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="e935c-182">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="e935c-183">Se la profondità del colore è maggiore di 8 bit per pixel, questo valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e935c-183">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="e935c-184">Esempio: 20</span><span class="sxs-lookup"><span data-stu-id="e935c-184">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="e935c-185">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e935c-185">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e935c-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-188">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e935c-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e935c-189">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="e935c-189">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e935c-190">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e935c-190">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e935c-191">**SystemPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="e935c-191">**SystemPaletteEntries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-192">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-194">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")</span><span class="sxs-lookup"><span data-stu-id="e935c-194">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|NUMRESERVED")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-195">Numero corrente di voci di indice dei colori riservate per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="e935c-195">Current number of color index entries reserved for system use.</span></span> <span data-ttu-id="e935c-196">Questo valore è valido solo per le impostazioni di visualizzazione che usano una tavolozza indicizzata.</span><span class="sxs-lookup"><span data-stu-id="e935c-196">This value is only valid for display settings that use an indexed palette.</span></span> <span data-ttu-id="e935c-197">Le tavolozze indicizzate non vengono usate per le profondità dei colori maggiori di 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="e935c-197">Indexed palettes are not used for color depths greater than 8 bits per pixel.</span></span> <span data-ttu-id="e935c-198">Se la profondità del colore è maggiore di 8 bit per pixel, questo valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e935c-198">If the color depth is more than 8 bits per pixel, this value is set to **NULL**.</span></span>

<span data-ttu-id="e935c-199">Esempio: 20</span><span class="sxs-lookup"><span data-stu-id="e935c-199">Example: 20</span></span>

</dd> <dt>

<span data-ttu-id="e935c-200">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="e935c-200">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e935c-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-203">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span><span class="sxs-lookup"><span data-stu-id="e935c-203">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)\|VERTRES"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-204">Numero corrente di pixel nella direzione verticale (asse y) dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e935c-204">Current number of pixels in the vertical direction (y-axis) of the display.</span></span>

<span data-ttu-id="e935c-205">Esempio: 768</span><span class="sxs-lookup"><span data-stu-id="e935c-205">Example: 768</span></span>

</dd> <dt>

<span data-ttu-id="e935c-206">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="e935c-206">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e935c-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e935c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e935c-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e935c-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e935c-209">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="e935c-209">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e935c-210">Descrizione leggibile dall'utente della risoluzione dello schermo e dell'impostazione del colore correnti della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e935c-210">User-readable description of the current screen resolution and color setting of the display.</span></span>

<span data-ttu-id="e935c-211">Esempio: "1024 768 con colori 256"</span><span class="sxs-lookup"><span data-stu-id="e935c-211">Example: "1024   768 with 256 colors"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e935c-212">Commenti</span><span class="sxs-lookup"><span data-stu-id="e935c-212">Remarks</span></span>

<span data-ttu-id="e935c-213">La classe **Win32 \_ DisplayControllerConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e935c-213">The **Win32\_DisplayControllerConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e935c-214">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e935c-214">Requirements</span></span>



| <span data-ttu-id="e935c-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="e935c-215">Requirement</span></span> | <span data-ttu-id="e935c-216">Valore</span><span class="sxs-lookup"><span data-stu-id="e935c-216">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e935c-217">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e935c-217">Minimum supported client</span></span><br/> | <span data-ttu-id="e935c-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e935c-218">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e935c-219">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e935c-219">Minimum supported server</span></span><br/> | <span data-ttu-id="e935c-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e935c-220">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e935c-221">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e935c-221">Namespace</span></span><br/>                | <span data-ttu-id="e935c-222">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e935c-222">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e935c-223">MOF</span><span class="sxs-lookup"><span data-stu-id="e935c-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e935c-224"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e935c-224"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e935c-225">DLL</span><span class="sxs-lookup"><span data-stu-id="e935c-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e935c-226"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e935c-226"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e935c-227">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e935c-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e935c-228">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="e935c-228">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="e935c-229">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e935c-229">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

