---
description: Le costanti seguenti specificano il set valido di proprietà degli elementi dello scanner WIA (Windows Image Acquisition).
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Costanti della proprietà elemento WIA dello scanner (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307287"
---
# <a name="scanner-wia-item-property-constants"></a><span data-ttu-id="cc171-103">Costanti della proprietà elemento WIA dello scanner</span><span class="sxs-lookup"><span data-stu-id="cc171-103">Scanner WIA Item Property Constants</span></span>

<span data-ttu-id="cc171-104">Le costanti seguenti specificano il set valido di proprietà degli elementi dello scanner WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="cc171-104">The following constants specify the valid set of Windows Image Acquisition (WIA) scanner item properties.</span></span>

<span data-ttu-id="cc171-105">Il prefisso "WIA \_ IP \_ " indica una proprietà Item per i dispositivi scanner e rappresenta la convenzione di denominazione usata in C/C++.</span><span class="sxs-lookup"><span data-stu-id="cc171-105">The prefix "WIA\_IPS\_" indicates an Item Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="cc171-106">Per finalità di scripting queste costanti usano il prefisso "ScannerPicture" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="cc171-106">For scripting purposes these constants use the prefix "ScannerPicture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="cc171-107">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="cc171-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="cc171-108">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="cc171-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cc171-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <span data-ttu-id="cc171-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-110"><dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="cc171-111">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-111">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="cc171-112">Attiva o disattiva l'inclinazione automatica.</span><span class="sxs-lookup"><span data-stu-id="cc171-112">Turns automatic deskew on or off.</span></span><br/> <span data-ttu-id="cc171-113">Facoltativo solo per WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-113">Optional for WIA_CATEGORY_FEEDER only.</span></span><br/> <span data-ttu-id="cc171-114">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-114">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="cc171-115">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-115">The following table has the constants that are valid with this property.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-116">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-116">Constant</span></span></th>
<th><span data-ttu-id="cc171-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-118">WIA_AUTO_DESKEW_ON</span><span class="sxs-lookup"><span data-stu-id="cc171-118">WIA_AUTO_DESKEW_ON</span></span></td>
<td><span data-ttu-id="cc171-119">Attivare l'inclinazione automatica.</span><span class="sxs-lookup"><span data-stu-id="cc171-119">Turn on automatic deskew.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-120">WIA_AUTO_DESKEW_OFF</span><span class="sxs-lookup"><span data-stu-id="cc171-120">WIA_AUTO_DESKEW_OFF</span></span></td>
<td><span data-ttu-id="cc171-121">Disattiva la deasimmetria automatica.</span><span class="sxs-lookup"><span data-stu-id="cc171-121">Turn off automatic deskew.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <span data-ttu-id="cc171-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-122"><dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-123">Valori di luminosità dell'immagine disponibili nello scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-123">The image brightness values available within the scanner.</span></span></p>
<p><span data-ttu-id="cc171-124">Contiene l'impostazione della luminosità hardware corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-124">Contains the current hardware brightness setting for the device.</span></span> <span data-ttu-id="cc171-125">Un'applicazione imposta questa proprietà sul valore di luminosità dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="cc171-125">An application sets this property to the hardware's brightness value.</span></span> <span data-ttu-id="cc171-126">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-126">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-127">I valori devono essere mappati in un intervallo compreso tra-1000 e 1000, dove 1000 corrisponde alla luminosità massima, 0 corrisponde alla luminosità normale e-1000 corrisponde alla luminosità minima.</span><span class="sxs-lookup"><span data-stu-id="cc171-127">Values should be mapped in a range from -1000 through 1000, where 1000 corresponds to the maximum brightness, 0 corresponds to normal brightness, and -1000 corresponds to the minimum brightness.</span></span></p>
<p><span data-ttu-id="cc171-128">Obbligatorio per tutti gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-128">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-129">Facoltativo, ma consigliato, per WIA_CATEGORY_FINISHED_FILE elementi che supportano le anteprime.</span><span class="sxs-lookup"><span data-stu-id="cc171-129">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="cc171-130">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-130">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <span data-ttu-id="cc171-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-131"><dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-132">Contiene l'impostazione di contrasto hardware corrente per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-132">Contains the current hardware contrast setting for a device.</span></span> <span data-ttu-id="cc171-133">Un'applicazione imposta questa proprietà sul valore di contrasto dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="cc171-133">An application sets this property to the hardware's contrast value.</span></span> <span data-ttu-id="cc171-134">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-134">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-135">I valori devono essere mappati in un intervallo compreso tra-1000 e 1000, dove-1000 corrisponde al contrasto minimo, 0 corrisponde al contrasto normale e 1000 corrisponde al contrasto massimo.</span><span class="sxs-lookup"><span data-stu-id="cc171-135">Values should be mapped in a range from -1000 through 1000, where -1000 corresponds to the minimum contrast, 0 corresponds to normal contrast, and 1000 corresponds to the maximum contrast.</span></span></p>
<p><span data-ttu-id="cc171-136">Obbligatorio per tutti gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-136">Required for all items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-137">Facoltativo, ma consigliato, per WIA_CATEGORY_FINISHED_FILE elementi che supportano le anteprime.</span><span class="sxs-lookup"><span data-stu-id="cc171-137">Optional, but recommended, for WIA_CATEGORY_FINISHED_FILE items supporting previews.</span></span></p>
<p><span data-ttu-id="cc171-138">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-138">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <span data-ttu-id="cc171-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-139"><dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-140">Contiene le impostazioni relative allo scopo corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-140">Contains the current intent settings.</span></span> <span data-ttu-id="cc171-141">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-141">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-142">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-142">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-143">Non è supportata per gli elementi WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-143">It is not supported for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-144">Tipo: accesso <strong>VT_I4</strong> : lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span><span class="sxs-lookup"><span data-stu-id="cc171-144">Type: <strong>VT_I4</strong> Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></span></span></p>
<p><span data-ttu-id="cc171-145">Il driver li usa per impostare le proprietà dell'elemento in base all'uso previsto dell'immagine da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc171-145">The driver uses these to preset item properties based on an application's intended use of the image.</span></span> <span data-ttu-id="cc171-146">Questo potrebbe includere, ad esempio, la qualità massima, le dimensioni minime e così via.</span><span class="sxs-lookup"><span data-stu-id="cc171-146">This might include, for example, maximum quality, minimum size, and so on.</span></span></p>
<p><span data-ttu-id="cc171-147">Il driver sceglie la profondità del bit, espressa in punti per pollice, e le altre impostazioni che determina sono appropriate per lo scopo selezionato.</span><span class="sxs-lookup"><span data-stu-id="cc171-147">The driver chooses the bit depth, in dots per inch, and other settings that it determines are appropriate for the selected intent.</span></span> <span data-ttu-id="cc171-148">Spetta all'applicazione leggere le impostazioni correnti per determinare quali proprietà sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="cc171-148">It is up to the application to read the current settings to determine which properties were changed.</span></span> <span data-ttu-id="cc171-149">Un'applicazione imposta questa proprietà per impostare automaticamente le proprietà WIA per finalità di acquisizione specifiche.</span><span class="sxs-lookup"><span data-stu-id="cc171-149">An application sets this property to auto-set the WIA properties for specific acquisition intent.</span></span> <span data-ttu-id="cc171-150">Questa proprietà è obbligatoria per tutti gli scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-150">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="cc171-151">Un'applicazione imposta questa proprietà per impostare automaticamente le proprietà WIA per finalità di acquisizione specifiche</span><span class="sxs-lookup"><span data-stu-id="cc171-151">An application sets this property to auto-set the WIA properties for specific acquisition intent</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-152">I flag possono essere combinati con un <strong>operatore OR</strong> bit per bit, ma un'immagine non può essere sia di scala di grigi che di colore.</span><span class="sxs-lookup"><span data-stu-id="cc171-152">The flags can be combined with a bitwise <strong>OR</strong> operator, but an image cannot be both grayscale and color.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-153">Questa proprietà è obbligatoria per tutti gli scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-153">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="cc171-154">La tabella seguente contiene i flag del tipo di immagine e le relative definizioni.</span><span class="sxs-lookup"><span data-stu-id="cc171-154">The following table contains the image-type flags and their definitions.</span></span> <span data-ttu-id="cc171-155">Questi flag vengono usati per impostare il tipo di immagine desiderato: colore, scala di grigi e così via.</span><span class="sxs-lookup"><span data-stu-id="cc171-155">These flags are used to set which type of image is intended: color, grayscale, and so on.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-156">Flag del tipo di immagine previsto</span><span class="sxs-lookup"><span data-stu-id="cc171-156">Intended image type flags</span></span></th>
<th><span data-ttu-id="cc171-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-158">WIA_INTENT_NONE</span><span class="sxs-lookup"><span data-stu-id="cc171-158">WIA_INTENT_NONE</span></span></td>
<td><span data-ttu-id="cc171-159">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cc171-159">Default value.</span></span> <span data-ttu-id="cc171-160">Non è stato specificato alcun preventivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-160">No intent is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-161">WIA_INTENT_IMAGE_TYPE_COLOR</span><span class="sxs-lookup"><span data-stu-id="cc171-161">WIA_INTENT_IMAGE_TYPE_COLOR</span></span></td>
<td><span data-ttu-id="cc171-162">L'applicazione intende preparare il dispositivo per un'analisi dei colori.</span><span class="sxs-lookup"><span data-stu-id="cc171-162">The application intends to prepare the device for a color scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="cc171-163">WIA_INTENT_IMAGE_TYPE_GRAYSCALE</span></span></td>
<td><span data-ttu-id="cc171-164">L'applicazione intende preparare il dispositivo per un'analisi in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="cc171-164">The application intends to prepare the device for a grayscale scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-165">WIA_INTENT_IMAGE_TYPE_TEXT</span><span class="sxs-lookup"><span data-stu-id="cc171-165">WIA_INTENT_IMAGE_TYPE_TEXT</span></span></td>
<td><span data-ttu-id="cc171-166">L'applicazione intende preparare il dispositivo per la scansione del testo.</span><span class="sxs-lookup"><span data-stu-id="cc171-166">The application intends to prepare the device for scanning text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-167">WIA_INTENT_IMAGE_TYPE_MASK</span><span class="sxs-lookup"><span data-stu-id="cc171-167">WIA_INTENT_IMAGE_TYPE_MASK</span></span></td>
<td><span data-ttu-id="cc171-168">Maschera per tutti i flag di tipo immagine.</span><span class="sxs-lookup"><span data-stu-id="cc171-168">Mask for all of the image-type flags.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cc171-169">La tabella seguente contiene i flag di qualità e dimensioni e le relative definizioni.</span><span class="sxs-lookup"><span data-stu-id="cc171-169">The following table contains the quality and size flags and their definitions.</span></span> <span data-ttu-id="cc171-170">Questi flag vengono usati per impostare il livello di qualità desiderato.</span><span class="sxs-lookup"><span data-stu-id="cc171-170">These flags are used to set which level of quality is intended.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-171">Flag di qualità/dimensioni immagine previsti</span><span class="sxs-lookup"><span data-stu-id="cc171-171">Intended image size/quality flags</span></span></th>
<th><span data-ttu-id="cc171-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-172">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-173">WIA_INTENT_MINIMIZE_SIZE</span><span class="sxs-lookup"><span data-stu-id="cc171-173">WIA_INTENT_MINIMIZE_SIZE</span></span></td>
<td><span data-ttu-id="cc171-174">L'applicazione intende preparare il dispositivo per l'analisi di un'immagine che risulta in un'analisi di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="cc171-174">The application intends to prepare the device for scanning an image that result's in a small scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-175">WIA_INTENT_MAXIMIZE_QUALITY</span><span class="sxs-lookup"><span data-stu-id="cc171-175">WIA_INTENT_MAXIMIZE_QUALITY</span></span></td>
<td><span data-ttu-id="cc171-176">L'applicazione intende preparare il dispositivo per l'analisi di un'immagine di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="cc171-176">The application intends to prepare the device for scanning a high-quality image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-177">WIA_INTENT_SIZE_MASK</span><span class="sxs-lookup"><span data-stu-id="cc171-177">WIA_INTENT_SIZE_MASK</span></span></td>
<td><span data-ttu-id="cc171-178">Questo flag è una maschera per tutti i flag di dimensione/qualità.</span><span class="sxs-lookup"><span data-stu-id="cc171-178">This flag is a mask for all of the size/quality flags.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-179">WIA_INTENT_BEST_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="cc171-179">WIA_INTENT_BEST_PREVIEW</span></span></td>
<td><span data-ttu-id="cc171-180">L'applicazione intende preparare il dispositivo per l'analisi di un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="cc171-180">The application intends to prepare the device for scanning a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <span data-ttu-id="cc171-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-181"><dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-182">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-182">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-183">Contiene il numero di pixel nella direzione x da WIA_IPS_XPOS alla coordinata x dell'angolo superiore dell'immagine da dependere.</span><span class="sxs-lookup"><span data-stu-id="cc171-183">Contains the number of pixels in the x-direction from WIA_IPS_XPOS to the x-coordinate of the uppermost corner of the image to be deskewed.</span></span> <span data-ttu-id="cc171-184">Viene quindi descritto, in combinazione con WIA_IPS_DESKEW_Y, in cui i due angoli superiori dell'immagine asimmetrica si trovano all'interno del rettangolo di delimitazione definito da WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="cc171-184">Hence, it describes, in conjunction with WIA_IPS_DESKEW_Y, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="cc171-185">la proprietà viene implementata dal driver dello scanner se supporta la deasimmetria.</span><span class="sxs-lookup"><span data-stu-id="cc171-185">his property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="cc171-186">I valori validi per WIA_IPS_DESKEW_X devono essere compresi tra 0 e (WIA_IPS_XEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="cc171-186">The valid values for WIA_IPS_DESKEW_X must be between 0 and (WIA_IPS_XEXTENT - 1).</span></span> <span data-ttu-id="cc171-187">Il valore 0 indica che non deve essere eseguita alcuna disasimmetria.</span><span class="sxs-lookup"><span data-stu-id="cc171-187">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="cc171-188">Questa proprietà è facoltativa per gli elementi delle categorie WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e non è disponibile per WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementi.</span><span class="sxs-lookup"><span data-stu-id="cc171-188">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-189">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="cc171-189">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <span data-ttu-id="cc171-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-190"><dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-191">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-191">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-192">Contiene il numero di pixel nella direzione y da WIA_IPS_YPOS alla coordinata y dell'angolo più a sinistra dell'immagine da dependere.</span><span class="sxs-lookup"><span data-stu-id="cc171-192">Contains the number of pixels in the y-direction from WIA_IPS_YPOS to the y-coordinate of the leftmost corner of the image to be deskewed.</span></span> <span data-ttu-id="cc171-193">Viene quindi descritto, in combinazione con WIA_IPS_DESKEW_X, in cui i due angoli superiori dell'immagine asimmetrica si trovano all'interno del rettangolo di delimitazione definito da WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT.</span><span class="sxs-lookup"><span data-stu-id="cc171-193">Hence, it describes, in conjunction with WIA_IPS_DESKEW_X, where the two upper corners of the skewed image are located within the bounding rectangle defined by WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT and WIA_IPS_YEXTENT.</span></span> <span data-ttu-id="cc171-194">Questa proprietà viene implementata dal driver dello scanner se supporta la deasimmetria.</span><span class="sxs-lookup"><span data-stu-id="cc171-194">This property is implemented by the scanner driver if it supports deskewing.</span></span></p>
<p><span data-ttu-id="cc171-195">I valori validi per WIA_IPS_DESKEW_Y devono essere compresi tra 0 e (WIA_IPS_YEXTENT-1).</span><span class="sxs-lookup"><span data-stu-id="cc171-195">The valid values for WIA_IPS_DESKEW_Y must be between 0 and (WIA_IPS_YEXTENT - 1).</span></span> <span data-ttu-id="cc171-196">Il valore 0 indica che non deve essere eseguita alcuna disasimmetria.</span><span class="sxs-lookup"><span data-stu-id="cc171-196">A value of 0 means that no deskew should be performed.</span></span></p>
<p><span data-ttu-id="cc171-197">Questa proprietà è facoltativa per gli elementi delle categorie WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e non è disponibile per WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementi.</span><span class="sxs-lookup"><span data-stu-id="cc171-197">This property is optional for items of the categories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM; and it is not available for WIA_CATEGORY_FINISHED_FILE or WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-198">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="cc171-198">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <span data-ttu-id="cc171-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-199"><dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-200">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-200">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-201">Contiene l'origine e la modalità di acquisizione dello scanner corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-201">Contains the current scanner acquisition source and mode.</span></span> <span data-ttu-id="cc171-202">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-202">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-203">Un'applicazione legge questa proprietà per determinare l'origine di acquisizione corrente dello scanner o per scrivere questa proprietà per impostare l'origine e la modalità dello scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-203">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="cc171-204">Inoltre, le applicazioni usano questa proprietà per abilitare e disabilitare la funzionalità di duplex.</span><span class="sxs-lookup"><span data-stu-id="cc171-204">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="cc171-205">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="cc171-205">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="cc171-206">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-206">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-207">Flags</span><span class="sxs-lookup"><span data-stu-id="cc171-207">Flags</span></span></th>
<th><span data-ttu-id="cc171-208">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-209">DUPLEX</span><span class="sxs-lookup"><span data-stu-id="cc171-209">DUPLEX</span></span></td>
<td><span data-ttu-id="cc171-210">Eseguire l'analisi usando le operazioni di duplex.</span><span class="sxs-lookup"><span data-stu-id="cc171-210">Scan using duplexer operations.</span></span> <span data-ttu-id="cc171-211">Analizza entrambi i lati del documento usando le impostazioni comuni configurate per l'elemento del feeder (WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="cc171-211">Scan both document sides using common settings configured for the feeder item (WIA_CATEGORY_FEEDER).</span></span> <span data-ttu-id="cc171-212">Non è possibile impostare entrambi DUPLEX e ADVANCE_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="cc171-212">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-213">ADVANCED_DUPLEX</span><span class="sxs-lookup"><span data-stu-id="cc171-213">ADVANCED_DUPLEX</span></span></td>
<td><span data-ttu-id="cc171-214">Eseguire l'analisi usando le singole impostazioni configurate per ogni elemento del feeder figlio (WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK).</span><span class="sxs-lookup"><span data-stu-id="cc171-214">Scan using individual settings configured for each child feeder item (WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK).</span></span> <span data-ttu-id="cc171-215">Non è possibile impostare entrambi DUPLEX e ADVANCE_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="cc171-215">DUPLEX and ADVANCE_DUPLEX cannot both be set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-216">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="cc171-216">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="cc171-217">Eseguire prima l'analisi della parte anteriore del documento.</span><span class="sxs-lookup"><span data-stu-id="cc171-217">Scan the front of the document first.</span></span> <span data-ttu-id="cc171-218">Questo valore è valido quando si imposta DUPLEX o ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="cc171-218">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-219">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="cc171-219">BACK_FIRST</span></span></td>
<td><span data-ttu-id="cc171-220">Eseguire prima la scansione della parte posteriore del documento.</span><span class="sxs-lookup"><span data-stu-id="cc171-220">Scan the back of the document first.</span></span> <span data-ttu-id="cc171-221">Questo valore è valido quando si imposta DUPLEX o ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="cc171-221">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-222">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="cc171-222">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="cc171-223">Esegue l'analisi solo dell'oggetto front.</span><span class="sxs-lookup"><span data-stu-id="cc171-223">Scan the front only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-224">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="cc171-224">BACK_ONLY</span></span></td>
<td><span data-ttu-id="cc171-225">Eseguire la scansione solo della parte posteriore.</span><span class="sxs-lookup"><span data-stu-id="cc171-225">Scan the back only.</span></span> <span data-ttu-id="cc171-226">Questo valore è valido quando si imposta DUPLEX o ADVANCED_DUPLEX.</span><span class="sxs-lookup"><span data-stu-id="cc171-226">This value is valid when DUPLEX or ADVANCED_DUPLEX is set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <span data-ttu-id="cc171-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-227"><dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-228">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-228">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-229">Abilita la specifica di un particolare allegato di analisi della pellicola quando ne sono presenti più di uno.</span><span class="sxs-lookup"><span data-stu-id="cc171-229">Enables specification of a particular film scanning attachment when there is more than one.</span></span></p>
<p><span data-ttu-id="cc171-230">Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FILM quando sono presenti più elementi di analisi del film.</span><span class="sxs-lookup"><span data-stu-id="cc171-230">This property is required for the WIA_CATEGORY_FILM items when there are multiple film scan items.</span></span> <span data-ttu-id="cc171-231">Se il dispositivo supporta solo un elemento del film dello scanner radice, questa proprietà è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="cc171-231">If the device supports only one root scanner film item then this property is optional.</span></span></p>
<p><span data-ttu-id="cc171-232">Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-232">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cc171-233">Valori consentiti: BSTR deve avere il formato @ResourceBinary ,- <ResourceID> per consentire la localizzazione perché questa stringa verrebbe esposta all'utente tramite l'interfaccia utente di analisi dei film.</span><span class="sxs-lookup"><span data-stu-id="cc171-233">Allowed values: The BSTR should be in the form of @ResourceBinary,-<ResourceID> to allow localization as this string would be exposed to the user through the film scanning UI.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <span data-ttu-id="cc171-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-234"><dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-235">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-235">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-236">Consente la configurazione dell'analisi del film corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-236">Enables configuration of the current film scan.</span></span></p>
<p><span data-ttu-id="cc171-237">Questa proprietà è obbligatoria per l'elemento WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-237">This property is required for the WIA_CATEGORY_FILM item.</span></span></p>
<p><span data-ttu-id="cc171-238">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-238">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cc171-239">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-239">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-240">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-240">Constant</span></span></th>
<th><span data-ttu-id="cc171-241">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-241">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-242">WIA_FILM_COLOR_SLIDE</span><span class="sxs-lookup"><span data-stu-id="cc171-242">WIA_FILM_COLOR_SLIDE</span></span></td>
<td><span data-ttu-id="cc171-243">Esegue l'analisi della diapositiva di un colore.</span><span class="sxs-lookup"><span data-stu-id="cc171-243">Scan for a color slide.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-244">WIA_FILM_COLOR_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="cc171-244">WIA_FILM_COLOR_NEGATIVE</span></span></td>
<td><span data-ttu-id="cc171-245">Esegue l'analisi di un colore negativo.</span><span class="sxs-lookup"><span data-stu-id="cc171-245">Scan for a color negative.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-246">WIA_FILM_BW_NEGATIVE</span><span class="sxs-lookup"><span data-stu-id="cc171-246">WIA_FILM_BW_NEGATIVE</span></span></td>
<td><span data-ttu-id="cc171-247">Cerca un valore negativo nero e bianco.</span><span class="sxs-lookup"><span data-stu-id="cc171-247">Scan for a black and white negative.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <span data-ttu-id="cc171-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-248"><dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-249">Riservato per un utilizzo futuro e non è implementato in questo momento.</span><span class="sxs-lookup"><span data-stu-id="cc171-249">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="cc171-250">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-250">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="cc171-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-251"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-252">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-252">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-253">Specifica il numero di elementi archiviati nell'elemento WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-253">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="cc171-254">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-254">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <span data-ttu-id="cc171-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-255"><dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-256">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-256">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-257">Attiva o disattiva la lampada dello scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-257">Turns the scanner lamp on or off.</span></span></p>
<p><span data-ttu-id="cc171-258">Facoltativo per gli elementi WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e consigliati per WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-258">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-259">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-259">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cc171-260">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-260">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-261">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-261">Constant</span></span></th>
<th><span data-ttu-id="cc171-262">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-263">WIA_LAMP_ON</span><span class="sxs-lookup"><span data-stu-id="cc171-263">WIA_LAMP_ON</span></span></td>
<td><span data-ttu-id="cc171-264">Accendere la lampada.</span><span class="sxs-lookup"><span data-stu-id="cc171-264">Turn on the lamp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-265">WIA_LAMP_OFF</span><span class="sxs-lookup"><span data-stu-id="cc171-265">WIA_LAMP_OFF</span></span></td>
<td><span data-ttu-id="cc171-266">Spegnere la lampada.</span><span class="sxs-lookup"><span data-stu-id="cc171-266">Turn off the lamp.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <span data-ttu-id="cc171-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-267"><dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-268">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-268">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-269">Imposta il tempo massimo di conservazione della lampada quando lo scanner non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cc171-269">Sets the maximum time to keep the lamp on when the scanner is not being used.</span></span></p>
<p><span data-ttu-id="cc171-270">Facoltativo per gli elementi WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e consigliati per WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-270">Optional for the WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, and WIA_CATEGORY_FILM items and recommended for WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-271">Tipo: <strong>VT_UI4</strong>, accesso: lettura/scrittura, valori validi: 0-0xFFF secondi</span><span class="sxs-lookup"><span data-stu-id="cc171-271">Type: <strong>VT_UI4</strong>, Access: Read/Write, Valid Values: 0 - 0xFFF seconds</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <span data-ttu-id="cc171-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-272"><dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-273">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-273">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-274">Specifica la larghezza massima, in millesimi di pollice, che viene analizzata nell'asse orizzontale (X) in corrispondenza della risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-274">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span> <span data-ttu-id="cc171-275">È possibile che si tratta della larghezza del feeder del foglio o del letto di analisi, in base al tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="cc171-275">This may be the width of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="cc171-276">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <span data-ttu-id="cc171-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-277"><dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-278">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-278">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-279">Specifica l'altezza massima, in millesimi di pollice, che viene analizzata nell'asse verticale (Y) in corrispondenza della risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-279">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span> <span data-ttu-id="cc171-280">Può trattarsi dell'altezza del feeder del foglio o del letto di analisi, in base al tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="cc171-280">This may be the height of the sheet feeder or the scanning bed, according to the type of item.</span></span></p>
<p><span data-ttu-id="cc171-281">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-281">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <span data-ttu-id="cc171-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-282"><dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-283">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-283">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-284">Specifica la larghezza minima, in millesimi di pollice, che viene analizzata nell'asse orizzontale (X) in corrispondenza della risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-284">Specifies the minimum width, in thousandths of an inch, that is scanned in the horizontal (X) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="cc171-285">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-285">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <span data-ttu-id="cc171-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-286"><dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-287">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-287">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-288">Specifica l'altezza minima, in millesimi di pollice, che viene analizzata nell'asse verticale (Y) in corrispondenza della risoluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-288">Specifies the minimum height, in thousandths of an inch, that is scanned in the vertical (Y) axis at the current resolution.</span></span></p>
<p><span data-ttu-id="cc171-289">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-289">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <span data-ttu-id="cc171-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-290"><dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-291">Riservato per un utilizzo futuro e non è implementato in questo momento.</span><span class="sxs-lookup"><span data-stu-id="cc171-291">Reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="cc171-292">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-292">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <span data-ttu-id="cc171-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-293"><dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-294">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-294">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-295">Risoluzione ottica orizzontale.</span><span class="sxs-lookup"><span data-stu-id="cc171-295">Horizontal Optical Resolution.</span></span> <span data-ttu-id="cc171-296">Risoluzione ottica orizzontale più elevata supportata in DPI.</span><span class="sxs-lookup"><span data-stu-id="cc171-296">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="cc171-297">Questa proprietà è un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="cc171-297">This property is a single value.</span></span> <span data-ttu-id="cc171-298">Non si tratta di un elenco di tutte le risoluzioni che possono essere generate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-298">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="cc171-299">Piuttosto, si tratta della risoluzione dell'ottica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-299">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="cc171-300">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-300">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cc171-301">Questa proprietà è obbligatoria per tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="cc171-301">This property is required for all items.</span></span></p>
<p><span data-ttu-id="cc171-302">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-302">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <span data-ttu-id="cc171-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-303"><dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-304">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-304">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-305">Risoluzione ottica verticale.</span><span class="sxs-lookup"><span data-stu-id="cc171-305">Vertical Optical Resolution.</span></span> <span data-ttu-id="cc171-306">Risoluzione ottica verticale massima supportata in DPI.</span><span class="sxs-lookup"><span data-stu-id="cc171-306">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="cc171-307">Questa proprietà è un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="cc171-307">This property is a single value.</span></span> <span data-ttu-id="cc171-308">Non si tratta di un elenco di tutte le risoluzioni generate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-308">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="cc171-309">Piuttosto, si tratta della risoluzione dell'ottica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-309">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="cc171-310">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-310">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cc171-311">Questa proprietà è obbligatoria per tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="cc171-311">This property is required for all items.</span></span></p>
<p><span data-ttu-id="cc171-312">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <span data-ttu-id="cc171-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-313"><dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-314">Specifica l'orientamento corrente dei documenti da analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-314">Specifies the current orientation of the documents to be scanned.</span></span> <span data-ttu-id="cc171-315">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-315">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-316">Un'applicazione imposta questa proprietà per definire l'orientamento originale di una pagina o di un'immagine da acquisire.</span><span class="sxs-lookup"><span data-stu-id="cc171-316">An application sets this property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="cc171-317">Per informazioni sull'utilizzo di WIA_IPS_ORIENTATION, vedere <strong>WIA_IPS_PAGE_SIZE</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc171-317">For information on how to use WIA_IPS_ORIENTATION, see <strong>WIA_IPS_PAGE_SIZE</strong>.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-318">WIA_IPS_ORIENTATION si riferisce alla posizione del documento da analizzare sul letto o sul feeder dello scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-318">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="cc171-319">Si tratta dell'orientamento del documento relativo alla direzione dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="cc171-319">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="cc171-320">WIA_IPS_ROTATION fa riferimento alla rotazione applicata all'immagine dopo che è stata eseguita l'analisi, appena prima che l'immagine venga trasferita nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc171-320">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-321">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-321">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cc171-322">La tabella seguente include le quattro costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-322">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-323">valore</span><span class="sxs-lookup"><span data-stu-id="cc171-323">Value</span></span></th>
<th><span data-ttu-id="cc171-324">Definizione</span><span class="sxs-lookup"><span data-stu-id="cc171-324">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-325">VERTICALE</span><span class="sxs-lookup"><span data-stu-id="cc171-325">PORTRAIT</span></span></td>
<td><span data-ttu-id="cc171-326">0 gradi.</span><span class="sxs-lookup"><span data-stu-id="cc171-326">0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-327">ORIZZONTALE</span><span class="sxs-lookup"><span data-stu-id="cc171-327">LANDSCAPE</span></span></td>
<td><span data-ttu-id="cc171-328">rotazione in senso antiorario di 90 gradi, relativa all'orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="cc171-328">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-329">ROT180</span><span class="sxs-lookup"><span data-stu-id="cc171-329">ROT180</span></span></td>
<td><span data-ttu-id="cc171-330">rotazione in senso antiorario di 180 gradi, relativa all'orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="cc171-330">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-331">ROT270</span><span class="sxs-lookup"><span data-stu-id="cc171-331">ROT270</span></span></td>
<td><span data-ttu-id="cc171-332">rotazione in senso antiorario di 270 gradi, relativa all'orientamento verticale.</span><span class="sxs-lookup"><span data-stu-id="cc171-332">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <span data-ttu-id="cc171-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-333"><dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-334">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-334">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-335">Contiene la dimensione della pagina attualmente impostata per essere analizzata.</span><span class="sxs-lookup"><span data-stu-id="cc171-335">Contains the size of the page that is currently set to be scanned.</span></span> <span data-ttu-id="cc171-336">Un'applicazione imposta questa proprietà per selezionare le dimensioni della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-336">An application sets this property to select the dimensions of the page to scan.</span></span> <span data-ttu-id="cc171-337">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-337">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-338">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-338">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cc171-339">Per le costanti che possono essere usate con questa proprietà, vedere le <a href="-wia-wia2-pagesizeconstants.md"><strong>costanti di dimensione della pagina WIA 2,0</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cc171-339">For the constants that can be used with this property, see <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 Page Size Constants</strong></a>.</span></span> <span data-ttu-id="cc171-340">Si noti che queste dimensioni non fisse, in particolare:</span><span class="sxs-lookup"><span data-stu-id="cc171-340">Note these non-fixed sizes, in particular:</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-341">valore</span><span class="sxs-lookup"><span data-stu-id="cc171-341">Value</span></span></th>
<th><span data-ttu-id="cc171-342">Definizione</span><span class="sxs-lookup"><span data-stu-id="cc171-342">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-343">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="cc171-343">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="cc171-344">Definito dai valori delle proprietà <strong>WIA_IPS_PAGE_HEIGHT</strong> e <strong>WIA_IPS_PAGE_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="cc171-344">Defined by the values of the <strong>WIA_IPS_PAGE_HEIGHT</strong> and <strong>WIA_IPS_PAGE_WIDTH</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-345">WIA_PAGE_AUTO</span><span class="sxs-lookup"><span data-stu-id="cc171-345">WIA_PAGE_AUTO</span></span></td>
<td><span data-ttu-id="cc171-346">Le dimensioni della pagina vengono determinate automaticamente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-346">Page size is automatically determined by the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-347">WIA_PAGE_CUSTOM_BASE</span><span class="sxs-lookup"><span data-stu-id="cc171-347">WIA_PAGE_CUSTOM_BASE</span></span></td>
<td><span data-ttu-id="cc171-348">Dimensioni di pagina personalizzate le cui dimensioni sono già note all'applicazione e al driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-348">A custom page size whose dimensions are already known to the application and the device driver.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="cc171-349">Il valore della proprietà <strong>WIA_IPS_ORIENTATION</strong> determina l'orientamento della pagina attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="cc171-349">The value of the <strong>WIA_IPS_ORIENTATION</strong> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="cc171-350">Le proprietà <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> segnalano le dimensioni della pagina, in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="cc171-350">The <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="cc171-351">Queste proprietà devono essere concordate con <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, che contengono le dimensioni della pagina in pixel.</span><span class="sxs-lookup"><span data-stu-id="cc171-351">These properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-352">I valori validi di tipo WIA_PROP_LIST dipendono da impostazioni valide della proprietà <strong>WIA_IPS_ORIENTATION</strong> .</span><span class="sxs-lookup"><span data-stu-id="cc171-352">Valid values of type WIA_PROP_LIST depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="cc171-353">Se, ad esempio, il dispositivo non è in grado di analizzare documenti orientati al paesaggio con un'impostazione WIA_PAGE_A4, WIA_PAGE_A4 non è un valore valido per la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> è impostato su orizzontale.</span><span class="sxs-lookup"><span data-stu-id="cc171-353">If, for example, the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 is not a valid value for the <strong>WIA_IPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-354">Se un'applicazione imposta <strong>WIA_IPS_PAGE_SIZE</strong> su un valore diverso da tre nella tabella precedente, il minidriver deve regolare i valori di <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> alle dimensioni della pagina in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="cc171-354">If an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to any value other than the three in the table above, the minidriver should adjust the values of <strong>WIA_IPS_PAGE_WIDTH</strong> and <strong>WIA_IPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="cc171-355">Deve anche modificare i valori delle <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> alle dimensioni della pagina in pixel.</span><span class="sxs-lookup"><span data-stu-id="cc171-355">It should also adjust the values of <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="cc171-356">Se un'impostazione di extent (<strong>WIA_IPS_XEXTENT</strong> o <strong>WIA_IPS_YEXTENT</strong>) viene modificata in un valore che non corrisponde all'impostazione della dimensione della pagina corrente, minidriver deve modificare il valore della proprietà <strong>WIA_IPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="cc171-356">If an extent setting (<strong>WIA_IPS_XEXTENT</strong> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page size setting, the minidriver should change the value of the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="cc171-357">Il minidriver deve anche modificare <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> o <strong>WIA_IPS_PAGE_HEIGHT</strong> in base alla nuova impostazione dell'extent.</span><span class="sxs-lookup"><span data-stu-id="cc171-357">The minidriver should also modify <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> or <strong>WIA_IPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="cc171-358">Se <strong>WIA_IPS_ORIENTATION</strong> è impostato su orizzontale, le impostazioni dell'extent verranno scambiate rispetto ai valori usuali.</span><span class="sxs-lookup"><span data-stu-id="cc171-358">If <strong>WIA_IPS_ORIENTATION</strong> is set to LANDSCAPE, the extent settings will be exchanged relative to their usual values.</span></span> <span data-ttu-id="cc171-359">Se, ad esempio, un'applicazione imposta <strong>WIA_IPS_PAGE_SIZE</strong> su WIA_PAGE_A4, minidriver imposta <strong>WIA_IPS_PAGE_WIDTH</strong> su 11692 e <strong>WIA_IPS_PAGE_HEIGHT</strong> su 8267.</span><span class="sxs-lookup"><span data-stu-id="cc171-359">For example, if an application sets <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver sets <strong>WIA_IPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_IPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="cc171-360">Il minidriver deve anche modificare <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="cc171-360">(The minidriver should also adjust <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.)</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-361">Se <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> è impostato su WIA_PAGE_CUSTOM, l'impostazione dell'orientamento non viene utilizzata per determinare le dimensioni dell'extent della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-361">If <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-362">Il minidriver è responsabile di garantire che la proprietà <strong>WIA_IPS_ORIENTATION</strong> sia concordata con l'area di selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-362">The minidriver is responsible for ensuring that the <strong>WIA_IPS_ORIENTATION</strong> property is in agreement with the current selection area.</span></span> <span data-ttu-id="cc171-363">Se un'applicazione modifica il valore di <strong>WIA_IPS_ORIENTATION</strong> a uno non valido per le dimensioni di pagina attualmente selezionate, minidriver deve modificare il valore di <strong>WIA_IPS_PAGE_SIZE</strong> in base a una dimensione di pagina supportata dal nuovo valore di orientamento.</span><span class="sxs-lookup"><span data-stu-id="cc171-363">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_IPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="cc171-364">Se un'applicazione imposta la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> su WIA_PAGE_CUSTOM, l'area di selezione corrente non è interessata.</span><span class="sxs-lookup"><span data-stu-id="cc171-364">If an application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="cc171-365">Il minidriver WIA dovrebbe ottenere il layout dell'immagine corrente, a partire dalle impostazioni correnti delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> .</span><span class="sxs-lookup"><span data-stu-id="cc171-365">The WIA minidriver should obtain the current image layout, starting from the current settings of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="cc171-366">Se l'impostazione delle dimensioni della pagina produce un'area di selezione esterna al letto dello scanner, il minidriver deve modificare automaticamente i valori delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> in impostazioni valide.</span><span class="sxs-lookup"><span data-stu-id="cc171-366">If the page size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="cc171-367">Se le proprietà <strong>WIA_IPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> sono impostate contemporaneamente e non sono valide se applicate in combinazione, il minidriver deve avere esito negativo sulle impostazioni dell'applicazione restituendo un errore in <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</span><span class="sxs-lookup"><span data-stu-id="cc171-367">If the <strong>WIA_IPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span></p>
<p><span data-ttu-id="cc171-368">Nei quattro esempi seguenti vengono illustrati scenari di <strong>WIA_IPS_PAGE_SIZE</strong> diversi.</span><span class="sxs-lookup"><span data-stu-id="cc171-368">The following four examples show different <strong>WIA_IPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="cc171-369">Il driver segnala le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="cc171-369">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="cc171-370">Un'applicazione imposta la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> su WIA_PAGE_LETTER.</span><span class="sxs-lookup"><span data-stu-id="cc171-370">An application sets the <strong>WIA_IPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="cc171-371">Un'applicazione imposta la proprietà <strong>WIA_IPS_ORIENTATION</strong> su Landscape.</span><span class="sxs-lookup"><span data-stu-id="cc171-371">An application sets the <strong>WIA_IPS_ORIENTATION</strong> property to LANDSCAPE.</span></span></li>
<li><span data-ttu-id="cc171-372">Un'applicazione modifica la proprietà <strong>WIA_IPS_XEXTENT</strong> in un valore più piccolo.</span><span class="sxs-lookup"><span data-stu-id="cc171-372">An application changes the <strong>WIA_IPS_XEXTENT</strong> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="cc171-373"><strong>Esempio 1: minidriver segnala le impostazioni</strong></span><span class="sxs-lookup"><span data-stu-id="cc171-373"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="cc171-374">Nell'esempio seguente minidriver imposta un'area di selezione personalizzata prima che un'applicazione imposti le proprietà WIA.</span><span class="sxs-lookup"><span data-stu-id="cc171-374">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="cc171-375">In questo caso, l'area di selezione rappresenta l'intero piano.</span><span class="sxs-lookup"><span data-stu-id="cc171-375">In this case, the selection area represents the entire flatbed.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
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
<p><span data-ttu-id="cc171-376"><strong>Esempio 2: un'applicazione imposta la</strong> <strong></strong><strong>Proprietà WIA_IPS_PAGE_SIZE su WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="cc171-376"><strong>Example 2: An application sets the</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
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
<p><span data-ttu-id="cc171-377"><strong>Esempio 3: un'applicazione imposta la</strong> <strong></strong><strong>Proprietà WIA_IPS_ORIENTATION su Landscape</strong>  </span><span class="sxs-lookup"><span data-stu-id="cc171-377"><strong>Example 3: An application sets the</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>property to LANDSCAPE</strong></span></span></p>
<p><span data-ttu-id="cc171-378">Il letto fisico deve essere in grado di acquisire una pagina originariamente con orientamento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="cc171-378">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<p><span data-ttu-id="cc171-379"><strong>Esempio 4: un'applicazione modifica la</strong> <strong></strong> <strong>Proprietà WIA_IPS_XEXTENT in un valore più piccolo</strong></span><span class="sxs-lookup"><span data-stu-id="cc171-379"><strong>Example 4: An application changes the</strong> <strong>WIA_IPS_XEXTENT</strong> <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="cc171-380">Nell'esempio seguente un'applicazione modifica la proprietà <strong>WIA_IPS_XEXTENT</strong> in 1000.</span><span class="sxs-lookup"><span data-stu-id="cc171-380">In the following example, an application changes the <strong>WIA_IPS_XEXTENT</strong> property to 1000.</span></span> <span data-ttu-id="cc171-381">Il minidriver deve presupporre che il nuovo valore contenuto in <strong>WIA_IPS_XEXTENT</strong> non sia più valido per la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> e pertanto debba modificare <strong>WIA_IPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="cc171-381">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_IPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_IPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="cc171-382">Il minidriver deve anche modificare <strong>WIA_IPS_PAGE_WIDTH</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc171-382">The minidriver must also adjust <strong>WIA_IPS_PAGE_WIDTH</strong>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <span data-ttu-id="cc171-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-383"><dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-384">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-384">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-385">Contiene l'altezza, in millesimi di pollice, della pagina attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="cc171-385">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="cc171-386">Minidriver crea e gestisce la proprietà <strong>WIA_IPS_PAGE_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="cc171-386">The minidriver creates and maintains the <strong>WIA_IPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="cc171-387">Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione.</span><span class="sxs-lookup"><span data-stu-id="cc171-387">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="cc171-388">Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica l'altezza della pagina la cui proprietà <strong>WIA_IPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM (valore della proprietà <strong>WIA_IPS_PAGE_SIZE</strong> ).</span><span class="sxs-lookup"><span data-stu-id="cc171-388">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_IPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="cc171-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> deve essere sincronizzato con <strong>WIA_IPS_XEXTENT</strong>, che indica l'altezza, in pixel, della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-389"><strong>WIA_IPS_PAGE_HEIGHT</strong> must be in sync with <strong>WIA_IPS_XEXTENT</strong>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="cc171-390">Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-390">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="cc171-391">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <span data-ttu-id="cc171-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-392"><dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-393">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-393">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-394">Contiene la larghezza della pagina corrente selezionata, in millesimi di pollice.</span><span class="sxs-lookup"><span data-stu-id="cc171-394">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="cc171-395">Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione.</span><span class="sxs-lookup"><span data-stu-id="cc171-395">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="cc171-396">Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica la larghezza della pagina la cui proprietà <strong>WIA_IPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM.</span><span class="sxs-lookup"><span data-stu-id="cc171-396">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_IPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="cc171-397"><strong>WIA_IPS_PAGE_WIDTH</strong> deve essere sincronizzato con il valore di <strong>WIA_IPS_XEXTENT</strong>, che indica la larghezza, in pixel, della pagina da analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-397"><strong>WIA_IPS_PAGE_WIDTH</strong> must be in sync with the value of <strong>WIA_IPS_XEXTENT</strong>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="cc171-398">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-398">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-399">Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-399">This property is required for WIA_CATEGORY_FEEDER items.</span></span></p>
<p><span data-ttu-id="cc171-400">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-400">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <span data-ttu-id="cc171-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-401"><dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-402">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-402">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-403">Contiene il numero corrente di pagine da acquisire da un feeder di documenti automatico.</span><span class="sxs-lookup"><span data-stu-id="cc171-403">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="cc171-404">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-404">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-405">Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> questo valore è pari a zero fino al numero massimo di pagine che lo scanner è in grado di analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-405">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> This is zero through the maximum number of pages that the scanner can scan.</span></span> <span data-ttu-id="cc171-406">Il valore è ALL_PAGES (= 0) se lo scanner è in grado di eseguire un'analisi continua.</span><span class="sxs-lookup"><span data-stu-id="cc171-406">The value is ALL_PAGES (= 0) if the scanner can scan continuously.</span></span></p>
<p><span data-ttu-id="cc171-407">Un'applicazione legge questa proprietà per determinare la capacità della pagina del feeder del documento.</span><span class="sxs-lookup"><span data-stu-id="cc171-407">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="cc171-408">L'applicazione imposta anche questa proprietà sul numero di pagine che verranno analizzate.</span><span class="sxs-lookup"><span data-stu-id="cc171-408">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-409">Se è abilitata la modalità duplex (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> è impostata su Feeder | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> è ancora uguale al numero di pagine da analizzare.</span><span class="sxs-lookup"><span data-stu-id="cc171-409">If duplex mode is enabled (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-410">Un foglio di carta conterrà automaticamente due pagine se DUPLEX è abilitato, anche se il lato posteriore della pagina è vuoto.</span><span class="sxs-lookup"><span data-stu-id="cc171-410">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="cc171-411">Se si imposta <strong>WIA_IPS_PAGES</strong> su 1, lo scanner elabora un lato della pagina.</span><span class="sxs-lookup"><span data-stu-id="cc171-411">Setting <strong>WIA_IPS_PAGES</strong> to 1 causes a scanner to process one side of the page.</span></span> <span data-ttu-id="cc171-412">Se uno scanner non è in grado di eseguire l'analisi di un solo lato di una pagina in modalità duplex, è consigliabile modificare il valore <strong>WIA_IPS_PAGES</strong> per il membro Inc del membro range della struttura WIA_PROPERTY_INFO su 2.</span><span class="sxs-lookup"><span data-stu-id="cc171-412">We recommend that, if a scanner is unable to scan only one side of a page while in duplex mode, you change the <strong>WIA_IPS_PAGES</strong> value for the Inc member of the Range member of the WIA_PROPERTY_INFO structure to 2.</span></span> <span data-ttu-id="cc171-413">Questo valore segnala all'applicazione che deve richiedere le pagine in multipli di due.</span><span class="sxs-lookup"><span data-stu-id="cc171-413">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="cc171-414">Il valore ALL_PAGES (= 0) indica che <em>tutte le</em> pagine attualmente caricate nel Feeder del documento devono essere analizzate.</span><span class="sxs-lookup"><span data-stu-id="cc171-414">A value of ALL_PAGES (= 0) means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <span data-ttu-id="cc171-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-415"><dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-416">Contiene l'impostazione corrente per i pixel bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="cc171-416">Contains the current setting for white and black pixels.</span></span> <span data-ttu-id="cc171-417">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-417">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-418">Un'applicazione legge questo valore per determinare il valore di bianco o nero (a seconda di ciò che l'applicazione sta eseguendo).</span><span class="sxs-lookup"><span data-stu-id="cc171-418">An application reads this value to determine the value of WHITE or BLACK (depending on what the application is doing).</span></span></p>
<p><span data-ttu-id="cc171-419">Obbligatorio per tutti gli elementi di acquisizione abilitati o archiviati; ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-419">Required for all acquisition enabled or stored items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-420">Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-420">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-421">Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="cc171-421">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="cc171-422">Se il dispositivo può essere impostato su un solo valore, creare un tipo di WIA_PROP_LIST e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="cc171-422">If the device can be set to only a single value, create a WIA_PROP_LIST type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="cc171-423">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-423">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-424">valore</span><span class="sxs-lookup"><span data-stu-id="cc171-424">Value</span></span></th>
<th><span data-ttu-id="cc171-425">Definizione</span><span class="sxs-lookup"><span data-stu-id="cc171-425">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-426">WIA_PHOTO_WHITE_0</span><span class="sxs-lookup"><span data-stu-id="cc171-426">WIA_PHOTO_WHITE_0</span></span></td>
<td><span data-ttu-id="cc171-427">Il bianco è 0 e il nero è 1.</span><span class="sxs-lookup"><span data-stu-id="cc171-427">WHITE is 0, and BLACK is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-428">WIA_PHOTO_WHITE_1</span><span class="sxs-lookup"><span data-stu-id="cc171-428">WIA_PHOTO_WHITE_1</span></span></td>
<td><span data-ttu-id="cc171-429">Il bianco è 1 e il nero è 0.</span><span class="sxs-lookup"><span data-stu-id="cc171-429">WHITE is 1, and BLACK is 0.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <span data-ttu-id="cc171-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-430"><dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-431">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-431">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-432">Indica la modalità di anteprima per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-432">Indicates the preview mode for a device.</span></span> <span data-ttu-id="cc171-433">Un'applicazione imposta questa proprietà per posizionare il dispositivo in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="cc171-433">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="cc171-434">Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM, facoltativo per l'elemento WIA_CATEGORY_FEEDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-434">This property is required for the WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items, optional for the WIA_CATEGORY_FEEDER item.</span></span></p>
<p><span data-ttu-id="cc171-435">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-435">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cc171-436">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-436">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-437">valore</span><span class="sxs-lookup"><span data-stu-id="cc171-437">Value</span></span></th>
<th><span data-ttu-id="cc171-438">Definizione</span><span class="sxs-lookup"><span data-stu-id="cc171-438">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-439">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="cc171-439">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="cc171-440">L'applicazione eseguirà un'analisi finale.</span><span class="sxs-lookup"><span data-stu-id="cc171-440">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-441">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="cc171-441">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="cc171-442">L'applicazione eseguirà un'analisi di anteprima.</span><span class="sxs-lookup"><span data-stu-id="cc171-442">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <span data-ttu-id="cc171-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-443"><dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-444">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-444">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-445">Specifica se l'immagine di anteprima esistente può essere aggiornata durante un'anteprima dell'immagine, in risposta a una modifica apportata alle proprietà WIA_IPA_DATATYPE o WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="cc171-445">Specifies whether the existing preview image can be updated during an image preview (in response to a change in the WIA_IPA_DATATYPE or WIA_IPA_DEPTH properties).</span></span></p>
<p><span data-ttu-id="cc171-446">Questa proprietà è facoltativa per tutti gli elementi abilitati per l'acquisizione che supportano le analisi di anteprima; ovvero WIA_IPS_PREVIEW è supportato con WIA_PREVIEW_SCAN.</span><span class="sxs-lookup"><span data-stu-id="cc171-446">This property is optional for all acquisition enabled items that support preview scans; that is, WIA_IPS_PREVIEW is supported with WIA_PREVIEW_SCAN.</span></span> <span data-ttu-id="cc171-447">Sono inclusi gli elementi di tipo WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-447">This includes items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-448">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-448">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cc171-449">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-449">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-450">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-450">Constant</span></span></th>
<th><span data-ttu-id="cc171-451">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-451">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-452">WIA_ADVANCED_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="cc171-452">WIA_ADVANCED_PREVIEW</span></span></td>
<td><span data-ttu-id="cc171-453">È possibile aggiornare l'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="cc171-453">Updating the existing image is possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-454">WIA_BASIC_PREVIEW</span><span class="sxs-lookup"><span data-stu-id="cc171-454">WIA_BASIC_PREVIEW</span></span></td>
<td><span data-ttu-id="cc171-455">È necessario eseguire un'altra analisi di anteprima perché non è possibile aggiornare l'immagine esistente.</span><span class="sxs-lookup"><span data-stu-id="cc171-455">Another preview scan must be executed because updating the existing image is not possible.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <span data-ttu-id="cc171-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-456"><dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-457">Contiene l'impostazione di rotazione corrente, se implementata.</span><span class="sxs-lookup"><span data-stu-id="cc171-457">Contains the current rotation setting, if it is implemented.</span></span> <span data-ttu-id="cc171-458">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-458">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-459">Un'applicazione imposta questa proprietà per indicare al driver la quantità (se presente) di ruotare l'immagine prima che il driver la restituisca all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc171-459">An application sets this property to inform the driver how much (if at all) to rotate the image before the driver returns it to the application.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-460">WIA_IPS_ORIENTATION si riferisce alla posizione del documento da analizzare sul letto o sul feeder dello scanner.</span><span class="sxs-lookup"><span data-stu-id="cc171-460">WIA_IPS_ORIENTATION refers to the position of the document to be scanned on the scanner bed or feeder.</span></span> <span data-ttu-id="cc171-461">Si tratta dell'orientamento del documento relativo alla direzione dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="cc171-461">It is the orientation of the document relative to the direction of the scan.</span></span> <span data-ttu-id="cc171-462">WIA_IPS_ROTATION fa riferimento alla rotazione applicata all'immagine dopo che è stata eseguita l'analisi, appena prima che l'immagine venga trasferita nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc171-462">WIA_IPS_ROTATION refers to rotation that is applied to the image after it is scanned, just before the image is transferred to the application.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-463">Il minidriver WIA è responsabile della rotazione dei dati dell'immagine prima di inviarli nuovamente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc171-463">The WIA minidriver is responsible for rotating the image data before sending it back to the application.</span></span> <span data-ttu-id="cc171-464">L'applicazione è responsabile del controllo delle intestazioni di immagine per visualizzare i valori appena ruotati.</span><span class="sxs-lookup"><span data-stu-id="cc171-464">The application is responsible for checking the image headers to see the newly rotated values.</span></span></p>
<p><span data-ttu-id="cc171-465">Esiste una notevole confusione sulla risoluzione dell'effetto della rotazione sull'area di selezione dell'immagine corrente (definita dalle proprietà <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> ).</span><span class="sxs-lookup"><span data-stu-id="cc171-465">Considerable confusion exists about resolving the effect of rotation on the current image's selection area (which is defined by the <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> properties).</span></span></p>
<p><span data-ttu-id="cc171-466"><em>Area di selezione</em> si riferisce all'area selezionata sul letto dello scanner fisico da cui viene acquisita un'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc171-466"><em>Selection area</em> refers to the selected area on the physical scanner bed that an image is be acquired from.</span></span> <span data-ttu-id="cc171-467"><strong>WIA_IPS_ROTATION</strong> non modifica l'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="cc171-467"><strong>WIA_IPS_ROTATION</strong> does not modify the selection area.</span></span> <span data-ttu-id="cc171-468">Il driver applica una rotazione in senso antiorario in base a <strong>WIA_IPS_ROTATION</strong> solo dopo che il driver ha acquisito l'area di selezione appropriata.</span><span class="sxs-lookup"><span data-stu-id="cc171-468">The driver applies a counterclockwise rotation according to <strong>WIA_IPS_ROTATION</strong> only after the driver has acquired the appropriate selection area.</span></span> <span data-ttu-id="cc171-469"><strong>WIA_IPS_ROTATION</strong> influisce sulle dimensioni dell'immagine di output, quindi tali dimensioni devono essere riflesse nell'intestazione dei dati dell'immagine risultante.</span><span class="sxs-lookup"><span data-stu-id="cc171-469"><strong>WIA_IPS_ROTATION</strong> does affect the dimensions of the output image, so these dimensions must be reflected in the resulting image's data header.</span></span></p>
<p><span data-ttu-id="cc171-470">Facoltativo per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-470">Optional for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-471">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="cc171-471">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="cc171-472">Sono definite le costanti di rotazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc171-472">The following rotation constants are defined.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-473">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-473">Constant</span></span></th>
<th><span data-ttu-id="cc171-474">Definizione</span><span class="sxs-lookup"><span data-stu-id="cc171-474">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-475">VERTICALE</span><span class="sxs-lookup"><span data-stu-id="cc171-475">PORTRAIT</span></span></td>
<td><span data-ttu-id="cc171-476">Il driver non effettuerà la rotazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc171-476">The driver will not rotate the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-477">ORIZZONTALE</span><span class="sxs-lookup"><span data-stu-id="cc171-477">LANDSCAPE</span></span></td>
<td><span data-ttu-id="cc171-478">Il driver TImpossibile ruota l'immagine di 90 gradi in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="cc171-478">TThe driver rotates the image 90 degrees counterclockwise.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-479">ROT180</span><span class="sxs-lookup"><span data-stu-id="cc171-479">ROT180</span></span></td>
<td><span data-ttu-id="cc171-480">Il driver ruota l'immagine di 180 gradi in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="cc171-480">The driver rotates the image 180 degrees counterclockwise.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-481">ROT270</span><span class="sxs-lookup"><span data-stu-id="cc171-481">ROT270</span></span></td>
<td><span data-ttu-id="cc171-482">Il driver ruota l'immagine di 270 gradi in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="cc171-482">The driver rotates the image 270 degrees counterclockwise.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <span data-ttu-id="cc171-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-483"><dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-484">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-484">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-485">Specifica se l'applicazione deve utilizzare il filtro di segmentazione del driver per l'analisi in più aree.</span><span class="sxs-lookup"><span data-stu-id="cc171-485">Specifies whether the application should use the driver's segmentation filter for multi-region scanning.</span></span> <span data-ttu-id="cc171-486">È necessario implementare WIA_IPS_SEGMENTATION per gli elementi WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM se supportano la creazione di elementi figlio con un filtro di segmentazione o se il driver crea elementi figlio per i frame fissi.</span><span class="sxs-lookup"><span data-stu-id="cc171-486">WIA_IPS_SEGMENTATION must be implemented for WIA_CATEGORY_FLATBED and WIA_CATEGORY_FILM items if they support either the creation of child items with a segmentation filter or if the driver itself creates child items for fixed frames.</span></span></p>
<p><span data-ttu-id="cc171-487">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-487">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cc171-488">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-488">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-489">valore</span><span class="sxs-lookup"><span data-stu-id="cc171-489">Value</span></span></th>
<th><span data-ttu-id="cc171-490">Definizione</span><span class="sxs-lookup"><span data-stu-id="cc171-490">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-491">WIA_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="cc171-491">WIA_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="cc171-492">L'applicazione deve usare il filtro di segmentazione per l'analisi in più aree.</span><span class="sxs-lookup"><span data-stu-id="cc171-492">The application should use the segmentation filter for multi-region scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-493">WIA_DONT_USE_SEGMENTATION_FILTER</span><span class="sxs-lookup"><span data-stu-id="cc171-493">WIA_DONT_USE_SEGMENTATION_FILTER</span></span></td>
<td><span data-ttu-id="cc171-494">Il driver crea gli elementi figlio per l'analisi in più aree.</span><span class="sxs-lookup"><span data-stu-id="cc171-494">The driver creates the child items itself for multi-region scanning.</span></span> <span data-ttu-id="cc171-495">Questa situazione si verifica in genere se lo scanner usa frame fissi a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="cc171-495">This is usually the case if the scanner uses fixed frames for this purpose.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-496">È possibile che un driver includa un filtro di segmentazione, ma che ancora WIA_IPS_SEGMENTATION sia impostato su WIA_DONT_USE_SEGMENTATION_FILTER per uno degli elementi (ad esempio, l'elemento WIA_CATEGORY_FILM).</span><span class="sxs-lookup"><span data-stu-id="cc171-496">It is possible for a driver to come with a segmentation filter, but still have WIA_IPS_SEGMENTATION set to WIA_DONT_USE_SEGMENTATION_FILTER for one of its items (such as, the WIA_CATEGORY_FILM item).</span></span> <span data-ttu-id="cc171-497">Questa situazione può verificarsi se lo scanner usa frame fissi per l'analisi dei film, ma non per l'analisi regolare dagli elementi WIA_CATEGORY_FLATBED.</span><span class="sxs-lookup"><span data-stu-id="cc171-497">This could be the case if the scanner uses fixed frames for film scanning, but not for regular scanning from WIA_CATEGORY_FLATBED items.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <span data-ttu-id="cc171-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-498"><dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-499">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-499">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-500">Contiene la registrazione, ovvero l'allineamento e il rilevamento dei bordi, per i documenti posizionati sul piano.</span><span class="sxs-lookup"><span data-stu-id="cc171-500">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="cc171-501">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-501">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="cc171-502">Questa proprietà indica il modo in cui il foglio è posizionato orizzontalmente sull'inizio di un'analisi di un palmare o di uno scanner a schede.</span><span class="sxs-lookup"><span data-stu-id="cc171-502">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="cc171-503">La proprietà viene usata per stimare la posizione di un documento all'interno dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="cc171-503">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="cc171-504">Per gli scanner che supportano più intestazioni di analisi, questa proprietà è relativa alla testa dell'analisi in primo piano.</span><span class="sxs-lookup"><span data-stu-id="cc171-504">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="cc171-505">Questa proprietà è obbligatoria per gli scanner a foglio, a scorrimento e con alimentazione a scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cc171-505">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="cc171-506">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-506">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cc171-507">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-507">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-508">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-508">Constant</span></span></th>
<th><span data-ttu-id="cc171-509">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-509">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-510">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cc171-510">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cc171-511">Il foglio è posizionato a sinistra rispetto alla testa di analisi.</span><span class="sxs-lookup"><span data-stu-id="cc171-511">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-512">CENTRATO</span><span class="sxs-lookup"><span data-stu-id="cc171-512">CENTERED</span></span></td>
<td><span data-ttu-id="cc171-513">Il foglio è centrato sulla testa di scansione.</span><span class="sxs-lookup"><span data-stu-id="cc171-513">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc171-514">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="cc171-514">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="cc171-515">Il foglio è posizionato a destra rispetto alla testa di analisi.</span><span class="sxs-lookup"><span data-stu-id="cc171-515">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <span data-ttu-id="cc171-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-516"><dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-517">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-517">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-518">Indica se un elemento necessita di un controllo anteprima visualizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="cc171-518">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="cc171-519">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-519">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-520">Facoltativo per tutti gli elementi abilitati per il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="cc171-520">Optional for all transfer enabled items.</span></span> <span data-ttu-id="cc171-521">Si tratta in genere solo di elementi delle categorie WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e WIA_CATEGORY_FINISHED_FILE.</span><span class="sxs-lookup"><span data-stu-id="cc171-521">This is usually just items of the categories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM, and WIA_CATEGORY_FINISHED_FILE.</span></span></p>
<p><span data-ttu-id="cc171-522">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-522">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="cc171-523">La tabella seguente contiene le costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-523">The following table has the constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc171-524">Costante</span><span class="sxs-lookup"><span data-stu-id="cc171-524">Constant</span></span></th>
<th><span data-ttu-id="cc171-525">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc171-525">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc171-526">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="cc171-526">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="cc171-527">Mostra un controllo anteprima per l'utente, perché questo dispositivo può eseguire un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="cc171-527">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc171-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="cc171-528">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="cc171-529">Non visualizzare un controllo anteprima per l'utente, perché questo dispositivo non è in grado di eseguire un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="cc171-529">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <span data-ttu-id="cc171-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-530"><dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-531">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-531">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-532">Specifica se l'applicazione (o i filtri) può creare elementi figlio sotto l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="cc171-532">Specifies whether the application (or the filters) can create child items under the current item.</span></span></p>
<p><span data-ttu-id="cc171-533">Facoltativo per tutte le categorie di elementi abilitati per il trasferimento: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e persino WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-533">Optional for all transfer enabled item categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM and even WIA_CATEGORY_FOLDER.</span></span> <span data-ttu-id="cc171-534">Se l'archiviazione non supporta il caricamento di nuovi elementi, questa proprietà non deve essere supportata o supportata con il valore <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="cc171-534">(If the storage won't support upload of new items then this property should be either unsupported or supported with the <strong>FALSE</strong> value.)</span></span></p>
<p><span data-ttu-id="cc171-535">Gli elementi che supportano WIA_IPS_SEGMENTATION e WIA_USE_SEGMENTATION_FILTER devono supportare anche WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION e devono essere impostati su <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc171-535">Items supporting WIA_IPS_SEGMENTATION and WIA_USE_SEGMENTATION_FILTER must also support WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION and have it set to <strong>TRUE</strong>.</span></span></p>
<p><span data-ttu-id="cc171-536">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <strong>true</strong> e <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="cc171-536">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <strong>TRUE</strong> and <strong>FALSE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <span data-ttu-id="cc171-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-537"><dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-538">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-538">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-539">Specifica il valore in scala di grigi che determina se un pixel verrà convertito in bianco o nero quando un'immagine viene convertita in monocromatico.</span><span class="sxs-lookup"><span data-stu-id="cc171-539">Specifies the grayscale value that determines whether a pixel will be converted to white or black when an image is converted to monochromatic.</span></span> <span data-ttu-id="cc171-540">I pixel al di sopra della soglia diventano bianchi.</span><span class="sxs-lookup"><span data-stu-id="cc171-540">Pixels above the threshold become white.</span></span> <span data-ttu-id="cc171-541">I pixel al di sotto della soglia diventano bianchi.</span><span class="sxs-lookup"><span data-stu-id="cc171-541">Pixels below the threshold become white.</span></span></p>
<p><span data-ttu-id="cc171-542">Questa proprietà è obbligatoria per gli elementi di acquisizione che supportano le analisi con 1 BPP e la cui proprietà WIA_IPA_DATATYPE è impostata su WIA_DATA_THRESHOLD.</span><span class="sxs-lookup"><span data-stu-id="cc171-542">This property is required for acquisition items that support 1-bpp scans and that have the WIA_IPA_DATATYPE property set to WIA_DATA_THRESHOLD.</span></span></p>
<p><span data-ttu-id="cc171-543">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-543">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <span data-ttu-id="cc171-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-544"><dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-545">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-545">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-546">Specifica se il driver è in grado di trasferire più elementi figlio in una singola chiamata di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="cc171-546">Specifies whether the driver is capable of transferring multiple child items in single transfer call.</span></span></p>
<p><span data-ttu-id="cc171-547">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="cc171-547">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="cc171-548">L'unico valore possibile per questa proprietà è WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span><span class="sxs-lookup"><span data-stu-id="cc171-548">The only possible value for this property is WIA_TRANSFER_CHILDREN_SINGLE_SCAN.</span></span> <span data-ttu-id="cc171-549">Se questo flag è impostato, il driver è in grado di trasferire più elementi figlio in una singola chiamata di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="cc171-549">If this flag is set, then the driver is capable of transfering multiple child items in single transfer call.</span></span> <span data-ttu-id="cc171-550">Se il flag non è impostato, il servizio WIA scorre gli elementi figlio in modo ricorsivo e quindi trasferisce ciascuno di tali elementi.</span><span class="sxs-lookup"><span data-stu-id="cc171-550">If the flag is not set, the WIA Service will walk through the child items recursively and then transfer each of those items.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="cc171-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-551"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-552">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-552">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-553">Specifica il numero di byte da caricare per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="cc171-553">Specifies the number of bytes to upload for the item.</span></span></p>
<p><span data-ttu-id="cc171-554">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-554">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <span data-ttu-id="cc171-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-555"><dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-556">Specifica il tempo di riscaldamento massimo, in millisecondi, necessario per il dispositivo prima di avviare l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="cc171-556">Specifies the maximum warm-up time, in milliseconds, that the device needs before starting the scanning operation.</span></span> <span data-ttu-id="cc171-557">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-557">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-558">Un'applicazione può leggere questa proprietà per determinare il tempo massimo di riscaldamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-558">An application can read this property to determine the maximum warm-up time for this device.</span></span> <span data-ttu-id="cc171-559">Può quindi presentare una finestra di &quot; dialogo in attesa del dispositivo per il riscaldamento &quot; , per informare l'utente che è possibile che si verifichi un'attesa o una pausa prima che succeda qualcosa.</span><span class="sxs-lookup"><span data-stu-id="cc171-559">It can then present a &quot;waiting for the device to warm up&quot; dialog box, to let the user know that a wait or pause might occur before anything happens.</span></span></p>
<p><span data-ttu-id="cc171-560">Questa proprietà è obbligatoria per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-560">This property is required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-561">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <span data-ttu-id="cc171-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-562"><dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-563">Contiene la larghezza corrente, in pixel, dell'immagine selezionata da acquisire.</span><span class="sxs-lookup"><span data-stu-id="cc171-563">Contains the current width, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="cc171-564">Un'applicazione imposta questa proprietà per contrassegnare la larghezza di un'area di selezione da acquisire.</span><span class="sxs-lookup"><span data-stu-id="cc171-564">An application sets this property to mark the width of a selection area to acquire.</span></span> <span data-ttu-id="cc171-565">Questa proprietà deve essere conforme alla proprietà <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc171-565">This property must agree with the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="cc171-566">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-566">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-567">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-567">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-568">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-568">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <span data-ttu-id="cc171-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-569"><dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-570">Contiene la coordinata x, in pixel, dell'angolo superiore sinistro dell'immagine selezionata.</span><span class="sxs-lookup"><span data-stu-id="cc171-570">Contains the x coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="cc171-571">Un'applicazione imposta questa proprietà per contrassegnare l'angolo superiore sinistro dell'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="cc171-571">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="cc171-572">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-572">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-573">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-573">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-574">Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-574">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-575">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-575">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <span data-ttu-id="cc171-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-576"><dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-577">Contiene la risoluzione orizzontale corrente, in pixel per pollice, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-577">Contains the current horizontal resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="cc171-578">Un'applicazione imposta questa proprietà per impostare la risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="cc171-578">An application sets this property to set the horizontal resolution.</span></span> <span data-ttu-id="cc171-579">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-579">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-580">Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="cc171-580">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="cc171-581">Questo è anche un caso in cui un'impostazione di risoluzione dipende da un'altra soluzione.</span><span class="sxs-lookup"><span data-stu-id="cc171-581">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="cc171-582">(La risoluzione verticale può dipendere dalla risoluzione orizzontale).</span><span class="sxs-lookup"><span data-stu-id="cc171-582">(The vertical resolution can depend on the horizontal resolution.)</span></span></p>
<p><span data-ttu-id="cc171-583">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-583">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-584">Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-584">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-585">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="cc171-585">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <span data-ttu-id="cc171-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-586"><dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-587">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-587">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-588">Imposta il ridimensionamento orizzontale, in percentuale, che può essere applicato alle immagini analizzate all'interno del dispositivo dello scanner o del relativo driver.</span><span class="sxs-lookup"><span data-stu-id="cc171-588">Sets the horizontal scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="cc171-589">Questa proprietà è facoltativa per tutti gli elementi abilitati per l'acquisizione. ovvero elementi di tipo WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-589">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-590">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="cc171-590">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="cc171-591">I valori possono essere compresi tra 1 e massimo VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="cc171-591">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="cc171-592">100, ad esempio, non prevede alcun ridimensionamento, 050 indica il ridimensionamento fino al 50% della dimensione originale e 200 indica il ridimensionamento fino al 200% delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="cc171-592">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <span data-ttu-id="cc171-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-593"><dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-594">Contiene l'altezza corrente, in pixel, dell'immagine selezionata da acquisire.</span><span class="sxs-lookup"><span data-stu-id="cc171-594">Contains the current height, in pixels, of the selected image to acquire.</span></span> <span data-ttu-id="cc171-595">Un'applicazione imposta questa proprietà per contrassegnare l'altezza di un'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="cc171-595">An application sets this property to mark the height of a selection area.</span></span> <span data-ttu-id="cc171-596">Questa proprietà deve essere conforme al valore della proprietà <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc171-596">This property must be agree with the value of the <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> property.</span></span> <span data-ttu-id="cc171-597">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-597">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-598">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-598">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-599">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-599">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <span data-ttu-id="cc171-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-600"><dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-601">Coordinata y corrente, espressa in pixel, dell'angolo superiore sinistro dell'immagine selezionata.</span><span class="sxs-lookup"><span data-stu-id="cc171-601">Current y coordinate, in pixels, of the upper-left corner of the selected image.</span></span> <span data-ttu-id="cc171-602">Un'applicazione imposta questa proprietà per contrassegnare l'angolo superiore sinistro dell'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="cc171-602">An application sets this property to mark the upper-left corner of the selection area.</span></span> <span data-ttu-id="cc171-603">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-603">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-604">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-604">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-605">Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-605">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-606">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span><span class="sxs-lookup"><span data-stu-id="cc171-606">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <span data-ttu-id="cc171-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-607"><dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="cc171-608">Contiene la risoluzione verticale corrente, in pixel per pollice, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc171-608">Contains the current vertical resolution, in pixels per inch, for the device.</span></span> <span data-ttu-id="cc171-609">Un'applicazione imposta questa proprietà per impostare la risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="cc171-609">An application sets this property to set the vertical resolution.</span></span> <span data-ttu-id="cc171-610">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cc171-610">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="cc171-611">Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno.</span><span class="sxs-lookup"><span data-stu-id="cc171-611">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span> <span data-ttu-id="cc171-612">Questo è anche un caso in cui un'impostazione di risoluzione dipende da un'altra soluzione.</span><span class="sxs-lookup"><span data-stu-id="cc171-612">This is also a case where one resolution setting depends on another resolution.</span></span> <span data-ttu-id="cc171-613">La risoluzione orizzontale può dipendere dalla risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="cc171-613">(The horizontal resolution can depend on the vertical resolution.)</span></span></p>
<p><span data-ttu-id="cc171-614">Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-614">Required for all acquisition enabled items; that is, items in the categories: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE, and WIA_CATEGORY_FILM.</span></span> <span data-ttu-id="cc171-615">Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="cc171-615">It is not supported for WIA_CATEGORY_FOLDER items.</span></span></p>
<p><span data-ttu-id="cc171-616">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="cc171-616">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <span data-ttu-id="cc171-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span><span class="sxs-lookup"><span data-stu-id="cc171-617"><dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="cc171-618">Questa proprietà è supportata solo da Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cc171-618">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="cc171-619">Imposta il ridimensionamento verticale, in percentuale, che può essere applicato alle immagini analizzate all'interno del dispositivo dello scanner o del relativo driver.</span><span class="sxs-lookup"><span data-stu-id="cc171-619">Sets the vertical scaling, as a percentage, that may be applied to scanned images within the scanner device or its driver.</span></span></p>
<p><span data-ttu-id="cc171-620">Questa proprietà è facoltativa per tutti gli elementi abilitati per l'acquisizione. ovvero elementi di tipo WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</span><span class="sxs-lookup"><span data-stu-id="cc171-620">This property is optional for all acquisition enabled items; that is, items of types WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, and WIA_CATEGORY_FILM.</span></span></p>
<p><span data-ttu-id="cc171-621">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</span><span class="sxs-lookup"><span data-stu-id="cc171-621">Type: <strong>VT_I4</strong>, Access: Read/Write or Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE.</span></span></p>
<p><span data-ttu-id="cc171-622">I valori possono essere compresi tra 1 e massimo VT_I4 (0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="cc171-622">Values can be from 1 to maximum VT_I4 (0xFFFF).</span></span> <span data-ttu-id="cc171-623">100, ad esempio, non prevede alcun ridimensionamento, 050 indica il ridimensionamento fino al 50% della dimensione originale e 200 indica il ridimensionamento fino al 200% delle dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="cc171-623">For example, 100 means no scaling, 050 means scaling down to 50% of the orignal size, and 200 means scaling up to 200% of the original size.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="cc171-624">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc171-624">Requirements</span></span>



| <span data-ttu-id="cc171-625">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc171-625">Requirement</span></span> | <span data-ttu-id="cc171-626">Valore</span><span class="sxs-lookup"><span data-stu-id="cc171-626">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc171-627">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc171-627">Minimum supported client</span></span><br/> | <span data-ttu-id="cc171-628">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cc171-628">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="cc171-629">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc171-629">Minimum supported server</span></span><br/> | <span data-ttu-id="cc171-630">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cc171-630">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cc171-631">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc171-631">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc171-632"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc171-632"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




