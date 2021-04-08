---
description: La \_ classe WMI PrinterConfiguration Win32 rappresenta la configurazione per un dispositivo stampante. Sono incluse funzionalità quali la risoluzione, il colore, i tipi di carattere e l'orientamento.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Classe Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966261"
---
# <a name="win32_printerconfiguration-class"></a><span data-ttu-id="57c19-104">Win32 \_ PrinterConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="57c19-104">Win32\_PrinterConfiguration class</span></span>

<span data-ttu-id="57c19-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterConfiguration Win32** rappresenta la configurazione per un dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="57c19-105">The **Win32\_PrinterConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the configuration for a printer device.</span></span> <span data-ttu-id="57c19-106">Sono incluse funzionalità quali la risoluzione, il colore, i tipi di carattere e l'orientamento.</span><span class="sxs-lookup"><span data-stu-id="57c19-106">This includes capabilities such as resolution, color, fonts, and orientation.</span></span>

<span data-ttu-id="57c19-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="57c19-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="57c19-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="57c19-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57c19-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57c19-109">Syntax</span></span>

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a><span data-ttu-id="57c19-110">Members</span><span class="sxs-lookup"><span data-stu-id="57c19-110">Members</span></span>

<span data-ttu-id="57c19-111">La classe **Win32 \_ PrinterConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="57c19-111">The **Win32\_PrinterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="57c19-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57c19-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57c19-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57c19-113">Properties</span></span>

<span data-ttu-id="57c19-114">La classe **Win32 \_ PrinterConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="57c19-114">The **Win32\_PrinterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57c19-115">**BitsPerPel**</span><span class="sxs-lookup"><span data-stu-id="57c19-115">**BitsPerPel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-118">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57c19-118">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-119">Numero di bit utilizzati per rappresentare il colore in questa configurazione (bit per pixel).</span><span class="sxs-lookup"><span data-stu-id="57c19-119">Number of bits used to represent the color in this configuration (the bits per pixel).</span></span> <span data-ttu-id="57c19-120">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="57c19-120">This property is obsolete.</span></span> <span data-ttu-id="57c19-121">Usare invece le proprietà nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) per determinare il modo in cui viene rappresentato il colore.</span><span class="sxs-lookup"><span data-stu-id="57c19-121">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) classes to determine how color is represented.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-122">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="57c19-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-125">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="57c19-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-126">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="57c19-126">Short textual description of the current object.</span></span>

<span data-ttu-id="57c19-127">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="57c19-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="57c19-128">**Fascicola**</span><span class="sxs-lookup"><span data-stu-id="57c19-128">**Collate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57c19-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-131">Se **true**, le pagine stampate devono essere confrontate.</span><span class="sxs-lookup"><span data-stu-id="57c19-131">If **TRUE**, the pages that are printed should be collated.</span></span> <span data-ttu-id="57c19-132">Per eseguire l'ordinamento è necessario stampare l'intero documento prima di stampare la copia successiva, anziché stampare ogni pagina del documento per il numero di volte necessario.</span><span class="sxs-lookup"><span data-stu-id="57c19-132">To collate is to print out the entire document before printing the next copy, as opposed to printing out each page of the document the required number of times.</span></span>

