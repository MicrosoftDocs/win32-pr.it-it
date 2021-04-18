---
description: I dispositivi hardware Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema di Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Costanti della proprietà del dispositivo dello scanner (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307288"
---
# <a name="scanner-device-property-constants"></a><span data-ttu-id="b3aa3-103">Costanti della proprietà del dispositivo dello scanner</span><span class="sxs-lookup"><span data-stu-id="b3aa3-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="b3aa3-104">I dispositivi hardware Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="b3aa3-105">Per altre informazioni, vedere [**costanti della proprietà del dispositivo comune**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="b3aa3-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="b3aa3-106">Le seguenti costanti della proprietà del dispositivo, con le relative stringhe associate, sono specifiche per gli scanner di immagini digitali.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="b3aa3-107">Il prefisso "WIA \_ DPS \_ " indica una proprietà del dispositivo per i dispositivi dello scanner e rappresenta la convenzione di denominazione usata in C/C++.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="b3aa3-108">Per finalità di scripting queste costanti usano il prefisso "ScannerDevice" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="b3aa3-109">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b3aa3-110">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b3aa3-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b3aa3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="b3aa3-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-113">Questa proprietà è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="b3aa3-114">Contiene un identificatore di istanza di funzione univoco per un dispositivo scanner di servizi Web.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="b3aa3-115">Questo identificatore rappresenta il servizio Web sul dispositivo dello scanner con cui comunica il mini driver WIA.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="b3aa3-116">Non è necessario che venga creato alcun presupposto sul formato di questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="b3aa3-117">Il mini driver WIA crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="b3aa3-118">Le applicazioni WIA possono usare il valore di WIA_DPS_DEVICE_ID per trovare, usando l'API di individuazione delle funzioni, l'oggetto istanza della funzione che rappresenta il dispositivo di scanner dei servizi Web usato nella sessione WIA 2,0 corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="b3aa3-119">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="b3aa3-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b3aa3-121">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="b3aa3-122">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="b3aa3-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b3aa3-124">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="b3aa3-125">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="b3aa3-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b3aa3-127">Contiene le funzionalità dello scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="b3aa3-128">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="b3aa3-129">Un'applicazione legge questa proprietà per determinare se lo scanner ha un piano, un alimentatore di documenti o un duplex installato.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="b3aa3-130">Questa proprietà viene inoltre utilizzata per definire ulteriormente le funzionalità installate.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="b3aa3-131">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="b3aa3-132">Nella tabella seguente vengono descritte le costanti valide solo per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-133">Flags</span><span class="sxs-lookup"><span data-stu-id="b3aa3-133">Flags</span></span></th>
<th><span data-ttu-id="b3aa3-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="b3aa3-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="b3aa3-136">Per lo scanner è installato un gestore di documenti automatico.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-137">Nella tabella seguente vengono descritte le costanti valide solo per Windows 7 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-138">Flags</span><span class="sxs-lookup"><span data-stu-id="b3aa3-138">Flags</span></span></th>
<th><span data-ttu-id="b3aa3-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="b3aa3-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="b3aa3-141">Il dispositivo supporta la configurazione avanzata di analisi duplex.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="b3aa3-142">Usare WIA_IPS_DUPLEX_SETTINGS per passare dall'uso di configurazioni duplex di base e avanzate.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="b3aa3-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="b3aa3-144">Lo scanner è in grado di rilevare quando la scheda trasparenza/film è pronta per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="b3aa3-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="b3aa3-146">Lo scanner è in grado di rilevare quando sono presenti documenti nella risorsa di archiviazione interna.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="b3aa3-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="b3aa3-148">Lo scanner è dotato di una scheda di analisi trasparente/film.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-149">STOR</span><span class="sxs-lookup"><span data-stu-id="b3aa3-149">STOR</span></span></td>
<td><span data-ttu-id="b3aa3-150">Lo scanner è dotato di un dispositivo di archiviazione immagini interno.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-151">Nella tabella seguente vengono descritte le costanti valide per Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-152">Flags</span><span class="sxs-lookup"><span data-stu-id="b3aa3-152">Flags</span></span></th>
<th><span data-ttu-id="b3aa3-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="b3aa3-155">Lo scanner è in grado di rilevare un documento nel feeder.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="b3aa3-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="b3aa3-157">Lo scanner è in grado di rilevare un documento sulla piastra piana.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="b3aa3-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="b3aa3-159">Lo scanner è in grado di rilevare un documento nel Feeder solo analizzando.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-160">DUP</span><span class="sxs-lookup"><span data-stu-id="b3aa3-160">DUP</span></span></td>
<td><span data-ttu-id="b3aa3-161">Lo scanner ha un duplex.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-162">FEED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-162">FEED</span></span></td>
<td><span data-ttu-id="b3aa3-163">Per lo scanner è installato un gestore di documenti automatico.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-164">PIATTO</span><span class="sxs-lookup"><span data-stu-id="b3aa3-164">FLAT</span></span></td>
<td><span data-ttu-id="b3aa3-165">Lo scanner ha una piastra piana.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-166">Nella tabella seguente vengono descritte le costanti valide solo per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="b3aa3-167">Questi valori sono stati deprecati per Windows 7 e Windows Vista e non devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-168">Flags</span><span class="sxs-lookup"><span data-stu-id="b3aa3-168">Flags</span></span></th>
<th><span data-ttu-id="b3aa3-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="b3aa3-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="b3aa3-171">Lo scanner è in grado di rilevare una richiesta di analisi duplex da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="b3aa3-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="b3aa3-173">Lo scanner è in grado di stabilire quando è installato il duplex.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="b3aa3-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="b3aa3-175">Lo scanner è in grado di stabilire quando viene installato il feeder automatico del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="b3aa3-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-177">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-178">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-179">Contiene l'origine e la modalità di acquisizione dello scanner corrente. Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-180">Un'applicazione legge questa proprietà per determinare l'origine di acquisizione corrente dello scanner o per scrivere questa proprietà per impostare l'origine e la modalità dello scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="b3aa3-181">Inoltre, le applicazioni usano questa proprietà per abilitare e disabilitare la funzionalità di duplex.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="b3aa3-182">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="b3aa3-183">La tabella seguente contiene le dieci costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-184">Flags</span><span class="sxs-lookup"><span data-stu-id="b3aa3-184">Flags</span></span></th>
<th><span data-ttu-id="b3aa3-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-186">FEEDER</span><span class="sxs-lookup"><span data-stu-id="b3aa3-186">FEEDER</span></span></td>
<td><span data-ttu-id="b3aa3-187">Eseguire l'analisi usando il feeder del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-188">PIANALE</span><span class="sxs-lookup"><span data-stu-id="b3aa3-188">FLATBED</span></span></td>
<td><span data-ttu-id="b3aa3-189">Eseguire l'analisi usando il piano.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-190">DUPLEX</span><span class="sxs-lookup"><span data-stu-id="b3aa3-190">DUPLEX</span></span></td>
<td><span data-ttu-id="b3aa3-191">Eseguire l'analisi usando le operazioni di duplex.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="b3aa3-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="b3aa3-193">Consente l'inserimento automatico del documento successivo dopo un'analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="b3aa3-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="b3aa3-195">Eseguire prima l'analisi della parte anteriore del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-195">Scan the front of the document first.</span></span> <span data-ttu-id="b3aa3-196">Questo valore è valido quando si imposta DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="b3aa3-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="b3aa3-198">Eseguire prima la scansione della parte posteriore del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-198">Scan the back of the document first.</span></span> <span data-ttu-id="b3aa3-199">Questo valore è valido quando si imposta DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b3aa3-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="b3aa3-201">Esegue l'analisi solo dell'oggetto front.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-201">Scan the front only.</span></span> <span data-ttu-id="b3aa3-202">Questo valore è valido quando si imposta DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="b3aa3-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="b3aa3-204">Eseguire la scansione solo della parte posteriore.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-204">Scan the back only.</span></span> <span data-ttu-id="b3aa3-205">Questo valore è valido quando si imposta DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="b3aa3-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="b3aa3-207">Esegue l'analisi della pagina successiva del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-208">Prefeed</span><span class="sxs-lookup"><span data-stu-id="b3aa3-208">PREFEED</span></span></td>
<td><span data-ttu-id="b3aa3-209">Abilitare la modalità pre-feed.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-209">Enable pre-feed mode.</span></span> <span data-ttu-id="b3aa3-210">Pre-posizionare il documento successivo durante l'analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="b3aa3-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-212">Contiene lo stato corrente del piano, del feeder di documenti o del duplex installato dello scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="b3aa3-213">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-214">Un'applicazione legge questa proprietà per determinare se il dispositivo scanner è pronto per essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="b3aa3-215">Si tratta di un modo ideale per verificare se la carta si trova nel feeder prima di acquisire un'immagine.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="b3aa3-216">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-217">La tabella seguente contiene le costanti valide per questa proprietà. Un asterisco \* indica che il flag non è supportato in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="b3aa3-218">Il simbolo <strong>V</strong> indica che il flag è supportato solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-219">Flags</span><span class="sxs-lookup"><span data-stu-id="b3aa3-219">Flags</span></span></th>
<th><span data-ttu-id="b3aa3-220">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="b3aa3-221">FEED_READY</span></span></td>
<td><span data-ttu-id="b3aa3-222">Il piano è pronto per l'uso.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="b3aa3-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="b3aa3-224">Lo scanner ha un documento sulla piastra piana.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="b3aa3-225">DUP_READY</span></span></td>
<td><span data-ttu-id="b3aa3-226">Il duplex è abilitato e pronto per l'uso.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="b3aa3-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="b3aa3-228">La copertura del letto flat è attiva.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="b3aa3-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="b3aa3-230">Il percorso carta è coperto e impedisce il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="b3aa3-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="b3aa3-232">Un documento è bloccato nel Feeder del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="b3aa3-234">La scheda trasparenza è installata e pronta per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="b3aa3-236">Il dispositivo di archiviazione interno è pronto.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="b3aa3-238">Lo spazio di archiviazione è pieno e non è possibile caricare operazioni.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="b3aa3-240">Si è verificata una condizione di feed multiplo (in genere con un PAPER_JAM).</span><span class="sxs-lookup"><span data-stu-id="b3aa3-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="b3aa3-242">Si è verificato un errore che richiede l'intervento dell'utente sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="b3aa3-244">Lo scanner non è pronto a causa di un problema lamp.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="b3aa3-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-246">Contiene tutti i caratteri validi che un'applicazione può usare per creare stringhe di approvazione valide.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="b3aa3-247">Un approvatore è una stampante installata in uno scanner che stampa un SMS in ogni pagina analizzata.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="b3aa3-248">Minidriver deve convalidare l'impostazione della proprietà <strong>WIA_DPS_ENDORSER_STRING</strong> in base al set di caratteri valido in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="b3aa3-249">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-250">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="b3aa3-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-252">Contiene una stringa che deve essere approvata (in altre parole, stampata) in ogni pagina analizzata da minidriver.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="b3aa3-253">Un'applicazione imposta questa proprietà utilizzando il set di caratteri valido indicato nella proprietà <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="b3aa3-254">Il minidriver deve avallare i documenti solo se in questa proprietà è impostata una stringa.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="b3aa3-255">Una stringa vuota indica che la funzionalità dell'approvatore è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="b3aa3-256">Poiché è responsabilità del driver interpretare la stringa dell'approvatore, il driver può utilizzare caratteri speciali in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="b3aa3-257">Tuttavia, solo le applicazioni capirebbero questi caratteri.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="b3aa3-258">Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-259">Un driver che supporta la proprietà <strong>WIA_DPS_ENDORSER_STRING</strong> deve supportare il seguente elenco di token.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-260">token</span><span class="sxs-lookup"><span data-stu-id="b3aa3-260">Token</span></span></th>
<th><span data-ttu-id="b3aa3-261">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-262">$DATE $</span><span class="sxs-lookup"><span data-stu-id="b3aa3-262">$DATE$</span></span></td>
<td><span data-ttu-id="b3aa3-263">Data nel formato AAAA/MM/GG.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-264">$DAY $</span><span class="sxs-lookup"><span data-stu-id="b3aa3-264">$DAY$</span></span></td>
<td><span data-ttu-id="b3aa3-265">Il giorno nel formato gg.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="b3aa3-266">$MONTH$</span></span></td>
<td><span data-ttu-id="b3aa3-267">Mese dell'anno nel formato MM.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-268">$PAGE _COUNT $</span><span class="sxs-lookup"><span data-stu-id="b3aa3-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="b3aa3-269">Numero di pagine trasferite.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-270">$TIME $</span><span class="sxs-lookup"><span data-stu-id="b3aa3-270">$TIME$</span></span></td>
<td><span data-ttu-id="b3aa3-271">Ora del giorno nel formato HH: MM: SS.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-272">$YEAR $</span><span class="sxs-lookup"><span data-stu-id="b3aa3-272">$YEAR$</span></span></td>
<td><span data-ttu-id="b3aa3-273">Anno nel formato aaaa.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="b3aa3-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-275">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="b3aa3-276">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="b3aa3-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-278">Questa proprietà è supportata solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-279">Contiene l'indirizzo SOAP di un dispositivo scanner di servizi Web.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="b3aa3-280">Il mini driver WIA 2,0 crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-281">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="b3aa3-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-283">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-284">Contiene la registrazione, o allineamento orizzontale, per i documenti posizionati sulla superficie piana.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="b3aa3-285">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-286">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-287">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-288">Costante</span><span class="sxs-lookup"><span data-stu-id="b3aa3-288">Constant</span></span></th>
<th><span data-ttu-id="b3aa3-289">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b3aa3-291">Il documento viene lasciato giustificato.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-292">CENTRATO</span><span class="sxs-lookup"><span data-stu-id="b3aa3-292">CENTERED</span></span></td>
<td><span data-ttu-id="b3aa3-293">Il documento è centrato.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b3aa3-295">Il documento è giustificato a destra.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-296"><strong>Vedere anche</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="b3aa3-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="b3aa3-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-299">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-300">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-301">Specifica la larghezza massima, in millesimi di pollice, sottoposta a scansione nell'asse orizzontale (X) dalla piastra di uno scanner piano alla risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="b3aa3-302">Questa proprietà si applica anche ai feeder di documenti automatici che spostano i fogli sulla piastra di uno scanner per la scansione.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="b3aa3-303">Questa proprietà è obbligatoria per gli scanner con un piatto.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="b3aa3-304">Per gli altri tipi di scanner viene invece implementata la proprietà <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="b3aa3-305">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="b3aa3-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-307">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-308">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-309">Specifica la larghezza massima, in millesimi di pollice, che viene analizzata nell'asse orizzontale (X) da uno scanner di feed di fogli o palmari alla risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="b3aa3-310">Questa proprietà si applica anche ai feeder di documenti automatici che eseguono l'analisi senza trasferire i fogli alla piastra di uno scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="b3aa3-311">Questa proprietà è obbligatoria per gli scanner a foglio, a scorrimento e con alimentazione manuale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="b3aa3-312">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="b3aa3-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-314">Contiene il tempo massimo per l'analisi di una singola pagina con le impostazioni delle proprietà correnti, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="b3aa3-315">Questa proprietà viene letta da un'applicazione per stimare il tempo necessario per l'analisi di una pagina.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="b3aa3-316">Questa operazione è utile quando si determinano le condizioni di un dispositivo che ha smesso di rispondere.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="b3aa3-317">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b3aa3-318">Questa proprietà è obbligatoria per tutti gli scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="b3aa3-319">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="b3aa3-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-321">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-322">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-323">Contiene le dimensioni orizzontali fisiche della pagina più piccola che il feeder di documenti dello scanner è in grado di analizzare, in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="b3aa3-324">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-325">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-326"><strong>Vedere anche</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="b3aa3-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="b3aa3-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-329">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-330">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-331">Contiene le dimensioni verticali fisiche della pagina più piccola che il feeder di documenti dello scanner è in grado di analizzare, in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="b3aa3-332">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-333">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-334"><strong>Vedere anche</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="b3aa3-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="b3aa3-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-337">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-338">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-339">Risoluzione ottica orizzontale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="b3aa3-340">Risoluzione ottica orizzontale più elevata supportata in DPI.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="b3aa3-341">Questa proprietà è un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-341">This property is a single value.</span></span> <span data-ttu-id="b3aa3-342">Non si tratta di un elenco di tutte le risoluzioni che possono essere generate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="b3aa3-343">Piuttosto, si tratta della risoluzione dell'ottica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="b3aa3-344">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b3aa3-345">Questa proprietà è obbligatoria per tutti gli scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="b3aa3-346">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="b3aa3-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-348">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-349">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-350">Risoluzione ottica verticale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="b3aa3-351">Risoluzione ottica verticale massima supportata in DPI.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="b3aa3-352">Questa proprietà è un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-352">This property is a single value.</span></span> <span data-ttu-id="b3aa3-353">Non si tratta di un elenco di tutte le risoluzioni generate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="b3aa3-354">Piuttosto, si tratta della risoluzione dell'ottica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="b3aa3-355">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b3aa3-356">Questa proprietà è obbligatoria per tutti gli scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="b3aa3-357">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="b3aa3-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-359">Contiene l'impostazione di orientamento corrente. Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-360">Un'applicazione imposta la proprietà <strong>WIA_DPS_ORIENTATION</strong> per definire l'orientamento originale di una pagina o di un'immagine da acquisire.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="b3aa3-361">Per informazioni sull'utilizzo di WIA_DPS_ORIENTATION, vedere <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="b3aa3-362">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b3aa3-363">La tabella seguente include le quattro costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-364">Valore</span><span class="sxs-lookup"><span data-stu-id="b3aa3-364">Value</span></span></th>
<th><span data-ttu-id="b3aa3-365">Defination</span><span class="sxs-lookup"><span data-stu-id="b3aa3-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-366">ORIZZONTALE</span><span class="sxs-lookup"><span data-stu-id="b3aa3-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="b3aa3-367">rotazione in senso antiorario di 90 gradi, relativa all'orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-368">VERTICALE</span><span class="sxs-lookup"><span data-stu-id="b3aa3-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="b3aa3-369">0 gradi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="b3aa3-370">ROT180</span></span></td>
<td><span data-ttu-id="b3aa3-371">rotazione in senso antiorario di 180 gradi, relativa all'orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="b3aa3-372">ROT270</span></span></td>
<td><span data-ttu-id="b3aa3-373">rotazione in senso antiorario di 270 gradi, relativa all'orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-374"><strong>Vedere anche</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="b3aa3-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="b3aa3-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-377">Colore utilizzato per il riempimento quando non sono disponibili dati di immagine sufficienti per riempire un buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="b3aa3-378">Questa proprietà viene implementata per gli scanner che riempiono il buffer.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="b3aa3-379">Questa proprietà è facoltativa per tutti gli scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-379">This property is optional for all scanners.</span></span> <span data-ttu-id="b3aa3-380">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-381">Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-382">Il formato delle informazioni sul colore è <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="b3aa3-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-384">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-385">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-386">Contiene l'altezza, in millesimi di pollice, della pagina attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="b3aa3-387">Minidriver crea e gestisce la proprietà <strong>WIA_DPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="b3aa3-388">Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="b3aa3-389">Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica l'altezza della pagina la cui proprietà <strong>WIA_DPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM (valore della proprietà <strong>WIA_DPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="b3aa3-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="b3aa3-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> deve essere sincronizzato con <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, che indica l'altezza, in pixel, della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="b3aa3-391">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="b3aa3-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-393">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-394">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-395">Contiene la dimensione della pagina attualmente selezionata per essere analizzata.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="b3aa3-396">Per selezionare le dimensioni della pagina da analizzare, questa proprietà viene impostata da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="b3aa3-397">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-398">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b3aa3-399">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-400">valore</span><span class="sxs-lookup"><span data-stu-id="b3aa3-400">Value</span></span></th>
<th><span data-ttu-id="b3aa3-401">Definizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="b3aa3-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="b3aa3-403">8267 X 11692 (orientamento verticale)</span><span class="sxs-lookup"><span data-stu-id="b3aa3-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="b3aa3-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="b3aa3-405">Definito dai valori delle proprietà <strong>WIA_DPS_PAGE_HEIGHT</strong> e <strong>WIA_DPS_PAGE_WIDTH</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="b3aa3-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="b3aa3-407">8500 X 11000 (orientamento verticale)</span><span class="sxs-lookup"><span data-stu-id="b3aa3-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-408">Il valore della proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina l'orientamento della pagina attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="b3aa3-409">Le proprietà <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> segnalano le dimensioni della pagina, in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="b3aa3-410">Si noti che queste proprietà devono essere concordate con <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, che contengono le dimensioni della pagina in pixel.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="b3aa3-411">I valori validi di tipo WIA_PROP_LIST devono dipendere da impostazioni valide della proprietà <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="b3aa3-412">Se il dispositivo non è in grado di analizzare documenti orientati al paesaggio con un'impostazione WIA_PAGE_A4, WIA_PAGE_A4 non deve essere visualizzato nell'elenco di valori validi per la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> è impostato su paesaggio.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="b3aa3-413">Se un'applicazione imposta <strong>WIA_DPS_PAGE_SIZE</strong> su un valore diverso da WIA_PAGE_CUSTOM, minidriver deve modificare i valori di <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> alle dimensioni della pagina in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="b3aa3-414">Deve anche modificare i valori delle <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> e <strong>WIA_IPS_YEXTENT</strong> alle dimensioni della pagina in pixel.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="b3aa3-415">Se un'impostazione di extent (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> o <strong>WIA_IPS_YEXTENT</strong>) viene modificata in un valore che non corrisponde all'impostazione della dimensione della pagina corrente, minidriver deve modificare il valore della proprietà <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="b3aa3-416">Il minidriver deve anche modificare <strong>WIA_DPS_PAGE_WIDTH</strong> o <strong>WIA_DPS_PAGE_HEIGHT</strong> in base alla nuova impostazione dell'extent.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="b3aa3-417">Se <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> è impostato su paesaggio, le impostazioni dell'extent verranno &quot; invertite. &quot; Se, ad esempio, un'applicazione imposta <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_A4, minidriver deve impostare <strong>WIA_DPS_PAGE_WIDTH</strong> su 11692 e <strong>WIA_DPS_PAGE_HEIGHT</strong> su 8267.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="b3aa3-418">Il minidriver deve inoltre impostare <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> di conseguenza. Si noti che se <strong>WIA_DPS_PAGE_SIZE</strong> è impostato su WIA_PAGE_CUSTOM, l'impostazione dell'orientamento non viene utilizzata per determinare le dimensioni dell'extent della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="b3aa3-419">Il minidriver è responsabile di garantire che la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> sia concordata con l'area di selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="b3aa3-420">Se un'applicazione modifica il valore di <strong>WIA_IPS_ORIENTATION</strong> a uno non valido per le dimensioni di pagina attualmente selezionate, minidriver deve modificare il valore di <strong>WIA_DPS_PAGE_SIZE</strong> in base a una dimensione di pagina supportata dal nuovo valore di orientamento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="b3aa3-421">Se un'applicazione imposta la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_CUSTOM, l'area di selezione corrente non è interessata.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="b3aa3-422">Il minidriver WIA dovrebbe ottenere il layout dell'immagine corrente, a partire dalle impostazioni correnti delle proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> e <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="b3aa3-423">Se l'impostazione delle dimensioni di pagina produce un'area di selezione esterna al letto dello scanner, il minidriver deve modificare automaticamente i valori delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> in impostazioni valide.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="b3aa3-424">Se le proprietà <strong>WIA_DPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> sono impostate contemporaneamente e non sono valide se applicate in combinazione, il minidriver deve avere esito negativo sulle impostazioni dell'applicazione restituendo un errore in <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="b3aa3-425">.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-425">.</span></span></p>
<p><span data-ttu-id="b3aa3-426">Nei quattro esempi seguenti vengono illustrati scenari di <strong>WIA_DPS_PAGE_SIZE</strong> diversi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="b3aa3-427">Il driver segnala le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="b3aa3-428">Un'applicazione imposta la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="b3aa3-429">Un'applicazione imposta la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> su paesaggio.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="b3aa3-430">Un'applicazione modifica la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> in un valore più piccolo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="b3aa3-431"><strong>Esempio 1: minidriver segnala le impostazioni</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="b3aa3-432">Nell'esempio seguente minidriver imposta un'area di selezione personalizzata prima che un'applicazione imposti le proprietà WIA.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="b3aa3-433">In questo caso, l'area di selezione rappresenta l'intero piano.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-433">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b3aa3-434"><strong>Esempio 2: un'applicazione imposta la</strong> <strong></strong><strong>Proprietà WIA_DPS_PAGE_SIZE su WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="b3aa3-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b3aa3-435"><strong>Esempio 3: un'applicazione imposta la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Proprietà WIA_IPS_ORIENTATION su paesaggio</strong>  </span><span class="sxs-lookup"><span data-stu-id="b3aa3-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="b3aa3-436">Il letto fisico deve essere in grado di acquisire una pagina originariamente con orientamento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b3aa3-437"><strong>Esempio 4: un'applicazione modifica la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Proprietà WIA_IPS_XEXTENT in un valore più piccolo</strong>  </span><span class="sxs-lookup"><span data-stu-id="b3aa3-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="b3aa3-438">Nell'esempio seguente un'applicazione modifica la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> in 1000.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="b3aa3-439">Il minidriver deve presupporre che il nuovo valore contenuto in <strong>WIA_IPS_XEXTENT</strong> non sia più valido per la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> e pertanto debba modificare <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="b3aa3-440">Il minidriver deve anche modificare <strong>WIA_DPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="b3aa3-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-442">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-443">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-444">Contiene la larghezza della pagina corrente selezionata, in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="b3aa3-445">Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="b3aa3-446">Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica la larghezza della pagina la cui proprietà <strong>WIA_DPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="b3aa3-447"><strong>WIA_DPS_PAGE_WIDTH</strong> deve essere sincronizzato con il valore di <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, che indica la larghezza, in pixel, della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="b3aa3-448">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-449">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="b3aa3-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-451">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-452">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-453">Contiene il numero corrente di pagine da acquisire da un feeder di documenti automatico.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="b3aa3-454">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-455">Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero per il numero massimo di pagine che possono essere mantenute dal feeder del documento)</span><span class="sxs-lookup"><span data-stu-id="b3aa3-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="b3aa3-456">Un'applicazione legge questa proprietà per determinare la capacità della pagina del feeder del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="b3aa3-457">L'applicazione imposta anche questa proprietà sul numero di pagine che verranno analizzate.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-458">Se è abilitata la modalità duplex (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> è impostata su Feeder | DUPLEX), <strong>WIA_DPS_PAGES</strong> è ancora uguale al numero di pagine da analizzare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-459">Un foglio di carta conterrà automaticamente due pagine se DUPLEX è abilitato, anche se il lato posteriore della pagina è vuoto.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="b3aa3-460">Impostando <strong>WIA_DPS_PAGES</strong> su 1, uno scanner elabora uno dei lati della pagina.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="b3aa3-461">Se uno scanner non è in grado di eseguire l'analisi di un solo lato di una pagina in modalità duplex, è consigliabile modificare il valore <strong>WIA_DPS_PAGES</strong> valido per il membro Inc della struttura WIA_PROPERTY_INFO su 2.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="b3aa3-462">Questo valore segnala all'applicazione che deve richiedere le pagine in multipli di due.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="b3aa3-463">Un valore pari a zero indica che <em>tutte le</em> pagine attualmente caricate nel Feeder del documento devono essere analizzate.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="b3aa3-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-465">Specifica il colore dell'oggetto platino nella parte posteriore del foglio da analizzare.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="b3aa3-466">Questa proprietà è facoltativa per gli scanner con un piatto.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="b3aa3-467">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-468">Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-469">Il formato delle informazioni sul colore è <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="b3aa3-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-471">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-472">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-473">Indica la modalità di anteprima per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="b3aa3-474">Un'applicazione imposta questa proprietà per posizionare il dispositivo in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="b3aa3-475">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="b3aa3-476">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-477">valore</span><span class="sxs-lookup"><span data-stu-id="b3aa3-477">Value</span></span></th>
<th><span data-ttu-id="b3aa3-478">Definizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="b3aa3-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="b3aa3-480">L'applicazione eseguirà un'analisi finale.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="b3aa3-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="b3aa3-482">L'applicazione eseguirà un'analisi di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="b3aa3-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b3aa3-484">Contiene un valore che indica se lo scanner memorizza nella cache le pagine in un buffer dello scanner prima di inviarle all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="b3aa3-485">Un valore pari a zero disabilita l'analisi in avanti e nessuna pagina verrà analizzata in anticipo.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="b3aa3-486">L'operazione di trasferimento dati normale nell'elemento Scan-Ahead memorizzato nel buffer consente di recuperare le pagine memorizzate nel buffer.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="b3aa3-487">Non è possibile modificare le proprietà WIA durante un'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="b3aa3-488">Questa proprietà è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-488">This property is optional.</span></span></p>
<p><span data-ttu-id="b3aa3-489">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> di zero al numero massimo di pagine che possono essere mantenute dal feeder del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="b3aa3-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-491">Questa proprietà è supportata solo da Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-492">Indica l'origine di input (piano, alimentatore automatico di documenti o adattatore di analisi fil) da cui eseguire l'analisi o il percorso di archiviazione da cui trasferire i dati.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="b3aa3-493">Un evento Scan notifica all'applicazione che l'utente ha avviato un'analisi, ma l'evento non fornisce il nome dell'elemento WIA che rappresenta l'origine di input.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="b3aa3-494">Il gestore eventi dell'applicazione può eseguire una query sulla proprietà WIA_DPS_SCAN_AVAILABLE_ITEM dell'elemento radice per ottenere il nome dell'elemento di origine di input.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="b3aa3-495">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> di zero al numero massimo di pagine che possono essere mantenute dal feeder del documento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="b3aa3-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-497">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-498">Contiene l'ID servizio di un dispositivo scanner di servizi Web.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="b3aa3-499">Il mini driver WIA 2,0 crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-500">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="b3aa3-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-502">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-503">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-504">Contiene la registrazione, ovvero l'allineamento e il rilevamento dei bordi, per i documenti posizionati sul piano.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="b3aa3-505">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="b3aa3-506">Questa proprietà indica il modo in cui il foglio è posizionato orizzontalmente sull'inizio di un'analisi di un palmare o di uno scanner a schede.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="b3aa3-507">La proprietà viene usata per stimare la posizione di un documento all'interno dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="b3aa3-508">Per gli scanner che supportano più intestazioni di analisi, questa proprietà è relativa alla testa dell'analisi in primo piano.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="b3aa3-509">Questa proprietà è obbligatoria per gli scanner a foglio, a scorrimento e con alimentazione a scorrimento.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="b3aa3-510">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-511">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-512">Costante</span><span class="sxs-lookup"><span data-stu-id="b3aa3-512">Constant</span></span></th>
<th><span data-ttu-id="b3aa3-513">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b3aa3-515">Il foglio è posizionato a sinistra rispetto alla testa di analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-516">CENTRATO</span><span class="sxs-lookup"><span data-stu-id="b3aa3-516">CENTERED</span></span></td>
<td><span data-ttu-id="b3aa3-517">Il foglio è centrato sulla testa di scansione.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b3aa3-519">Il foglio è posizionato a destra rispetto alla testa di analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="b3aa3-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-521">Questa proprietà non è supportata da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="b3aa3-522">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-523">Indica se un elemento necessita di un controllo anteprima visualizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="b3aa3-524">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-525">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-526">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-527">Costante</span><span class="sxs-lookup"><span data-stu-id="b3aa3-527">Constant</span></span></th>
<th><span data-ttu-id="b3aa3-528">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b3aa3-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="b3aa3-530">Mostra un controllo anteprima per l'utente, perché questo dispositivo può eseguire un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="b3aa3-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="b3aa3-532">Non visualizzare un controllo anteprima per l'utente, perché questo dispositivo non è in grado di eseguire un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="b3aa3-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-534">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-535">Utilizzato dal servizio WIA per informare il mini-driver sul nome dell'account utente (incluso il nome di dominio di rete quando applicabile) della sessione in cui è in esecuzione l'applicazione WIA corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="b3aa3-536">Si tratta di una proprietà elemento radice, gestita dal servizio WIA.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="b3aa3-537">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="b3aa3-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-539">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-540">Contiene la registrazione, ovvero l'allineamento verticale e il rilevamento dei bordi, per i documenti posizionati sul piano.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="b3aa3-541">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="b3aa3-542">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b3aa3-543">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3aa3-544">Costante</span><span class="sxs-lookup"><span data-stu-id="b3aa3-544">Constant</span></span></th>
<th><span data-ttu-id="b3aa3-545">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3aa3-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b3aa3-547">Il documento è giustificato in primo piano.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3aa3-548">CENTRATO</span><span class="sxs-lookup"><span data-stu-id="b3aa3-548">CENTERED</span></span></td>
<td><span data-ttu-id="b3aa3-549">Il documento è centrato.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3aa3-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="b3aa3-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="b3aa3-551">Il documento è giustificato in basso.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b3aa3-552"><strong>Vedere anche</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="b3aa3-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="b3aa3-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="b3aa3-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-555">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-556">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-557">Specifica l'altezza massima, in millesimi di pollice, sottoposta a scansione nell'asse verticale (Y) dalla piastra di uno scanner piano alla risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="b3aa3-558">Questa proprietà si applica anche ai feeder di documenti automatici, che spostano i fogli sulla piastra di uno scanner piano per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="b3aa3-559">Questa proprietà è obbligatoria per gli scanner con un piatto.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="b3aa3-560">Per gli altri tipi di scanner viene invece implementata la proprietà <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</span><span class="sxs-lookup"><span data-stu-id="b3aa3-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="b3aa3-561">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="b3aa3-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span><span class="sxs-lookup"><span data-stu-id="b3aa3-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="b3aa3-563">Questa proprietà non è supportata in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="b3aa3-564">Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="b3aa3-565">Specifica l'altezza massima, in millesimi di pollice, che viene analizzata nell'asse verticale (Y) da uno scanner di feed di fogli o palmari alla risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="b3aa3-566">Questa proprietà si applica anche ai feeder di documenti automatici che eseguono l'analisi senza trasferire i fogli alla piastra di uno scanner.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="b3aa3-567">Questa proprietà è obbligatoria per gli scanner a foglio.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="b3aa3-568">Gli scanner a scorrimento e con alimentazione a mano non devono implementare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3aa3-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="b3aa3-569">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b3aa3-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b3aa3-570">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3aa3-570">Requirements</span></span>



| <span data-ttu-id="b3aa3-571">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3aa3-571">Requirement</span></span> | <span data-ttu-id="b3aa3-572">Valore</span><span class="sxs-lookup"><span data-stu-id="b3aa3-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3aa3-573">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3aa3-573">Minimum supported client</span></span><br/> | <span data-ttu-id="b3aa3-574">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b3aa3-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b3aa3-575">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3aa3-575">Minimum supported server</span></span><br/> | <span data-ttu-id="b3aa3-576">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3aa3-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b3aa3-577">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3aa3-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3aa3-578"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3aa3-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
