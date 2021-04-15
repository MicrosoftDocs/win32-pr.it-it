---
description: I dispositivi hardware Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema di Windows. Per altre informazioni, vedere costanti della proprietà del dispositivo comune.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Costanti della proprietà del dispositivo della fotocamera (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485044"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="34e69-104">Costanti della proprietà del dispositivo della fotocamera</span><span class="sxs-lookup"><span data-stu-id="34e69-104">Camera Device Property Constants</span></span>

<span data-ttu-id="34e69-105">I dispositivi hardware Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="34e69-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="34e69-106">Per altre informazioni, vedere [**costanti della proprietà del dispositivo comune**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="34e69-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="34e69-107">Le costanti della proprietà del dispositivo seguenti, con le stringhe associate, sono specifiche delle fotocamere digitali.</span><span class="sxs-lookup"><span data-stu-id="34e69-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="34e69-108">Il prefisso "WIA \_ DPC \_ " indica una proprietà del dispositivo per le fotocamere e rappresenta la convenzione di denominazione usata in C/C++.</span><span class="sxs-lookup"><span data-stu-id="34e69-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="34e69-109">Per finalità di scripting queste costanti usano il prefisso "CameraDevice" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="34e69-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="34e69-110">Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="34e69-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="34e69-111">WIA non supporta le fotocamere in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="34e69-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="34e69-112">Per queste versioni di Windows, usare l'API Windows Portable Device (WPD) descritta in Windows Driver Development Kit (DDK) per acquisire immagini dalle fotocamere.</span><span class="sxs-lookup"><span data-stu-id="34e69-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="34e69-113">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="34e69-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="34e69-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="34e69-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="34e69-116">Il numero di immagini eseguite dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="34e69-117">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="34e69-118">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="34e69-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="34e69-120">Il numero di immagini che è possibile intraprendere, date le impostazioni correnti della proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="34e69-121">Se queste impostazioni cambiano e le modifiche influiscono sulle dimensioni delle immagini generate dal dispositivo della fotocamera, il minidriver WIA dovrebbe aggiornare il numero di immagini rimanenti.</span><span class="sxs-lookup"><span data-stu-id="34e69-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="34e69-122">Minidriver crea e gestisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="34e69-123">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="34e69-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="34e69-125">Indica la modalità di esposizione corrente della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="34e69-126">Un'applicazione modifica questa proprietà per controllare la modalità di esposizione del dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="34e69-127">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="34e69-128">La tabella seguente contiene le sette costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-129">Modalità di esposizione</span><span class="sxs-lookup"><span data-stu-id="34e69-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="34e69-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="34e69-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="34e69-132">La velocità e l'apertura dell'otturatore sono impostate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="34e69-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="34e69-134">La velocità e l'apertura dell'otturatore vengono impostati automaticamente dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="34e69-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="34e69-136">L'apertura viene impostata dall'utente e la fotocamera imposta automaticamente la velocità dell'otturatore.</span><span class="sxs-lookup"><span data-stu-id="34e69-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="34e69-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="34e69-138">La velocità dell'otturatore viene impostata dall'utente e la fotocamera imposta automaticamente l'apertura.</span><span class="sxs-lookup"><span data-stu-id="34e69-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="34e69-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="34e69-140">La velocità e l'apertura dell'otturatore vengono impostati automaticamente dalla fotocamera, ottimizzati per l'oggetto ancora.</span><span class="sxs-lookup"><span data-stu-id="34e69-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="34e69-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="34e69-142">La velocità e l'apertura dell'otturatore vengono impostate automaticamente dalla fotocamera, ottimizzate per le scene che contengono movimento veloce.</span><span class="sxs-lookup"><span data-stu-id="34e69-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="34e69-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="34e69-144">La velocità e l'apertura dell'otturatore vengono impostate automaticamente dalla fotocamera, ottimizzate per la fotografia verticale.</span><span class="sxs-lookup"><span data-stu-id="34e69-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="34e69-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-146">Consente la regolazione del punto di impostazione del controllo di esposizione automatica della fotocamera digitale.</span><span class="sxs-lookup"><span data-stu-id="34e69-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="34e69-147">Ad esempio, un'impostazione zero non modifica il livello di esposizione automatica del set di impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="34e69-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="34e69-148">Le unità sono in &quot; arresti &quot; ridimensionati in base a un fattore di 1000, per consentire i valori di arresto frazionario.</span><span class="sxs-lookup"><span data-stu-id="34e69-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="34e69-149">Un'impostazione di 2000 corrisponde a due arresti più esposti (quattro volte più energia sul sensore), ottenendo immagini più luminose.</span><span class="sxs-lookup"><span data-stu-id="34e69-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="34e69-150">L'impostazione-1000 corrisponde a una minore esposizione (uno-metà dell'energia sul sensore) che produce immagini più scure.</span><span class="sxs-lookup"><span data-stu-id="34e69-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="34e69-151">I valori dell'impostazione sono in un sistema aggiuntivo di unità di esposizione fotografica (APEX).</span><span class="sxs-lookup"><span data-stu-id="34e69-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="34e69-152">Questa proprietà può essere espressa come un elenco o un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="34e69-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="34e69-153">Questa proprietà viene in genere usata solo quando la proprietà <strong>WIA_DPC_EXPOSURE_MODE</strong> del dispositivo è impostata su EXPOSUREMODE_MANUAL.</span><span class="sxs-lookup"><span data-stu-id="34e69-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="34e69-154">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="34e69-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="34e69-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-156">Corrisponde alla velocità dell'otturatore, in secondi, ridimensionata di 10.000.</span><span class="sxs-lookup"><span data-stu-id="34e69-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="34e69-157">In genere, il dispositivo usa questa proprietà solo quando la proprietà <strong>WIA_DPC_EXPOSURE_MODE</strong> è impostata su EXPOSUREMODE_MANUAL o EXPOSUREMODE_SHUTTER_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="34e69-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="34e69-158">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="34e69-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="34e69-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-160">Corrisponde all'apertura della lente, in unità del numero di arresto f ridimensionato di 100.</span><span class="sxs-lookup"><span data-stu-id="34e69-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="34e69-161">L'impostazione di questa proprietà è in genere valida solo quando la proprietà <strong>WIA_DPC_EXPOSURE_MODE</strong> è impostata su EXPOSUREMODE_MANUAL o EXPOSUREMODE_APERTURE_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="34e69-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="34e69-162">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="34e69-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-164">Definisce l'impostazione della modalità Flash corrente per il dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="34e69-165">Il driver di dispositivo enumera i valori supportati di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="34e69-166">Un'applicazione scrive questa proprietà per impostare la modalità flash per il dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="34e69-167">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="34e69-168">La tabella seguente contiene le sei costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-169">Modalità flash</span><span class="sxs-lookup"><span data-stu-id="34e69-169">Flash Mode</span></span></th>
<th><span data-ttu-id="34e69-170">Definizione</span><span class="sxs-lookup"><span data-stu-id="34e69-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="34e69-172">Il dispositivo della fotocamera determina le impostazioni Flash appropriate.</span><span class="sxs-lookup"><span data-stu-id="34e69-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="34e69-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="34e69-174">Il dispositivo della fotocamera è configurato per Flash indipendentemente dalle condizioni di illuminazione correnti.</span><span class="sxs-lookup"><span data-stu-id="34e69-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="34e69-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="34e69-176">Il dispositivo della fotocamera viene configurato in modo da <em>non</em> lampeggiare per le immagini acquisite.</span><span class="sxs-lookup"><span data-stu-id="34e69-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="34e69-178">Il dispositivo della fotocamera determina le impostazioni Flash appropriate mediante la riduzione degli occhi rossi, indipendentemente dalle condizioni di illuminazione correnti.</span><span class="sxs-lookup"><span data-stu-id="34e69-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="34e69-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="34e69-180">Il dispositivo della fotocamera è configurato per l'uso della riduzione degli occhi rossi e del flash indipendentemente dalle condizioni di illuminazione correnti.</span><span class="sxs-lookup"><span data-stu-id="34e69-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="34e69-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="34e69-182">Il dispositivo della fotocamera è configurato per la sincronizzazione con unità flash esterne.</span><span class="sxs-lookup"><span data-stu-id="34e69-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="34e69-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-184">Definisce l'impostazione della modalità messa a fuoco corrente per il dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="34e69-185">Il driver di dispositivo enumera i valori supportati di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="34e69-186">Un'applicazione scrive questa proprietà per impostare la modalità messa a fuoco per il dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="34e69-187">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="34e69-188">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-189">Modalità messa a fuoco</span><span class="sxs-lookup"><span data-stu-id="34e69-189">Focus Mode</span></span></th>
<th><span data-ttu-id="34e69-190">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="34e69-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="34e69-192">Il dispositivo della fotocamera è configurato per consentire all'utente di concentrarsi manualmente.</span><span class="sxs-lookup"><span data-stu-id="34e69-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="34e69-194">Il dispositivo della fotocamera è configurato per concentrarsi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="34e69-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="34e69-196">Il dispositivo della fotocamera è configurato per concentrarsi automaticamente usando le impostazioni della macro di intervallo breve.</span><span class="sxs-lookup"><span data-stu-id="34e69-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="34e69-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-198">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-199">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="34e69-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-201">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-202">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="34e69-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-204">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-205">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="34e69-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-207">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-208">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="34e69-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-210">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-211">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="34e69-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-213">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-214">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="34e69-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-216">Definisce la fonte di alimentazione corrente per il dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="34e69-217">Un'applicazione legge questa proprietà per determinare la fonte di alimentazione usata dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="34e69-218">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="34e69-219">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-220">Modalità risparmio di energia</span><span class="sxs-lookup"><span data-stu-id="34e69-220">Power Mode</span></span></th>
<th><span data-ttu-id="34e69-221">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="34e69-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="34e69-223">Il dispositivo della fotocamera funziona su una scheda di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="34e69-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="34e69-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="34e69-225">Il dispositivo della fotocamera funziona con alimentazione a batteria.</span><span class="sxs-lookup"><span data-stu-id="34e69-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="34e69-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-227">Percentuale di alimentazione a batteria lasciata per il funzionamento del dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="34e69-228">Questo valore deve essere un numero intero compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="34e69-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="34e69-229">Un'applicazione legge questa proprietà per determinare la durata della batteria rimanente del dispositivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="34e69-230">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="34e69-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-232">Larghezza, in pixel, di un'immagine di anteprima da usare per le immagini appena acquisite.</span><span class="sxs-lookup"><span data-stu-id="34e69-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="34e69-233">Un'applicazione legge questo valore per ottenere una dimensione stimata per la visualizzazione delle anteprime nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="34e69-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="34e69-234">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o di sola lettura (WIA_PROP_NONE), valori validi: WIA_PROP_LIST o WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="34e69-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="34e69-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-236">Larghezza, in pixel, di un'immagine di anteprima da usare per le immagini appena acquisite.</span><span class="sxs-lookup"><span data-stu-id="34e69-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="34e69-237">Un'applicazione legge questo valore per ottenere una dimensione stimata per la visualizzazione delle anteprime nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="34e69-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="34e69-238">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o di sola lettura (WIA_PROP_NONE), valori validi: WIA_PROP_LIST o WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="34e69-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="34e69-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-240">Larghezza in pixel da usare per le immagini appena acquisite.</span><span class="sxs-lookup"><span data-stu-id="34e69-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="34e69-241">L'elenco dei valori validi per questa proprietà presenta una corrispondenza uno-a-uno con l'elenco dei valori validi per la proprietà <strong>WIA_DPC_PICT_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="34e69-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="34e69-242">Se la larghezza e l'altezza individuali sono impostate in modo lineare e ortogonale tra loro, possono essere espresse come un intervallo.</span><span class="sxs-lookup"><span data-stu-id="34e69-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="34e69-243">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="34e69-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-245">Altezza, in pixel, da utilizzare per le immagini appena acquisite.</span><span class="sxs-lookup"><span data-stu-id="34e69-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="34e69-246">L'elenco di valori validi per questa proprietà ha una corrispondenza uno-a-uno con l'elenco dei valori validi per la proprietà <strong>WIA_DPC_PICT_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="34e69-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="34e69-247">Se la larghezza e l'altezza individuali sono impostate in modo lineare e ortogonale tra loro, possono essere espresse come un intervallo.</span><span class="sxs-lookup"><span data-stu-id="34e69-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="34e69-248">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="34e69-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-250">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-251">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="34e69-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-253">Progettato per essere approssimativamente lineare rispetto alla qualità dell'immagine percepita in un'ampia gamma di contenuto della scena e contiene un intervallo o un elenco di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="34e69-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="34e69-254">I numeri interi più piccoli vengono usati per rappresentare una qualità inferiore, ovvero la compressione massima, mentre i numeri interi più grandi vengono usati per rappresentare una qualità maggiore (ovvero la compressione minima).</span><span class="sxs-lookup"><span data-stu-id="34e69-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="34e69-255">Le impostazioni disponibili in un dispositivo sono relative solo a tale dispositivo e sono quindi specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34e69-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="34e69-256">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="34e69-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-258">Riservato, non usare.</span><span class="sxs-lookup"><span data-stu-id="34e69-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="34e69-259">Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="34e69-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-261">Tempo, in millisecondi, tra le acquisizioni di immagini in un'operazione di acquisizione Time-lapse.</span><span class="sxs-lookup"><span data-stu-id="34e69-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="34e69-262">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="34e69-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-264">Il numero di immagini che il dispositivo tenta di acquisire durante un'acquisizione Time-lapse.</span><span class="sxs-lookup"><span data-stu-id="34e69-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="34e69-265">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="34e69-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-267">Tempo, in millisecondi, tra le acquisizioni di immagini durante un'operazione di espansione.</span><span class="sxs-lookup"><span data-stu-id="34e69-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="34e69-268">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="34e69-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-270">Il numero di immagini che il dispositivo tenta di acquisire durante un'operazione di espansione.</span><span class="sxs-lookup"><span data-stu-id="34e69-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="34e69-271">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="34e69-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-273">Specifica la modalità di acquisizione dell'immagine speciale della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="34e69-274">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="34e69-275">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-276">Modalità effetto</span><span class="sxs-lookup"><span data-stu-id="34e69-276">Effect Mode</span></span></th>
<th><span data-ttu-id="34e69-277">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="34e69-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="34e69-279">Acquisire un'immagine in modalità standard per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="34e69-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="34e69-281">Acquisisce un'immagine in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="34e69-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="34e69-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="34e69-283">Acquisire un'immagine seppia.</span><span class="sxs-lookup"><span data-stu-id="34e69-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="34e69-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-285">Rapporto di zoom effettivo dell'immagine acquisita della fotocamera digitale, ridimensionato in base a un fattore di 10.</span><span class="sxs-lookup"><span data-stu-id="34e69-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="34e69-286">Il valore 10 corrisponde all'assenza di zoom digitale (1X), ovvero la dimensione della scena standard acquisita dalla fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="34e69-287">Un valore pari a 20 corrisponde a uno zoom 2X, in cui la fotocamera acquisisce un trimestre della dimensione della scena standard.</span><span class="sxs-lookup"><span data-stu-id="34e69-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="34e69-288">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="34e69-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-290">Nitidezza percepita di un'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="34e69-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="34e69-291">Questa proprietà può utilizzare un elenco di valori o un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="34e69-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="34e69-292">Il valore minimo rappresenta il minor livello di nitidezza, mentre il valore massimo rappresenta la nitidezza massima.</span><span class="sxs-lookup"><span data-stu-id="34e69-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="34e69-293">In genere, un valore all'interno dell'intervallo rappresenta una nitidezza normale o predefinita.</span><span class="sxs-lookup"><span data-stu-id="34e69-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="34e69-294">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="34e69-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-296">Il contrasto percepito di un'immagine acquisita.</span><span class="sxs-lookup"><span data-stu-id="34e69-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="34e69-297">Questa proprietà può contenere un elenco di valori o un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="34e69-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="34e69-298">Il valore minimo supportato rappresenta il minor numero di contrasto, mentre il valore massimo rappresenta il contrasto maggiore.</span><span class="sxs-lookup"><span data-stu-id="34e69-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="34e69-299">In genere, un valore all'interno dell'intervallo rappresenta un contrasto normale o predefinito.</span><span class="sxs-lookup"><span data-stu-id="34e69-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="34e69-300">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="34e69-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-302">Imposta la modalità di acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="34e69-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="34e69-303">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="34e69-304">Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-305">Modalità acquisizione</span><span class="sxs-lookup"><span data-stu-id="34e69-305">Capture Mode</span></span></th>
<th><span data-ttu-id="34e69-306">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="34e69-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="34e69-308">Modalità normale per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="34e69-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="34e69-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="34e69-310">Acquisire più di un'immagine in rapida successione in base a quanto definito dai valori delle proprietà <strong>WIA_DPC_BURST_NUMBER</strong> e <strong>WIA_DPC_BURST_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="34e69-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="34e69-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="34e69-312">Acquisire più di un'immagine in successione in base a quanto definito dalle proprietà <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="34e69-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="34e69-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-314">Valore che rappresenta l'intervallo di tempo, in millisecondi, che deve essere inserito tra il trigger di acquisizione e l'avvio effettivo dell'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="34e69-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="34e69-315">Questa proprietà non può essere utilizzata per descrivere l'intervallo tra i frame per l'avvio singolo, più acquisizioni, ad esempio il tempo di espansione o di scadenza, che hanno proprietà di intervallo separate <strong>WIA_DPC_BURST_INTERVAL</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="34e69-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="34e69-316">In questi casi, viene comunque utilizzato come ritardo iniziale prima che la prima immagine della serie venga acquisita, indipendentemente dal tempo tra i frame.</span><span class="sxs-lookup"><span data-stu-id="34e69-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="34e69-317">Per nessun ritardo di acquisizione, questa proprietà deve essere impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="34e69-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="34e69-318">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="34e69-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-320">Consente di emulare le impostazioni della velocità della pellicola in una fotocamera digitale.</span><span class="sxs-lookup"><span data-stu-id="34e69-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="34e69-321">Le impostazioni corrispondono alle designazioni ISO (ASA/DIN).</span><span class="sxs-lookup"><span data-stu-id="34e69-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="34e69-322">In genere, un dispositivo supporta valori enumerati discreti, ma è possibile il controllo continuo su un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="34e69-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="34e69-323">Il valore 0xFFFF corrisponde all'impostazione ISO automatica.</span><span class="sxs-lookup"><span data-stu-id="34e69-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="34e69-324">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="34e69-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-326">Specifica la modalità utilizzata dalla fotocamera per regolare automaticamente l'impostazione di esposizione.</span><span class="sxs-lookup"><span data-stu-id="34e69-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="34e69-327">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-328">Modalità di misurazione dell'esposizione</span><span class="sxs-lookup"><span data-stu-id="34e69-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="34e69-329">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="34e69-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="34e69-331">Imposta l'esposizione in base a una media dell'intera scena.</span><span class="sxs-lookup"><span data-stu-id="34e69-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="34e69-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="34e69-333">Impostare l'esposizione in base a una media ponderata al centro.</span><span class="sxs-lookup"><span data-stu-id="34e69-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="34e69-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="34e69-335">Impostare l'esposizione in base a un modello a più punti.</span><span class="sxs-lookup"><span data-stu-id="34e69-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="34e69-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="34e69-337">Imposta l'esposizione in base a una posizione centrale.</span><span class="sxs-lookup"><span data-stu-id="34e69-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="34e69-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-339">Specifica la modalità utilizzata dalla fotocamera per regolare automaticamente lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="34e69-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="34e69-340">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="34e69-341">Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-342">Modalità di misurazione dello stato attivo</span><span class="sxs-lookup"><span data-stu-id="34e69-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="34e69-343">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="34e69-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="34e69-345">Regolare lo stato attivo in base a una posizione centrale.</span><span class="sxs-lookup"><span data-stu-id="34e69-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="34e69-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="34e69-347">Regolare lo stato attivo in base a un modello a più punti.</span><span class="sxs-lookup"><span data-stu-id="34e69-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="34e69-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-349">Distanza, in millimetri, tra il piano di acquisizione dell'immagine della fotocamera digitale e il punto di messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="34e69-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="34e69-350">Il valore 0xFFFF corrisponde a un'impostazione maggiore di 655 metri.</span><span class="sxs-lookup"><span data-stu-id="34e69-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="34e69-351">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="34e69-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="34e69-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-353">Lunghezza focale equivalente a 35mm.</span><span class="sxs-lookup"><span data-stu-id="34e69-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="34e69-354">I valori di questa proprietà corrispondono alla lunghezza focale in millimetri moltiplicata per 100.</span><span class="sxs-lookup"><span data-stu-id="34e69-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="34e69-355">La lunghezza focale determina lo zoom ottico.</span><span class="sxs-lookup"><span data-stu-id="34e69-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="34e69-356">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="34e69-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-358">Stringa Unicode con terminazione null che rappresenta il guadagno rosso, verde e blu applicato ai dati dell'immagine, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="34e69-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="34e69-359">4:25:50, ad esempio, &quot; &quot; rappresenta un guadagno rosso di 4, un guadagno verde di 25 e un guadagno blu di 50.</span><span class="sxs-lookup"><span data-stu-id="34e69-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="34e69-360">Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="34e69-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-362">Specifica il modo in cui la fotocamera digitale pondera i canali dei colori.</span><span class="sxs-lookup"><span data-stu-id="34e69-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="34e69-363">Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="34e69-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="34e69-364">Di seguito è riportato un elenco dei valori possibili per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34e69-365">Bilanciamento bianco</span><span class="sxs-lookup"><span data-stu-id="34e69-365">White Balance</span></span></th>
<th><span data-ttu-id="34e69-366">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e69-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34e69-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="34e69-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="34e69-368">Il bilanciamento bianco viene impostato direttamente usando la proprietà <strong>WIA_DPC_RGB_GAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="34e69-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="34e69-370">La fotocamera usa un meccanismo automatico per impostare il bilanciamento del bianco.</span><span class="sxs-lookup"><span data-stu-id="34e69-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="34e69-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="34e69-372">La fotocamera determina l'impostazione di bilanciamento del bianco quando un utente preme il pulsante Acquisisci puntando la fotocamera a una superficie bianca.</span><span class="sxs-lookup"><span data-stu-id="34e69-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="34e69-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="34e69-374">La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'utilizzo in condizioni diurne.</span><span class="sxs-lookup"><span data-stu-id="34e69-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="34e69-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="34e69-376">La fotocamera imposta il bilanciamento bianco su un valore appropriato per l'uso con una sorgente di luce fluorescente.</span><span class="sxs-lookup"><span data-stu-id="34e69-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34e69-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="34e69-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="34e69-378">La fotocamera imposta il bilanciamento bianco su un valore appropriato per l'uso con una sorgente di luce di tungsteno.</span><span class="sxs-lookup"><span data-stu-id="34e69-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34e69-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="34e69-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="34e69-380">La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'uso con un flash elettronico.</span><span class="sxs-lookup"><span data-stu-id="34e69-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="34e69-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-382">Descrive un URL.</span><span class="sxs-lookup"><span data-stu-id="34e69-382">Describes a URL.</span></span> <span data-ttu-id="34e69-383">L'URL descritto da questo proroperty è quello in cui è possibile caricare immagini o oggetti, dopo che sono stati acquisiti dal dispositivo, in base a uno degli scenari seguenti.</span><span class="sxs-lookup"><span data-stu-id="34e69-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="34e69-384">Un'applicazione WIA legge questa proprietà e consente all'utente di caricare automaticamente le immagini nell'URL.</span><span class="sxs-lookup"><span data-stu-id="34e69-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="34e69-385">Un'applicazione imposta l'URL e altri dispositivi (chioschi e così via) usano questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="34e69-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="34e69-386">Microsoft Windows non carica le immagini in modo autonomo.</span><span class="sxs-lookup"><span data-stu-id="34e69-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="34e69-387">Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="34e69-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-389">Nome del proprietario, ovvero l'utente corrente, del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34e69-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="34e69-390">Il dispositivo usa questa proprietà per popolare il campo Artist in ogni immagine EXIF acquisita.</span><span class="sxs-lookup"><span data-stu-id="34e69-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="34e69-391">Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="34e69-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span><span class="sxs-lookup"><span data-stu-id="34e69-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="34e69-393">Notifica sul copyright.</span><span class="sxs-lookup"><span data-stu-id="34e69-393">The copyright notification.</span></span> <span data-ttu-id="34e69-394">Il dispositivo usa questa proprietà per popolare il campo copyright in ogni immagine EXIF acquisita.</span><span class="sxs-lookup"><span data-stu-id="34e69-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="34e69-395">Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="34e69-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="34e69-396">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34e69-396">Requirements</span></span>



| <span data-ttu-id="34e69-397">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e69-397">Requirement</span></span> | <span data-ttu-id="34e69-398">Valore</span><span class="sxs-lookup"><span data-stu-id="34e69-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34e69-399">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34e69-399">Minimum supported client</span></span><br/> | <span data-ttu-id="34e69-400">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="34e69-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="34e69-401">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34e69-401">Minimum supported server</span></span><br/> | <span data-ttu-id="34e69-402">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34e69-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="34e69-403">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34e69-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="34e69-404"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e69-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




