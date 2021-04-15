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
# <a name="camera-device-property-constants"></a>Costanti della proprietà del dispositivo della fotocamera

I dispositivi hardware Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema di Windows. Per altre informazioni, vedere [**costanti della proprietà del dispositivo comune**](-wia-wiaitempropcommondevice.md).

Le costanti della proprietà del dispositivo seguenti, con le stringhe associate, sono specifiche delle fotocamere digitali. Il prefisso "WIA \_ DPC \_ " indica una proprietà del dispositivo per le fotocamere e rappresenta la convenzione di denominazione usata in C/C++. Per finalità di scripting queste costanti usano il prefisso "CameraDevice" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.

> [!Note]  
> WIA non supporta le fotocamere in Windows Vista o versioni successive. Per queste versioni di Windows, usare l'API Windows Portable Device (WPD) descritta in Windows Driver Development Kit (DDK) per acquisire immagini dalle fotocamere.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td style="text-align: left;">Il numero di immagini eseguite dalla fotocamera. Minidriver crea e gestisce questa proprietà.<br/> Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td style="text-align: left;">Il numero di immagini che è possibile intraprendere, date le impostazioni correnti della proprietà. Se queste impostazioni cambiano e le modifiche influiscono sulle dimensioni delle immagini generate dal dispositivo della fotocamera, il minidriver WIA dovrebbe aggiornare il numero di immagini rimanenti. Minidriver crea e gestisce questa proprietà.<br/> Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td style="text-align: left;">Indica la modalità di esposizione corrente della fotocamera. Un'applicazione modifica questa proprietà per controllare la modalità di esposizione del dispositivo della fotocamera.<br/> Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> La tabella seguente contiene le sette costanti valide per questa proprietà.<br/> 
<table>
<thead>
<tr class="header">
<th>Modalità di esposizione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>La velocità e l'apertura dell'otturatore sono impostate dall'utente.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>La velocità e l'apertura dell'otturatore vengono impostati automaticamente dalla fotocamera.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>L'apertura viene impostata dall'utente e la fotocamera imposta automaticamente la velocità dell'otturatore.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>La velocità dell'otturatore viene impostata dall'utente e la fotocamera imposta automaticamente l'apertura.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>La velocità e l'apertura dell'otturatore vengono impostati automaticamente dalla fotocamera, ottimizzati per l'oggetto ancora.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>La velocità e l'apertura dell'otturatore vengono impostate automaticamente dalla fotocamera, ottimizzate per le scene che contengono movimento veloce.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>La velocità e l'apertura dell'otturatore vengono impostate automaticamente dalla fotocamera, ottimizzate per la fotografia verticale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td style="text-align: left;"><p>Consente la regolazione del punto di impostazione del controllo di esposizione automatica della fotocamera digitale. Ad esempio, un'impostazione zero non modifica il livello di esposizione automatica del set di impostazioni predefinite. Le unità sono in &quot; arresti &quot; ridimensionati in base a un fattore di 1000, per consentire i valori di arresto frazionario. Un'impostazione di 2000 corrisponde a due arresti più esposti (quattro volte più energia sul sensore), ottenendo immagini più luminose. L'impostazione-1000 corrisponde a una minore esposizione (uno-metà dell'energia sul sensore) che produce immagini più scure. I valori dell'impostazione sono in un sistema aggiuntivo di unità di esposizione fotografica (APEX). Questa proprietà può essere espressa come un elenco o un intervallo di valori. Questa proprietà viene in genere usata solo quando la proprietà <strong>WIA_DPC_EXPOSURE_MODE</strong> del dispositivo è impostata su EXPOSUREMODE_MANUAL.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td style="text-align: left;"><p>Corrisponde alla velocità dell'otturatore, in secondi, ridimensionata di 10.000. In genere, il dispositivo usa questa proprietà solo quando la proprietà <strong>WIA_DPC_EXPOSURE_MODE</strong> è impostata su EXPOSUREMODE_MANUAL o EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td style="text-align: left;"><p>Corrisponde all'apertura della lente, in unità del numero di arresto f ridimensionato di 100. L'impostazione di questa proprietà è in genere valida solo quando la proprietà <strong>WIA_DPC_EXPOSURE_MODE</strong> è impostata su EXPOSUREMODE_MANUAL o EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td style="text-align: left;"><p>Definisce l'impostazione della modalità Flash corrente per il dispositivo della fotocamera. Il driver di dispositivo enumera i valori supportati di questa proprietà. Un'applicazione scrive questa proprietà per impostare la modalità flash per il dispositivo della fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabella seguente contiene le sei costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Modalità flash</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>Il dispositivo della fotocamera determina le impostazioni Flash appropriate.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>Il dispositivo della fotocamera è configurato per Flash indipendentemente dalle condizioni di illuminazione correnti.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>Il dispositivo della fotocamera viene configurato in modo da <em>non</em> lampeggiare per le immagini acquisite.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>Il dispositivo della fotocamera determina le impostazioni Flash appropriate mediante la riduzione degli occhi rossi, indipendentemente dalle condizioni di illuminazione correnti.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>Il dispositivo della fotocamera è configurato per l'uso della riduzione degli occhi rossi e del flash indipendentemente dalle condizioni di illuminazione correnti.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>Il dispositivo della fotocamera è configurato per la sincronizzazione con unità flash esterne.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td style="text-align: left;"><p>Definisce l'impostazione della modalità messa a fuoco corrente per il dispositivo della fotocamera. Il driver di dispositivo enumera i valori supportati di questa proprietà. Un'applicazione scrive questa proprietà per impostare la modalità messa a fuoco per il dispositivo della fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Modalità messa a fuoco</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>Il dispositivo della fotocamera è configurato per consentire all'utente di concentrarsi manualmente.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>Il dispositivo della fotocamera è configurato per concentrarsi automaticamente.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>Il dispositivo della fotocamera è configurato per concentrarsi automaticamente usando le impostazioni della macro di intervallo breve.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td style="text-align: left;"><p>Definisce la fonte di alimentazione corrente per il dispositivo della fotocamera. Un'applicazione legge questa proprietà per determinare la fonte di alimentazione usata dalla fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Modalità risparmio di energia</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>Il dispositivo della fotocamera funziona su una scheda di alimentazione.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>Il dispositivo della fotocamera funziona con alimentazione a batteria.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td style="text-align: left;"><p>Percentuale di alimentazione a batteria lasciata per il funzionamento del dispositivo della fotocamera. Questo valore deve essere un numero intero compreso tra 0 e 100. Un'applicazione legge questa proprietà per determinare la durata della batteria rimanente del dispositivo della fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td style="text-align: left;"><p>Larghezza, in pixel, di un'immagine di anteprima da usare per le immagini appena acquisite. Un'applicazione legge questo valore per ottenere una dimensione stimata per la visualizzazione delle anteprime nell'interfaccia utente.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o di sola lettura (WIA_PROP_NONE), valori validi: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td style="text-align: left;"><p>Larghezza, in pixel, di un'immagine di anteprima da usare per le immagini appena acquisite. Un'applicazione legge questo valore per ottenere una dimensione stimata per la visualizzazione delle anteprime nell'interfaccia utente.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o di sola lettura (WIA_PROP_NONE), valori validi: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td style="text-align: left;"><p>Larghezza in pixel da usare per le immagini appena acquisite. L'elenco dei valori validi per questa proprietà presenta una corrispondenza uno-a-uno con l'elenco dei valori validi per la proprietà <strong>WIA_DPC_PICT_HEIGHT</strong> . Se la larghezza e l'altezza individuali sono impostate in modo lineare e ortogonale tra loro, possono essere espresse come un intervallo.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td style="text-align: left;"><p>Altezza, in pixel, da utilizzare per le immagini appena acquisite. L'elenco di valori validi per questa proprietà ha una corrispondenza uno-a-uno con l'elenco dei valori validi per la proprietà <strong>WIA_DPC_PICT_WIDTH</strong> . Se la larghezza e l'altezza individuali sono impostate in modo lineare e ortogonale tra loro, possono essere espresse come un intervallo.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td style="text-align: left;"><p>Progettato per essere approssimativamente lineare rispetto alla qualità dell'immagine percepita in un'ampia gamma di contenuto della scena e contiene un intervallo o un elenco di numeri interi. I numeri interi più piccoli vengono usati per rappresentare una qualità inferiore, ovvero la compressione massima, mentre i numeri interi più grandi vengono usati per rappresentare una qualità maggiore (ovvero la compressione minima). Le impostazioni disponibili in un dispositivo sono relative solo a tale dispositivo e sono quindi specifiche del dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td style="text-align: left;"><p>Tempo, in millisecondi, tra le acquisizioni di immagini in un'operazione di acquisizione Time-lapse.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td style="text-align: left;"><p>Il numero di immagini che il dispositivo tenta di acquisire durante un'acquisizione Time-lapse.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td style="text-align: left;"><p>Tempo, in millisecondi, tra le acquisizioni di immagini durante un'operazione di espansione.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td style="text-align: left;"><p>Il numero di immagini che il dispositivo tenta di acquisire durante un'operazione di espansione.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td style="text-align: left;"><p>Specifica la modalità di acquisizione dell'immagine speciale della fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Modalità effetto</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Acquisire un'immagine in modalità standard per la fotocamera.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Acquisisce un'immagine in scala di grigi.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Acquisire un'immagine seppia.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td style="text-align: left;"><p>Rapporto di zoom effettivo dell'immagine acquisita della fotocamera digitale, ridimensionato in base a un fattore di 10. Il valore 10 corrisponde all'assenza di zoom digitale (1X), ovvero la dimensione della scena standard acquisita dalla fotocamera. Un valore pari a 20 corrisponde a uno zoom 2X, in cui la fotocamera acquisisce un trimestre della dimensione della scena standard.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td style="text-align: left;"><p>Nitidezza percepita di un'immagine acquisita. Questa proprietà può utilizzare un elenco di valori o un intervallo di valori. Il valore minimo rappresenta il minor livello di nitidezza, mentre il valore massimo rappresenta la nitidezza massima. In genere, un valore all'interno dell'intervallo rappresenta una nitidezza normale o predefinita.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td style="text-align: left;"><p>Il contrasto percepito di un'immagine acquisita. Questa proprietà può contenere un elenco di valori o un intervallo di valori. Il valore minimo supportato rappresenta il minor numero di contrasto, mentre il valore massimo rappresenta il contrasto maggiore. In genere, un valore all'interno dell'intervallo rappresenta un contrasto normale o predefinito.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td style="text-align: left;"><p>Imposta la modalità di acquisizione dell'immagine.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Modalità acquisizione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Modalità normale per la fotocamera.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Acquisire più di un'immagine in rapida successione in base a quanto definito dai valori delle proprietà <strong>WIA_DPC_BURST_NUMBER</strong> e <strong>WIA_DPC_BURST_INTERVAL</strong> .</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Acquisire più di un'immagine in successione in base a quanto definito dalle proprietà <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td style="text-align: left;"><p>Valore che rappresenta l'intervallo di tempo, in millisecondi, che deve essere inserito tra il trigger di acquisizione e l'avvio effettivo dell'acquisizione dei dati. Questa proprietà non può essere utilizzata per descrivere l'intervallo tra i frame per l'avvio singolo, più acquisizioni, ad esempio il tempo di espansione o di scadenza, che hanno proprietà di intervallo separate <strong>WIA_DPC_BURST_INTERVAL</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. In questi casi, viene comunque utilizzato come ritardo iniziale prima che la prima immagine della serie venga acquisita, indipendentemente dal tempo tra i frame. Per nessun ritardo di acquisizione, questa proprietà deve essere impostata su zero.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td style="text-align: left;"><p>Consente di emulare le impostazioni della velocità della pellicola in una fotocamera digitale. Le impostazioni corrispondono alle designazioni ISO (ASA/DIN). In genere, un dispositivo supporta valori enumerati discreti, ma è possibile il controllo continuo su un intervallo di valori. Il valore 0xFFFF corrisponde all'impostazione ISO automatica.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Specifica la modalità utilizzata dalla fotocamera per regolare automaticamente l'impostazione di esposizione.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Modalità di misurazione dell'esposizione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Imposta l'esposizione in base a una media dell'intera scena.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Impostare l'esposizione in base a una media ponderata al centro.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Impostare l'esposizione in base a un modello a più punti.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Imposta l'esposizione in base a una posizione centrale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td style="text-align: left;"><p>Specifica la modalità utilizzata dalla fotocamera per regolare automaticamente lo stato attivo.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Modalità di misurazione dello stato attivo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Regolare lo stato attivo in base a una posizione centrale.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Regolare lo stato attivo in base a un modello a più punti.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td style="text-align: left;"><p>Distanza, in millimetri, tra il piano di acquisizione dell'immagine della fotocamera digitale e il punto di messa a fuoco. Il valore 0xFFFF corrisponde a un'impostazione maggiore di 655 metri.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td style="text-align: left;"><p>Lunghezza focale equivalente a 35mm. I valori di questa proprietà corrispondono alla lunghezza focale in millimetri moltiplicata per 100. La lunghezza focale determina lo zoom ottico.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td style="text-align: left;"><p>Stringa Unicode con terminazione null che rappresenta il guadagno rosso, verde e blu applicato ai dati dell'immagine, rispettivamente. 4:25:50, ad esempio, &quot; &quot; rappresenta un guadagno rosso di 4, un guadagno verde di 25 e un guadagno blu di 50.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td style="text-align: left;"><p>Specifica il modo in cui la fotocamera digitale pondera i canali dei colori.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Di seguito è riportato un elenco dei valori possibili per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Bilanciamento bianco</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>Il bilanciamento bianco viene impostato direttamente usando la proprietà <strong>WIA_DPC_RGB_GAIN</strong> .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>La fotocamera usa un meccanismo automatico per impostare il bilanciamento del bianco.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>La fotocamera determina l'impostazione di bilanciamento del bianco quando un utente preme il pulsante Acquisisci puntando la fotocamera a una superficie bianca.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'utilizzo in condizioni diurne.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>La fotocamera imposta il bilanciamento bianco su un valore appropriato per l'uso con una sorgente di luce fluorescente.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>La fotocamera imposta il bilanciamento bianco su un valore appropriato per l'uso con una sorgente di luce di tungsteno.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'uso con un flash elettronico.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td style="text-align: left;"><p>Descrive un URL. L'URL descritto da questo proroperty è quello in cui è possibile caricare immagini o oggetti, dopo che sono stati acquisiti dal dispositivo, in base a uno degli scenari seguenti.</p>
<ul>
<li>Un'applicazione WIA legge questa proprietà e consente all'utente di caricare automaticamente le immagini nell'URL.</li>
<li>Un'applicazione imposta l'URL e altri dispositivi (chioschi e così via) usano questa proprietà.</li>
</ul>
<p>Microsoft Windows non carica le immagini in modo autonomo.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td style="text-align: left;"><p>Nome del proprietario, ovvero l'utente corrente, del dispositivo. Il dispositivo usa questa proprietà per popolare il campo Artist in ogni immagine EXIF acquisita.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td style="text-align: left;"><p>Notifica sul copyright. Il dispositivo usa questa proprietà per popolare il campo copyright in ogni immagine EXIF acquisita.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




