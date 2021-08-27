---
description: Windows I dispositivi hardware WIA (Image Acquisition) hanno valori di proprietà archiviati nel Registro Windows sistema. Per altre informazioni, vedere Costanti comuni delle proprietà dei dispositivi.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Costanti delle proprietà del dispositivo fotocamera (Wiadef.h)
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
ms.openlocfilehash: f33e7f2dfd17e535e47026aee173feccb7c69584
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624197"
---
# <a name="camera-device-property-constants"></a>Costanti delle proprietà del dispositivo fotocamera

Windows I dispositivi hardware WIA (Image Acquisition) hanno valori di proprietà archiviati nel Registro Windows sistema. Per altre informazioni, vedere [**Costanti comuni delle proprietà dei dispositivi.**](-wia-wiaitempropcommondevice.md)

Le costanti delle proprietà del dispositivo seguenti, con le stringhe associate, sono specifiche delle fotocamere digitali. Il prefisso "WIA DPC" indica una proprietà del dispositivo per le fotocamere ed è la convenzione di denominazione \_ \_ usata in C/C++. A scopo di scripting, queste costanti usano il prefisso "CameraDevice" e fanno parte del tipo [enumerato WiaItemPropertyId.](-wia-wiaitempropertyid.md) Il nome del membro corrispondente dell'enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.

> [!Note]  
> WIA non supporta le fotocamere Windows Vista o versioni successive. Per queste versioni del Windows, usare l'API WPD (Portable Device) di Windows descritta in Windows Driver Development Kit (DDK) per acquisire immagini dalle fotocamere.

 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Costante/valore</th>