<span data-ttu-id="57c19-133">Questa proprietà viene ignorata a meno che il driver della stampante non indichi il supporto per le regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="57c19-133">This property is ignored unless the printer driver indicates support for collation.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-134">**Colore**</span><span class="sxs-lookup"><span data-stu-id="57c19-134">**Color**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-137">Colore del documento.</span><span class="sxs-lookup"><span data-stu-id="57c19-137">Color of the document.</span></span> <span data-ttu-id="57c19-138">Alcune stampanti a colori hanno la possibilità di stampare usando il vero nero anziché una combinazione di cyan, magenta e Yellow (CMY).</span><span class="sxs-lookup"><span data-stu-id="57c19-138">Some color printers have the capability to print using true black instead of a combination of cyan, magenta, and yellow (CMY).</span></span> <span data-ttu-id="57c19-139">In genere viene creato un testo più scuro e più nitido per i documenti.</span><span class="sxs-lookup"><span data-stu-id="57c19-139">This usually creates darker and sharper text for documents.</span></span> <span data-ttu-id="57c19-140">Questa opzione è utile solo per le stampanti a colori che supportano la stampa true nero.</span><span class="sxs-lookup"><span data-stu-id="57c19-140">This option is only useful for color printers that support true black printing.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="57c19-141"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="57c19-141"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-142">Monocromatico (vero nero)</span><span class="sxs-lookup"><span data-stu-id="57c19-142">Monochrome (true black)</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="57c19-143"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-143"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-144">Colore</span><span class="sxs-lookup"><span data-stu-id="57c19-144">Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-145">**Copie**</span><span class="sxs-lookup"><span data-stu-id="57c19-145">**Copies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-148">Numero di copie da stampare.</span><span class="sxs-lookup"><span data-stu-id="57c19-148">Number of copies to be printed.</span></span> <span data-ttu-id="57c19-149">Il driver della stampante deve supportare la stampa di copie a più pagine.</span><span class="sxs-lookup"><span data-stu-id="57c19-149">The printer driver must support printing multi-page copies.</span></span>

<span data-ttu-id="57c19-150">Esempio: 2</span><span class="sxs-lookup"><span data-stu-id="57c19-150">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="57c19-151">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="57c19-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-154">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="57c19-154">Textual description of the current object.</span></span>

<span data-ttu-id="57c19-155">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="57c19-155">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="57c19-156">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="57c19-156">**DeviceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-159">Nome descrittivo della stampante.</span><span class="sxs-lookup"><span data-stu-id="57c19-159">Friendly name of the printer.</span></span> <span data-ttu-id="57c19-160">Questo nome è univoco per il tipo di stampante e può essere troncato a causa delle limitazioni della stringa da cui è derivato.</span><span class="sxs-lookup"><span data-stu-id="57c19-160">This name is unique to the type of printer and may be truncated because of the limitations of the string from which it is derived.</span></span>

<span data-ttu-id="57c19-161">Esempio: "PCL/HP LaserJet"</span><span class="sxs-lookup"><span data-stu-id="57c19-161">Example: "PCL/HP LaserJet"</span></span>

</dd> <dt>