<th >Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td >Numero di immagini scattate dalla fotocamera. Il minidriver crea e gestisce questa proprietà.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td >Numero di immagini che è possibile scattare, in base alle impostazioni correnti delle proprietà. Se queste impostazioni cambiano e le modifiche influiscono sulle dimensioni delle immagini prodotti dal dispositivo fotocamera, il minidriver WIA deve aggiornare il numero di immagini rimanenti. Il minidriver crea e gestisce questa proprietà.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td >Indica la modalità di esposizione corrente della fotocamera. Un'applicazione modifica questa proprietà per controllare la modalità di esposizione del dispositivo fotocamera.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> Nella tabella seguente sono riportate le sette costanti valide per questa proprietà.<br/> 
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
<td>La velocità e l'apertura della velocità vengono impostate dall'utente.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>La velocità e l'apertura della velocità vengono impostate automaticamente dalla fotocamera.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>L'apertura viene impostata dall'utente e la fotocamera imposta automaticamente la velocità di apertura.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>La velocità di apertura viene impostata dall'utente e la fotocamera imposta automaticamente l'apertura.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>La velocità e l'apertura della luce vengono impostate automaticamente dalla fotocamera, ottimizzate per l'argomento ancora in questione.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>La velocità e l'apertura della luce vengono impostate automaticamente dalla fotocamera, ottimizzate per le scene contenenti movimento rapido.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>La velocità e l'apertura della luce vengono impostate automaticamente dalla fotocamera, ottimizzate per la ritrassura verticale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td ><p>Consente la regolazione del punto impostato del controllo di esposizione automatica della fotocamera digitale. Ad esempio, un'impostazione pari a zero non modifica il livello di esposizione automatica del set di impostazioni predefinite. Le unità sono in &quot; interruzioni &quot; ridimensionate di un fattore di 1000, per consentire valori di arresto frazionari. Un'impostazione di 2000 corrisponde a due arresti più esposizione (quattro volte più energia sul sensore), producendo immagini più luminosi. Un'impostazione di -1000 corrisponde a un'interruzione dell'esposizione in meno (metà dell'energia sul sensore) che produce immagini più scuri. I valori delle impostazioni sono in unità APEX (Additive System of Exposure). Questa proprietà può essere espressa come elenco o intervallo di valori. Questa proprietà viene in genere usata solo quando la proprietà WIA_DPC_EXPOSURE_MODE <strong>dispositivo</strong> è impostata su EXPOSUREMODE_MANUAL.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td ><p>Corrisponde alla velocità di velocità, in secondi, ridimensionata di 10.000. In genere, il dispositivo usa questa proprietà solo quando <strong>la proprietà WIA_DPC_EXPOSURE_MODE</strong> è impostata su EXPOSUREMODE_MANUAL o EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td ><p>Corrisponde all'apertura della lente, in unità del numero f-stop ridimensionato di 100. L'impostazione di questa proprietà è in genere valida solo quando la <strong>proprietà</strong> WIA_DPC_EXPOSURE_MODE è impostata su EXPOSUREMODE_MANUAL o EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td ><p>Definisce l'impostazione corrente della modalità flash per il dispositivo fotocamera. Il driver di dispositivo enumera i valori supportati di questa proprietà. Un'applicazione scrive questa proprietà per impostare la modalità flash per il dispositivo fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono elencate le sei costanti valide per questa proprietà.</p>

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
<td>Il dispositivo fotocamera determina le impostazioni flash appropriate.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>Il dispositivo fotocamera è configurato per eseguire il flash indipendentemente dalle condizioni di illuminazione correnti.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>Il dispositivo fotocamera è configurato in <em>modo da non</em> lampeggiare per le immagini scattate.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>Il dispositivo fotocamera determina le impostazioni flash appropriate usando la riduzione degli occhi rossi, indipendentemente dalle condizioni di illuminazione correnti.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>Il dispositivo fotocamera è configurato per l'uso della riduzione degli occhi rossi e del flash indipendentemente dalle condizioni di illuminazione correnti.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>Il dispositivo fotocamera è configurato per la sincronizzazione con unità flash esterne.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td ><p>Definisce l'impostazione corrente della modalità messa a fuoco per il dispositivo fotocamera. Il driver di dispositivo enumera i valori supportati di questa proprietà. Un'applicazione scrive questa proprietà per impostare la modalità messa a fuoco per il dispositivo fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>Il dispositivo fotocamera è configurato per consentire all'utente di concentrarsi manualmente.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>Il dispositivo fotocamera è configurato per la messa a fuoco automatica.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>Il dispositivo fotocamera è configurato per lo stato attivo automaticamente usando le impostazioni macro a breve raggio.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td ><p>Definisce la fonte di alimentazione corrente per il dispositivo fotocamera. Un'applicazione legge questa proprietà per determinare la fonte di alimentazione utilizzata dalla fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le due costanti valide con questa proprietà.</p>

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
<td>Il dispositivo fotocamera funziona su un adattatore di alimentazione.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>Il dispositivo fotocamera funziona con alimentazione a batteria.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td ><p>Percentuale di alimentazione della batteria lasciata per usare il dispositivo fotocamera. Questo valore deve essere un numero intero compreso tra 0 e 100. Un'applicazione legge questa proprietà per determinare la durata rimanente della batteria del dispositivo fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td ><p>Larghezza, in pixel, di un'immagine di anteprima da usare per le immagini appena acquisite. Un'applicazione legge questo valore per ottenere una dimensione stimata per la visualizzazione delle anteprime nell'interfaccia utente.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o Sola lettura (WIA_PROP_NONE), Valori validi: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td ><p>Larghezza, in pixel, di un'immagine di anteprima da usare per le immagini appena acquisite. Un'applicazione legge questo valore per ottenere una dimensione stimata per la visualizzazione delle anteprime nell'interfaccia utente.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o Sola lettura (WIA_PROP_NONE), Valori validi: WIA_PROP_LIST o WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td ><p>Larghezza in pixel da usare per le immagini appena acquisite. L'elenco di valori validi per questa proprietà ha una corrispondenza uno-a-uno con l'elenco di valori validi per la WIA_DPC_PICT_HEIGHT <strong>proprietà.</strong> Se la larghezza e l'altezza individuali sono impostabili in modo lineare e ortogonali tra loro, possono essere espresse come intervallo.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori <a href="-wia-property-attributes.md">validi:</a> WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td ><p>Altezza in pixel da usare per le immagini appena acquisite. L'elenco di valori validi per questa proprietà ha una corrispondenza uno-a-uno con l'elenco <strong>di</strong> valori validi per la WIA_DPC_PICT_WIDTH proprietà. Se la larghezza e l'altezza individuali sono impostabili in modo lineare e ortogonali tra loro, possono essere espresse come intervallo.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori <a href="-wia-property-attributes.md">validi:</a> WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td ><p>Progettato per essere approssimativamente lineare rispetto alla qualità dell'immagine percepita su un'ampia gamma di contenuti della scena e contiene un intervallo o un elenco di numeri interi. I numeri interi più piccoli vengono usati per rappresentare una qualità inferiore,ovvero la compressione massima, mentre i numeri interi più grandi vengono usati per rappresentare una qualità superiore, ovvero la compressione minima. Tutte le impostazioni disponibili in un dispositivo sono relative solo a tale dispositivo e sono quindi specifiche del dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori <a href="-wia-property-attributes.md">validi:</a> WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td ><p>Tempo, in millisecondi, tra le acquisizioni di immagini in un'operazione di acquisizione time-lapse.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td ><p>Numero di immagini che il dispositivo tenta di acquisire durante un'acquisizione time-lapse.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td ><p>Tempo, in millisecondi, tra le acquisizioni di immagini durante un'operazione di burst.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td ><p>Numero di immagini che il dispositivo tenta di acquisire durante un'operazione burst.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE,</a>WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td ><p>Specifica la modalità di acquisizione dell'immagine speciale della fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide con questa proprietà.</p>

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
<td>Acquisire un'immagine in scala di grigi.</td>
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
<td ><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td ><p>Rapporto di zoom effettivo dell'immagine acquisita della fotocamera digitale, ridimensionato di un fattore di 10. Il valore 10 corrisponde all'assenza di zoom digitale (1X), ovvero le dimensioni della scena standard acquisite dalla fotocamera. Il valore 20 corrisponde a uno zoom 2X, in cui un quarto delle dimensioni standard della scena viene acquisito dalla fotocamera.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori <a href="-wia-property-attributes.md">validi:</a> WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td ><p>Nitidezza percepita di un'immagine acquisita. Questa proprietà può usare un elenco di valori o un intervallo di valori. Il valore minimo rappresenta la quantità minima di nitidezza, mentre il valore massimo rappresenta la massima nitidezza. In genere, un valore al centro dell'intervallo rappresenta la nitidezza normale o predefinita.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori <a href="-wia-property-attributes.md">validi:</a> WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td ><p>Contrasto percepito di un'immagine acquisita. Questa proprietà può contenere un elenco di valori o un intervallo di valori. Il valore minimo supportato rappresenta la quantità minima di contrasto, mentre il valore massimo rappresenta il contrasto più elevato. In genere, un valore al centro dell'intervallo rappresenta il contrasto normale o predefinito.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori <a href="-wia-property-attributes.md">validi:</a> WIA_PROP_LIST o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td ><p>Imposta la modalità di acquisizione dell'immagine.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>Acquisire più di un'immagine in rapida successione, come definito dai valori delle proprietà WIA_DPC_BURST_NUMBER <strong>e</strong> <strong>WIA_DPC_BURST_INTERVAL.</strong></td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Acquisire più di un'immagine in successione, come definito dalle proprietà WIA_DPC_TIMELAPSE_NUMBER <strong>e</strong> <strong>WIA_DPC_TIMELAPSE_INTERVAL.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td ><p>Valore che rappresenta l'intervallo di tempo, in millisecondi, che deve essere inserito tra il trigger di acquisizione e l'avvio effettivo di Data Capture. Questa proprietà non deve essere usata per descrivere il tempo tra i fotogrammi per l'avvio singolo, più acquisizioni, ad esempio burst o lapse temporale, che hanno proprietà di intervallo separate <strong>WIA_DPC_BURST_INTERVAL</strong> e <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>. In questi casi, viene comunque utilizzato come ritardo iniziale prima dell'acquisizione della prima immagine della serie, indipendentemente dal tempo tra i fotogrammi. Per nessun ritardo di pre-incapsulamento, questa proprietà deve essere impostata su zero.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td ><p>Consente l'emulazione delle impostazioni di velocità della filmato su una fotocamera digitale. Le impostazioni corrispondono alle designazioni ISO (ASA/DIN). In genere, un dispositivo supporta valori enumerati discreti, ma è possibile un controllo continuo su un intervallo di valori. Il valore 0xFFFF corrisponde all'impostazione ISO automatica.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td ><p>Specifica la modalità utilizzata dalla fotocamera per regolare automaticamente l'impostazione di esposizione.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

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
<td>Impostare l'esposizione in base a un modello multispot.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Impostare l'esposizione in base a un punto centrale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td ><p>Specifica la modalità utilizzata dalla fotocamera per regolare automaticamente lo stato attivo.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>Regolare lo stato attivo in base a un punto centrale.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Regolare lo stato attivo in base a un modello multispot.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td ><p>Distanza, in millimetri, tra il piano di acquisizione dell'immagine della fotocamera digitale e il punto di messa a fuoco. Il valore 0xFFFF corrisponde a un'impostazione maggiore di 655 metri.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td ><p>Lunghezza focale equivalente a 35 mm. I valori di questa proprietà corrispondono alla lunghezza focale in millimetri moltiplicata per 100. La lunghezza focale determina lo zoom ottico.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td ><p>Stringa Unicode con terminazione Null che rappresenta il guadagno rosso, verde e blu applicato rispettivamente ai dati dell'immagine. Ad esempio, 4:25:50 rappresenta un guadagno rosso di 4, un guadagno verde di 25 e un guadagno &quot; &quot; blu di 50.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td ><p>Specifica il modo in cui la fotocamera digitale pondera i canali di colore.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Di seguito è riportato un elenco di valori possibili per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Bilanciamento del bianco</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>Il bilanciamento del bianco viene impostato direttamente usando <strong>WIA_DPC_RGB_GAIN</strong> proprietà .</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>La fotocamera usa un meccanismo automatico per impostare il bilanciamento del bianco.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>La fotocamera determina l'impostazione del bilanciamento del bianco quando un utente preme il pulsante di acquisizione puntando la fotocamera su una superficie bianca.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'uso in condizioni di ora legale.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'uso con una sorgente di luce fluorescente.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>La fotocamera imposta il bilanciamento del bianco su un valore appropriato per l'uso con una sorgente di luce tungsteno.</td>
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
<td ><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td ><p>Descrive un URL. L'URL descritto da questa proroperty è quello in cui è possibile caricare immagini o oggetti, dopo che sono stati acquisiti dal dispositivo, in base a uno degli scenari seguenti.</p>
<ul>
<li>Un'applicazione WIA legge questa proprietà e consente all'utente di caricare automaticamente le immagini nell'URL.</li>
<li>Un'applicazione imposta l'URL e altri dispositivi (chioschi e così via) usano questa proprietà.</li>
</ul>
<p>Microsoft Windows non carica le immagini da solo.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td ><p>Nome del proprietario ( che è l'utente corrente) del dispositivo. Il dispositivo usa questa proprietà per popolare il campo Artista in ogni immagine EXIF che acquisisce.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td ><p>Notifica del copyright. Il dispositivo usa questa proprietà per popolare il campo Copyright in ogni immagine EXIF che acquisisce.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