<span data-ttu-id="57c19-162">**DisplayFlags**</span><span class="sxs-lookup"><span data-stu-id="57c19-162">**DisplayFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-165">Indica se il dispositivo di visualizzazione è colorato o monocromatico e se il tipo di analisi non è interlacciato o interlacciato.</span><span class="sxs-lookup"><span data-stu-id="57c19-165">Indicates whether the display device is color or monochrome and whether the type of scanning is noninterlaced or interlaced.</span></span> <span data-ttu-id="57c19-166">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="57c19-166">This property is obsolete.</span></span> <span data-ttu-id="57c19-167">Usare invece le proprietà di visualizzazione, ad esempio la proprietà **DisplayType** della classe **\_ DesktopMonitor Win32** .</span><span class="sxs-lookup"><span data-stu-id="57c19-167">Instead, use display properties such as the **DisplayType** property of the **Win32\_DesktopMonitor** class.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-168">**DisplayFrequency**</span><span class="sxs-lookup"><span data-stu-id="57c19-168">**DisplayFrequency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-169">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-171">Visualizza la frequenza di aggiornamento verticale.</span><span class="sxs-lookup"><span data-stu-id="57c19-171">Displays the vertical refresh rate.</span></span> <span data-ttu-id="57c19-172">La frequenza di aggiornamento per un monitoraggio è il numero di volte in cui lo schermo viene ridisegnato al secondo (frequenza).</span><span class="sxs-lookup"><span data-stu-id="57c19-172">The refresh rate for a monitor is the number of times the screen is redrawn per second (frequency).</span></span> <span data-ttu-id="57c19-173">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="57c19-173">This property is obsolete.</span></span> <span data-ttu-id="57c19-174">Usare invece le proprietà nella classe [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .</span><span class="sxs-lookup"><span data-stu-id="57c19-174">Instead, use properties in the [**Win32\_VideoController**](win32-videocontroller.md), [**Win32\_DesktopMonitor**](win32-desktopmonitor.md), or [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-175">**DitherType**</span><span class="sxs-lookup"><span data-stu-id="57c19-175">**DitherType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-176">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-178">Tipo di dithering della stampante.</span><span class="sxs-lookup"><span data-stu-id="57c19-178">Dither type of the printer.</span></span> <span data-ttu-id="57c19-179">Questa proprietà può assumere valori predefiniti da 1 a 5 o da 6 a 256 per i valori definiti dal driver.</span><span class="sxs-lookup"><span data-stu-id="57c19-179">This property can assume predefined values of 1 to 5, or driver-defined values from 6 to 256.</span></span> <span data-ttu-id="57c19-180">Il rethering dell'arte linea è un metodo speciale che produce bordi ben definiti tra le scalature di nero, bianco e grigio.</span><span class="sxs-lookup"><span data-stu-id="57c19-180">Line art dithering is a special dithering method that produces well defined borders between black, white, and gray scalings.</span></span> <span data-ttu-id="57c19-181">Non è adatta per le immagini che includono la graduazione continua in intensità e tonalità, ad esempio le fotografie analizzate.</span><span class="sxs-lookup"><span data-stu-id="57c19-181">It is not suitable for images that include continuous graduations in intensity and hue, such as scanned photographs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="57c19-182"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="57c19-182"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-183">Nessuna retinatura</span><span class="sxs-lookup"><span data-stu-id="57c19-183">No Dithering</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="57c19-184"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-184"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-185">Pennello grossolano</span><span class="sxs-lookup"><span data-stu-id="57c19-185">Coarse Brush</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="57c19-186"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="57c19-186"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-187">Pennello fine</span><span class="sxs-lookup"><span data-stu-id="57c19-187">Fine Brush</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="57c19-188"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="57c19-188"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-189">Linea artistica</span><span class="sxs-lookup"><span data-stu-id="57c19-189">Line Art</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="57c19-190"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="57c19-190"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-191">Gradazioni di grigio</span><span class="sxs-lookup"><span data-stu-id="57c19-191">Grayscale</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-192">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="57c19-192">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-195">Numero di versione del driver della stampante basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="57c19-195">Version number of the Windows-based printer driver.</span></span> <span data-ttu-id="57c19-196">I numeri di versione vengono creati e gestiti dal produttore del driver.</span><span class="sxs-lookup"><span data-stu-id="57c19-196">The version numbers are created and maintained by the driver manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-197">**Duplex**</span><span class="sxs-lookup"><span data-stu-id="57c19-197">**Duplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-198">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57c19-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-200">Se **true**, la stampa viene eseguita su entrambi i lati.</span><span class="sxs-lookup"><span data-stu-id="57c19-200">If **TRUE**, printing is done on both sides.</span></span> <span data-ttu-id="57c19-201">Se **false**, la stampa viene eseguita su un solo lato del supporto.</span><span class="sxs-lookup"><span data-stu-id="57c19-201">If **FALSE**, printing is done on only one side of the media.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-202">**Nomemodulo**</span><span class="sxs-lookup"><span data-stu-id="57c19-202">**FormName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-205">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="57c19-205">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-206">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="57c19-206">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-207">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-209">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (punti per pollice)</span><span class="sxs-lookup"><span data-stu-id="57c19-209">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-210">Risoluzione di stampa espressa in punti per pollice lungo l'asse x (larghezza) del processo di stampa (simile alla proprietà **XResolution** obsoleta).</span><span class="sxs-lookup"><span data-stu-id="57c19-210">Print resolution in dots per inch along the x-axis (width) of the print job (similar to the obsolete **XResolution** property).</span></span> <span data-ttu-id="57c19-211">Questo valore viene impostato solo quando la proprietà **PrintQuality** di questa classe è positiva.</span><span class="sxs-lookup"><span data-stu-id="57c19-211">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-212">**ICMIntent**</span><span class="sxs-lookup"><span data-stu-id="57c19-212">**ICMIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-213">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-213">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-215">Valore specifico di uno dei tre possibili metodi di corrispondenza dei colori (detti Intent) che devono essere utilizzati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="57c19-215">Specific value of one of the three possible color matching methods (called intents) that should be used by default.</span></span> <span data-ttu-id="57c19-216">Le applicazioni ICM stabiliscono gli Intent usando le funzioni ICM.</span><span class="sxs-lookup"><span data-stu-id="57c19-216">ICM applications establish intents by using the ICM functions.</span></span> <span data-ttu-id="57c19-217">Questa proprietà può assumere valori predefiniti compresi tra 1 e 3 o i valori definiti dal driver da 4 a 256.</span><span class="sxs-lookup"><span data-stu-id="57c19-217">This property can assume predefined values of 1 to 3, or driver-defined values from 4 to 256.</span></span> <span data-ttu-id="57c19-218">Le applicazioni non ICM possono utilizzare questo valore per determinare il modo in cui la stampante gestisce i processi di stampa dei colori.</span><span class="sxs-lookup"><span data-stu-id="57c19-218">Non-ICM applications can use this value to determine how the printer handles color printing jobs.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="57c19-219"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="57c19-219"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-220">Saturazione</span><span class="sxs-lookup"><span data-stu-id="57c19-220">Saturation</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="57c19-221"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-221"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-222">Si confronti</span><span class="sxs-lookup"><span data-stu-id="57c19-222">Contrast</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="57c19-223"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="57c19-223"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-224">Colore esatto</span><span class="sxs-lookup"><span data-stu-id="57c19-224">Exact Color</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-225">**ICMMethod**</span><span class="sxs-lookup"><span data-stu-id="57c19-225">**ICMMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-226">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-228">Modalità di gestione di ICM.</span><span class="sxs-lookup"><span data-stu-id="57c19-228">How ICM is handled.</span></span> <span data-ttu-id="57c19-229">Per un'applicazione non ICM, questa proprietà determina se ICM è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="57c19-229">For a non-ICM application, this property determines if ICM is enabled or disabled.</span></span> <span data-ttu-id="57c19-230">Per le applicazioni ICM, il sistema esamina questa proprietà per determinare quale parte del sistema del computer gestisce il supporto ICM.</span><span class="sxs-lookup"><span data-stu-id="57c19-230">For ICM applications, the system examines this property to determine which part of the computer system handles ICM support.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="57c19-231"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="57c19-231"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="57c19-232">Disabled</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="57c19-233"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-233"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-234">Windows</span><span class="sxs-lookup"><span data-stu-id="57c19-234">Windows</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="57c19-235"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="57c19-235"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-236">Driver di dispositivo</span><span class="sxs-lookup"><span data-stu-id="57c19-236">Device Driver</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="57c19-237"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="57c19-237"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-238">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="57c19-238">Device</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-239">**LogPixels**</span><span class="sxs-lookup"><span data-stu-id="57c19-239">**LogPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-240">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-240">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-242">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57c19-242">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-243">Numero di pixel per pollice logico.</span><span class="sxs-lookup"><span data-stu-id="57c19-243">Number of pixels per logical inch.</span></span> <span data-ttu-id="57c19-244">Questa proprietà obsoleta è valida solo con i dispositivi che funzionano con pixel, che esclude i dispositivi come le stampanti.</span><span class="sxs-lookup"><span data-stu-id="57c19-244">This obsolete property is valid only with devices that work with pixels, which excludes devices such as printers.</span></span> <span data-ttu-id="57c19-245">Non esiste alcun valore sostitutivo applicabile alle stampanti.</span><span class="sxs-lookup"><span data-stu-id="57c19-245">There is no replacement value that applies to printers.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-246">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="57c19-246">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-247">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-249">Tipo di supporto su cui stampa la stampante.</span><span class="sxs-lookup"><span data-stu-id="57c19-249">Type of media on which the printer prints.</span></span> <span data-ttu-id="57c19-250">La proprietà può essere impostata su un valore predefinito o su un valore definito dal driver maggiore o uguale a 256.</span><span class="sxs-lookup"><span data-stu-id="57c19-250">The property can be set to a predefined value or a driver-defined value greater than or equal to 256.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="57c19-251"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="57c19-251"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-252">Standard</span><span class="sxs-lookup"><span data-stu-id="57c19-252">Standard</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="57c19-253"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-253"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-254">Trasparenza</span><span class="sxs-lookup"><span data-stu-id="57c19-254">Transparency</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="57c19-255"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="57c19-255"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-256">Lucido</span><span class="sxs-lookup"><span data-stu-id="57c19-256">Glossy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-257">**Nome**</span><span class="sxs-lookup"><span data-stu-id="57c19-257">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-260">Qualificatori: [**Key**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="57c19-260">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-261">Nome della stampante a cui è associata questa configurazione.</span><span class="sxs-lookup"><span data-stu-id="57c19-261">Name of the printer with which this configuration is associated.</span></span> <span data-ttu-id="57c19-262">Questo valore corrisponde alla proprietà **Name** dell'istanza della [**\_ stampante Win32**](win32-printer.md) associata.</span><span class="sxs-lookup"><span data-stu-id="57c19-262">This value matches the **Name** property of the associated [**Win32\_Printer**](win32-printer.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-263">**Orientamento**</span><span class="sxs-lookup"><span data-stu-id="57c19-263">**Orientation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-264">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-266">Orientamento di stampa del documento.</span><span class="sxs-lookup"><span data-stu-id="57c19-266">Printing orientation of the paper.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="57c19-267"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="57c19-267"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-268">Verticale</span><span class="sxs-lookup"><span data-stu-id="57c19-268">Portrait</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="57c19-269"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-269"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-270">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="57c19-270">Landscape</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-271">**PaperLength**</span><span class="sxs-lookup"><span data-stu-id="57c19-271">**PaperLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-272">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-274">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (decimi di millimetro)</span><span class="sxs-lookup"><span data-stu-id="57c19-274">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-275">Lunghezza del documento.</span><span class="sxs-lookup"><span data-stu-id="57c19-275">Length of the paper.</span></span> <span data-ttu-id="57c19-276">Per determinare le dimensioni del foglio in pollici, dividere il valore per 254.</span><span class="sxs-lookup"><span data-stu-id="57c19-276">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="57c19-277">Esempio: 2794</span><span class="sxs-lookup"><span data-stu-id="57c19-277">Example: 2794</span></span>

</dd> <dt>

<span data-ttu-id="57c19-278">**PaperSize**</span><span class="sxs-lookup"><span data-stu-id="57c19-278">**PaperSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-281">Dimensioni del foglio.</span><span class="sxs-lookup"><span data-stu-id="57c19-281">Size of the paper.</span></span> <span data-ttu-id="57c19-282">Le dimensioni possibili si trovano nella proprietà **PaperSizesSupported** della classe [**\_ Printer Win32**](win32-printer.md) associata.</span><span class="sxs-lookup"><span data-stu-id="57c19-282">The possible sizes are found in the **PaperSizesSupported** property of the associated [**Win32\_Printer**](win32-printer.md) class.</span></span>

<span data-ttu-id="57c19-283">Esempio: "a4 o Letter".</span><span class="sxs-lookup"><span data-stu-id="57c19-283">Example: "A4 or Letter".</span></span>

</dd> <dt>

<span data-ttu-id="57c19-284">**PaperWidth**</span><span class="sxs-lookup"><span data-stu-id="57c19-284">**PaperWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-287">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (decimi di millimetro)</span><span class="sxs-lookup"><span data-stu-id="57c19-287">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Tenths of a millimeter)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-288">Larghezza del foglio.</span><span class="sxs-lookup"><span data-stu-id="57c19-288">Width of the paper.</span></span> <span data-ttu-id="57c19-289">Per determinare le dimensioni del foglio in pollici, dividere il valore per 254.</span><span class="sxs-lookup"><span data-stu-id="57c19-289">To determine the size of the paper in inches, divide this value by 254.</span></span>

<span data-ttu-id="57c19-290">Esempio: 2159</span><span class="sxs-lookup"><span data-stu-id="57c19-290">Example: 2159</span></span>

</dd> <dt>

<span data-ttu-id="57c19-291">**PelsHeight**</span><span class="sxs-lookup"><span data-stu-id="57c19-291">**PelsHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-292">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-294">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57c19-294">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-295">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="57c19-295">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-296">**PelsWidth**</span><span class="sxs-lookup"><span data-stu-id="57c19-296">**PelsWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-297">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-299">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57c19-299">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-300">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="57c19-300">This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-301">**PrintQuality**</span><span class="sxs-lookup"><span data-stu-id="57c19-301">**PrintQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-302">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-304">Uno dei quattro livelli di qualità del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="57c19-304">One of four quality levels of the print job.</span></span> <span data-ttu-id="57c19-305">Se viene specificato un valore positivo, la qualità viene misurata in punti per pollice.</span><span class="sxs-lookup"><span data-stu-id="57c19-305">If a positive value is specified, the quality is measured in dots per inch.</span></span>

<dt>

<span id="-1"></span>

<span data-ttu-id="57c19-306"><span id="-1"></span>**-1**</span><span class="sxs-lookup"><span data-stu-id="57c19-306"><span id="-1"></span>**-1**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-307">Bozza</span><span class="sxs-lookup"><span data-stu-id="57c19-307">Draft</span></span>

</dd> <dt>

<span id="-2"></span>

<span data-ttu-id="57c19-308"><span id="-2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="57c19-308"><span id="-2"></span>**-2**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-309">Basso</span><span class="sxs-lookup"><span data-stu-id="57c19-309">Low</span></span>

</dd> <dt>

<span id="-3"></span>

<span data-ttu-id="57c19-310"><span id="-3"></span>**-3**</span><span class="sxs-lookup"><span data-stu-id="57c19-310"><span id="-3"></span>**-3**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-311">Medio</span><span class="sxs-lookup"><span data-stu-id="57c19-311">Medium</span></span>

</dd> <dt>

<span id="-4"></span>

<span data-ttu-id="57c19-312"><span id="-4"></span>**-4**</span><span class="sxs-lookup"><span data-stu-id="57c19-312"><span id="-4"></span>**-4**</span></span>


</dt> <dd>

<span data-ttu-id="57c19-313">Alto</span><span class="sxs-lookup"><span data-stu-id="57c19-313">High</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-314">**Ridimensiona**</span><span class="sxs-lookup"><span data-stu-id="57c19-314">**Scale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-317">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (percentuale)</span><span class="sxs-lookup"><span data-stu-id="57c19-317">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (Percent)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-318">Fattore di ridimensionamento dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="57c19-318">Factor by which the printed output is to be scaled.</span></span> <span data-ttu-id="57c19-319">Una scala 75, ad esempio, riduce l'output di stampa a 3/4 l'altezza e la larghezza originali.</span><span class="sxs-lookup"><span data-stu-id="57c19-319">For example, a scale of 75 reduces the print output to 3/4 its original height and width.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-320">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="57c19-320">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57c19-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-323">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="57c19-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-324">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="57c19-324">Identifier by which the current object is known.</span></span>

<span data-ttu-id="57c19-325">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="57c19-325">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="57c19-326">**SpecificationVersion**</span><span class="sxs-lookup"><span data-stu-id="57c19-326">**SpecificationVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-327">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-329">Numero di versione dei dati di inizializzazione per il dispositivo associato alla stampante basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="57c19-329">Version number of the initialization data for the device associated with the Windows-based printer.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-330">**TTOption**</span><span class="sxs-lookup"><span data-stu-id="57c19-330">**TTOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-331">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57c19-333">Indica la modalità di stampa di tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="57c19-333">Indicates how TrueType fonts should be printed.</span></span>

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span data-ttu-id="57c19-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span><span class="sxs-lookup"><span data-stu-id="57c19-334"><span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)</span></span>


</dt> <dd>

<span data-ttu-id="57c19-335">Stampa i tipi di carattere TrueType come grafici.</span><span class="sxs-lookup"><span data-stu-id="57c19-335">Prints TrueType fonts as graphics.</span></span> <span data-ttu-id="57c19-336">Si tratta dell'azione predefinita per le stampanti a matrice di punti.</span><span class="sxs-lookup"><span data-stu-id="57c19-336">This is the default action for dot-matrix printers.</span></span>

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span data-ttu-id="57c19-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span><span class="sxs-lookup"><span data-stu-id="57c19-337"><span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)</span></span>


</dt> <dd>

<span data-ttu-id="57c19-338">Scarica i tipi di carattere TrueType come caratteri soft.</span><span class="sxs-lookup"><span data-stu-id="57c19-338">Downloads TrueType fonts as soft fonts.</span></span> <span data-ttu-id="57c19-339">Si tratta dell'azione predefinita per le stampanti che utilizzano il linguaggio di controllo della stampante (PCL).</span><span class="sxs-lookup"><span data-stu-id="57c19-339">This is the default action for printers that use the Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span data-ttu-id="57c19-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Sostituisci** (3)</span><span class="sxs-lookup"><span data-stu-id="57c19-340"><span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substitute** (3)</span></span>


</dt> <dd>

<span data-ttu-id="57c19-341">Sostituisce i tipi di carattere del dispositivo per i tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="57c19-341">Substitutes device fonts for TrueType fonts.</span></span> <span data-ttu-id="57c19-342">Si tratta dell'azione predefinita per le stampanti PostScript.</span><span class="sxs-lookup"><span data-stu-id="57c19-342">This is the default action for PostScript printers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57c19-343">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="57c19-343">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-344">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-346">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (punti per pollice)</span><span class="sxs-lookup"><span data-stu-id="57c19-346">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) (dots per inch)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-347">Risoluzione di stampa lungo l'asse y (altezza) del processo di stampa, simile alla proprietà **YResolution** obsoleta.</span><span class="sxs-lookup"><span data-stu-id="57c19-347">Print resolution along the y-axis (height) of the print job (similar to the obsolete **YResolution** property).</span></span> <span data-ttu-id="57c19-348">Questo valore viene impostato solo quando la proprietà **PrintQuality** di questa classe è positiva.</span><span class="sxs-lookup"><span data-stu-id="57c19-348">This value is only set when the **PrintQuality** property of this class is positive.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-349">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="57c19-349">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-350">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-350">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-352">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57c19-352">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-353">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="57c19-353">This property is obsolete.</span></span> <span data-ttu-id="57c19-354">In alternativa, usare la proprietà **HorizontalResolution** .</span><span class="sxs-lookup"><span data-stu-id="57c19-354">Use the **HorizontalResolution** property instead.</span></span>

</dd> <dt>

<span data-ttu-id="57c19-355">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="57c19-355">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57c19-356">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57c19-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57c19-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57c19-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57c19-358">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="57c19-358">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="57c19-359">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="57c19-359">This property is obsolete.</span></span> <span data-ttu-id="57c19-360">In alternativa, usare la proprietà **VerticalResolution** .</span><span class="sxs-lookup"><span data-stu-id="57c19-360">Use the **VerticalResolution** property instead.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57c19-361">Commenti</span><span class="sxs-lookup"><span data-stu-id="57c19-361">Remarks</span></span>

<span data-ttu-id="57c19-362">La classe **Win32 \_ PrinterConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="57c19-362">The **Win32\_PrinterConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="57c19-363">**Overview**</span><span class="sxs-lookup"><span data-stu-id="57c19-363">**Overview**</span></span>

<span data-ttu-id="57c19-364">Prima di poter determinare come distribuire e utilizzare al meglio le risorse di stampa, è necessario disporre di una conoscenza approfondita di tali risorse.</span><span class="sxs-lookup"><span data-stu-id="57c19-364">Before you can determine how to best distribute and use your printing resources, you must have a detailed knowledge of those resources.</span></span> <span data-ttu-id="57c19-365">Ad esempio, il reparto A può avere solo tre stampanti rispetto a cinque stampanti nel reparto B. Tuttavia, se le stampanti nel reparto A possono stampare 20 pagine al minuto e le stampanti nel reparto B possono stampare solo 5 pagine al minuto, gli utenti nel reparto A hanno effettivamente una maggiore capacità di stampa.</span><span class="sxs-lookup"><span data-stu-id="57c19-365">For example, Department A might have only three printers compared with five printers in Department B. However, if the printers in Department A can print 20 pages per minute and the printers in Department B can print only 5 pages per minute, users in Department A actually have more printing capacity.</span></span> <span data-ttu-id="57c19-366">Se non si conoscono le funzionalità dettagliate di queste stampanti, è possibile che si concluda erroneamente che un reparto A è breve sulla capacità di stampa e quindi si acquistano altre stampanti che finiscono inutilizzate.</span><span class="sxs-lookup"><span data-stu-id="57c19-366">Without knowing the detailed capabilities of these printers, you might erroneously conclude that Department A is short on printing capacity and thus purchase additional printers that end up going unused.</span></span>

<span data-ttu-id="57c19-367">WMI include due classi, [**\_ Printer Win32**](win32-printer.md) e **Win32 \_ PrinterConfiguration**, che possono essere utilizzate per restituire informazioni dettagliate su tutte le stampanti installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="57c19-367">WMI includes two classes, [**Win32\_Printer**](win32-printer.md) and **Win32\_PrinterConfiguration**, which can be used to return detailed information about all the printers installed on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="57c19-368">Esempio</span><span class="sxs-lookup"><span data-stu-id="57c19-368">Examples</span></span>

<span data-ttu-id="57c19-369">Nell'esempio di codice seguente vengono recuperate le informazioni sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="57c19-369">The following code sample retrieves printer information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a><span data-ttu-id="57c19-370">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57c19-370">Requirements</span></span>



| <span data-ttu-id="57c19-371">Requisito</span><span class="sxs-lookup"><span data-stu-id="57c19-371">Requirement</span></span> | <span data-ttu-id="57c19-372">Valore</span><span class="sxs-lookup"><span data-stu-id="57c19-372">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="57c19-373">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57c19-373">Minimum supported client</span></span><br/> | <span data-ttu-id="57c19-374">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57c19-374">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="57c19-375">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57c19-375">Minimum supported server</span></span><br/> | <span data-ttu-id="57c19-376">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57c19-376">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="57c19-377">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57c19-377">Namespace</span></span><br/>                | <span data-ttu-id="57c19-378">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="57c19-378">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="57c19-379">MOF</span><span class="sxs-lookup"><span data-stu-id="57c19-379">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57c19-380"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57c19-380"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="57c19-381">DLL</span><span class="sxs-lookup"><span data-stu-id="57c19-381">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57c19-382"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57c19-382"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="57c19-383">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57c19-383">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57c19-384">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="57c19-384">**CIM\_Setting**</span></span>](./cim-setting.md)
</dt> <dt>

[<span data-ttu-id="57c19-385">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="57c19-385">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
