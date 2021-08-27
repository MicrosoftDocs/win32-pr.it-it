---
description: Windows I dispositivi hardware WIA (Image Acquisition) hanno valori di proprietà archiviati nel registro Windows immagini.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Costanti delle proprietà del dispositivo scanner (Wiadef.h)
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
ms.openlocfilehash: d9e7afee9b5b639c21e52dc797e7ad42a6ee0dd0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627187"
---
# <a name="scanner-device-property-constants"></a>Costanti delle proprietà del dispositivo scanner

Windows I dispositivi hardware WIA (Image Acquisition) hanno valori di proprietà archiviati nel registro Windows immagini. Per altre informazioni, vedere [**Costanti comuni delle proprietà dei dispositivi.**](-wia-wiaitempropcommondevice.md) Le costanti delle proprietà del dispositivo seguenti, con le stringhe associate, sono specifiche per gli scanner di immagini digitali.

Il prefisso "WIA DPS" indica una proprietà del dispositivo per i dispositivi scanner ed è la convenzione di denominazione \_ \_ usata in C/C++. A scopo di scripting, queste costanti usano il prefisso "ScannerDevice" e fanno parte del tipo [enumerato WiaItemPropertyId.](-wia-wiaitempropertyid.md) Il nome del membro corrispondente dell'enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



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
<td ><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
Questa proprietà è supportata solo in Windows Vista e versioni successive.
</blockquote>
<br/> Contiene un identificatore univoco dell'istanza della funzione per un dispositivo scanner di servizi Web. Questo identificatore rappresenta il servizio Web nel dispositivo scanner con cui comunica il mini driver WIA. Non è necessario presunzioni sulla forma di questo identificatore. Il mini driver WIA crea e gestisce questa proprietà. <br/> Le applicazioni WIA possono usare il valore di WIA_DPS_DEVICE_ID per trovare, usando l'API di individuazione delle funzioni, l'oggetto istanza della funzione che rappresenta il dispositivo scanner dei servizi Web usato nella sessione WIA 2.0 corrente.<br/> Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td >Riservato, non usare.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td >Riservato, non usare.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td >Contiene le funzionalità dello scanner. Il minidriver crea e gestisce questa proprietà. <br/> Un'applicazione legge questa proprietà per determinare se per lo scanner è installato un feeder di documenti, un alimentatore di documenti o un duplex. Questa proprietà viene usata anche per definire ulteriormente le funzionalità installate.<br/> Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Nella tabella seguente vengono descritte le costanti valide solo con Windows 7.<br/> 
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>Per lo scanner è installato un gestore di documenti automatico.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Nella tabella seguente vengono descritte le costanti valide con Windows 7 e Windows Vista.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>Il dispositivo supporta la configurazione avanzata dell'analisi duplex. Usare WIA_IPS_DUPLEX_SETTINGS per passare dall'uso di configurazioni duplex di base a configurazioni duplex avanzate.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>Lo scanner può rilevare quando l'adattatore di trasparenza/film è pronto per l'analisi.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>Lo scanner può rilevare la presenza di documenti nell'archiviazione interna.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>Lo scanner è dotato di un adattatore di scansione trasparente/film.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>Lo scanner è dotato di un dispositivo di archiviazione immagini interno.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Nella tabella seguente vengono descritte le costanti valide con Windows XP o versioni successive.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>Lo scanner può rilevare un documento nell'alimentatore.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>Lo scanner è in grado di rilevare un documento sulla pistoiola bi flat.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>Lo scanner può rilevare un documento nell'alimentatore solo eseguendo l'analisi.</td>
</tr>
<tr class="even">
<td>DUP</td>
<td>Lo scanner ha un duplexer.</td>
</tr>
<tr class="odd">
<td>NUTRIRE</td>
<td>Per lo scanner è installato un gestore di documenti automatico.</td>
</tr>
<tr class="even">
<td>PIATTO</td>
<td>Lo scanner ha un pistoio bi flat.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Nella tabella seguente vengono descritte le costanti valide solo con Windows XP. Questi valori sono stati deprecati per Windows 7 e Windows Vista e non devono essere usati.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>Lo scanner può rilevare una richiesta di analisi duplex da parte dell'utente.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>Lo scanner può indicare quando è installato il duplexer.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>Lo scanner può indicare quando è installato l'alimentatore automatico di documenti.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'origine e la modalità di acquisizione dello scanner corrente. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare l'origine di acquisizione corrente dello scanner o per scrivere questa proprietà per impostare l'origine e la modalità dello scanner. Inoltre, le applicazioni usano questa proprietà per abilitare e disabilitare la funzionalità duplexer.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Nella tabella seguente sono elencate le dieci costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ALIMENTATORE</td>
<td>Eseguire la scansione usando l'alimentatore di documenti.</td>
</tr>
<tr class="even">
<td>PIANALE</td>
<td>Eseguire la scansione usando flatbed.</td>
</tr>
<tr class="odd">
<td>DUPLEX</td>
<td>Analisi tramite operazioni duplexer.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Abilita l'alimentazione automatica del documento successivo dopo un'analisi.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Analizzare prima la parte anteriore del documento. Questo valore è valido quando duPLEX è impostato.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Analizzare prima la parte posteriore del documento. Questo valore è valido quando duPLEX è impostato.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Analizzare solo la parte anteriore. Questo valore è valido quando duplex è impostato.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Eseguire la scansione solo sul retro. Questo valore è valido quando duplex è impostato.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Analizzare la pagina successiva del documento.</td>
</tr>
<tr class="even">
<td>PREFEED</td>
<td>Abilitare la modalità pre-feed. Pre-posizionare il documento successivo durante l'analisi.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td ><p>Contiene lo stato corrente del letto flat, dell'alimentatore di documenti o del duplex dello scanner installato. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare se il dispositivo scanner è pronto per l'uso. Questo è un modo ideale per verificare se la carta si trova nell'alimentatore prima di acquisire un'immagine.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le costanti valide per questa proprietà. Un asterisco * indica che il flag non è supportato in Windows Vista o versioni successive. Il <strong>simbolo V</strong> indica che il flag è supportato solo in Windows Vista e versioni successive. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>Il letto flat è pronto per l'uso.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>Lo scanner dispone di un documento sulla placca a piatte.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>Il duplexer è abilitato e pronto per l'uso.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>La copertura del letto piano è in su.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>Il percorso cartaceo è coperto e impedisce il corretto funzionamento.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Un documento viene bloccato nell'alimentatore di documenti.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>L'adattatore per la trasparenza è installato e pronto per l'uso.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>Il dispositivo di archiviazione interno è pronto.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>L'archiviazione è piena, non è possibile eseguire operazioni di caricamento.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Si è verificata una condizione di più feed (in genere con un PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Si è verificato un errore che richiede l'intervento dell'utente nel dispositivo.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>Lo scanner non è pronto a causa di un problema di lampadina.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td ><p>Contiene tutti i caratteri validi che un'applicazione può usare per creare stringhe di verifica valide. Un endorser è una stampante installata in uno scanner che stampa un SMS in ogni pagina analizzata. Il minidriver deve convalidare l'impostazione <strong>della proprietà WIA_DPS_ENDORSER_STRING</strong> rispetto al set di caratteri valido in questa proprietà. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td ><p>Contiene una stringa da approvare (in altre parole, stampata) in ogni pagina analizzata dal minidriver. Un'applicazione imposta questa proprietà usando il set di caratteri valido segnalato nella WIA_DPS_ENDORSER_CHARACTERS <strong>proprietà</strong> . Il minidriver deve approvare i documenti solo se in questa proprietà è impostata una stringa. Una stringa vuota indica che la funzionalità endorser è disabilitata.</p>
<p>Poiché è responsabilità del driver interpretare la stringa dell'endorser, il driver può usare caratteri speciali <strong>in</strong>WIA_DPS_ENDORSER_STRING . Tuttavia, solo le applicazioni possono comprendere questi caratteri.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Un driver che supporta la <strong>proprietà WIA_DPS_ENDORSER_STRING</strong> deve supportare l'elenco di token seguente. </p>
<table>
<thead>
<tr class="header">
<th>token</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE$</td>
<td>Data nel formato AAAA/MM/GG.</td>
</tr>
<tr class="even">
<td>$DAY$</td>
<td>Giorno nel formato DD.</td>
</tr>
<tr class="odd">
<td>$MONTH$</td>
<td>Mese dell'anno nel formato MM.</td>
</tr>
<tr class="even">
<td>$PAGE_COUNT$</td>
<td>Numero di pagine trasferite.</td>
</tr>
<tr class="odd">
<td>$TIME$</td>
<td>Ora del giorno nel formato HH:MM:SS.</td>
</tr>
<tr class="even">
<td>$YEAR$</td>
<td>Anno nel formato AAAA.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td ><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo in Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'indirizzo SOAP di un dispositivo scanner di servizi Web. Il mini driver WIA 2.0 crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la registrazione, o allineamento orizzontale, per i documenti posizionati sul letto flat. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide con questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Il documento viene giustificato a sinistra.</td>
</tr>
<tr class="even">
<td>CENTRATO</td>
<td>La carta è centrata.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Il documento è giustificato.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vedere anche</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica la larghezza massima, in millesimo di pollice, analizzata nell'asse orizzontale (X) dalla placca di uno scanner a piano piano alla risoluzione corrente. Questa proprietà si applica anche agli alimentatori di documenti automatici che spostano i fogli nella placca di uno scanner a piano per la scansione. Questa proprietà è obbligatoria per gli scanner con una piastine. Altri tipi di scanner implementeranno invece la <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> predefinita.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica la larghezza massima, in millesimo di pollice, analizzata nell'asse orizzontale (X) da un dispositivo portatile o da uno scanner di alimentazione di fogli alla risoluzione corrente. Questa proprietà si applica anche agli alimentatori di documenti automatici che esegueno l'analisi senza spostare i fogli nella placca di uno scanner a letti flat. Questa proprietà è obbligatoria per gli scanner con alimentazione a fogli, con scorrimento e mano.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td ><p>Contiene il tempo massimo di analisi di una singola pagina con le impostazioni correnti delle proprietà, in millisecondi. Un'applicazione legge questa proprietà per stimare il tempo necessario per analizzare una pagina. Ciò è utile quando si determinano le condizioni di un dispositivo che ha smesso di rispondere. Il minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene le dimensioni orizzontali fisiche della pagina più piccola che l'alimentatore di documenti dello scanner può analizzare, in migliaia di pollici. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vedere anche</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene le dimensioni verticali fisiche della pagina più piccola che l'alimentatore di documenti dello scanner può analizzare, in migliaia di pollici. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vedere anche</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Risoluzione ottica orizzontale. Risoluzione ottica orizzontale più elevata supportata in DPI. Questa proprietà è un singolo valore. Non si tratta di un elenco di tutte le risoluzioni che possono essere generate dal dispositivo. Si tratta invece della risoluzione dell'ottica del dispositivo. Il minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Risoluzione ottica verticale. Risoluzione ottica verticale più elevata supportata in DPI. Questa proprietà è un singolo valore. Non si tratta di un elenco di tutte le risoluzioni generate dal dispositivo. Si tratta invece della risoluzione dell'ottica del dispositivo. Il minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td ><p>Contiene l'impostazione di orientamento corrente. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione imposta <strong>WIA_DPS_ORIENTATION</strong> proprietà per definire l'orientamento originale di una pagina o di un'immagine da acquisire. Per informazioni su come usare WIA_DPS_ORIENTATION, vedere <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le quattro costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Defination</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PAESAGGIO</td>
<td>Rotazione in senso antiorario di 90 gradi rispetto all'orientamento PORTRAIT.</td>
</tr>
<tr class="even">
<td>RITRATTO</td>
<td>0 gradi.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Rotazione in senso antiorario di 180 gradi rispetto all'orientamento PORTRAIT.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Rotazione in senso antiorario di 270 gradi rispetto all'orientamento PORTRAIT.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vedere anche</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td ><p>Colore usato per il riempimento quando i dati dell'immagine non sono sufficienti per riempire un buffer richiesto. Questa proprietà viene implementata per gli scanner che esere esere il buffer. Questa proprietà è facoltativa per tutti gli scanner. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Il formato delle informazioni sul colore è <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD.</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'altezza, in migliaia di pollici, della pagina attualmente selezionata. Il minidriver crea e gestisce la <strong>WIA_DPS_PAGE_HEIGHT</strong> proprietà . Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina analizzata. Se le impostazioni dell'extent sono diverse dalle dimensioni di pagina note, questa proprietà segnala l'altezza della pagina la cui proprietà <strong>WIA_DPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM (che è un valore della proprietà <strong>WIA_DPS_PAGE_SIZE).</strong> <strong>WIA_DPS_PAGE_HEIGHT</strong> deve essere sincronizzato con <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, che indica l'altezza, in pixel, della pagina da analizzare.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene le dimensioni della pagina attualmente selezionata per l'analisi. Per selezionare le dimensioni della pagina da analizzare, un'applicazione imposta questa proprietà. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide con questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 X 11692 (orientamento VERTICALE)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definito dai valori delle <strong>proprietà</strong> WIA_DPS_PAGE_HEIGHT e <strong>WIA_DPS_PAGE_WIDTH</strong> proprietà</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientamento VERTICALE)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Il valore della proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina l'orientamento della pagina attualmente selezionata. Le <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> proprietà segnalano le dimensioni della pagina, in migliaia di pollice. Si noti che queste proprietà devono essere in accordo <strong>con WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, che contengono le dimensioni della pagina in pixel. I valori validi di WIA_PROP_LIST devono dipendere dalle impostazioni valide della <strong>WIA_IPS_ORIENTATION</strong> proprietà . Se il dispositivo non è in grado di analizzare documenti orientati all'orientamento orizzontale con un'impostazione WIA_PAGE_A4, WIA_PAGE_A4 non dovrebbe essere visualizzato nell'elenco di valori validi per la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> è impostato su LANSCAPE.</p>
<p>Se un'applicazione imposta <strong>WIA_DPS_PAGE_SIZE</strong> su un valore diverso da WIA_PAGE_CUSTOM, il minidriver deve modificare i valori di <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> in base alle dimensioni della pagina in milleli di pollice. Deve anche regolare i valori di <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> e <strong>WIA_IPS_YEXTENT</strong> alle dimensioni della pagina in pixel.</p>
<p>Se un'impostazione dell'extent (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> o <strong>WIA_IPS_YEXTENT</strong>) viene modificata in un valore che non corrisponde all'impostazione corrente delle dimensioni della pagina, il minidriver deve modificare il valore della proprietà <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM. Il minidriver deve anche <strong>modificare</strong> WIA_DPS_PAGE_WIDTH o <strong>WIA_DPS_PAGE_HEIGHT</strong> in base alla nuova impostazione extent.</p>
<p>Se <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> è impostato su LANSCAPE, le impostazioni degli extent verranno &quot; capovolte. &quot; Ad esempio, se un'applicazione imposta <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_A4, il minidriver deve impostare <strong>WIA_DPS_PAGE_WIDTH</strong> su 11692 e WIA_DPS_PAGE_HEIGHT <strong>su</strong> 8267. Il minidriver deve anche <strong>impostare</strong> WIA_IPS_XEXTENT e <strong>WIA_IPS_YEXTENT</strong> di conseguenza. Si noti che <strong>se WIA_DPS_PAGE_SIZE</strong> è impostato su WIA_PAGE_CUSTOM, l'impostazione dell'orientamento non viene usata per determinare le dimensioni dell'extent della pagina da analizzare.</p>
<p>Il minidriver è responsabile di garantire che la <a href="-wia-wiaitempropscanneritem.md"><strong>proprietà WIA_IPS_ORIENTATION</strong></a> sia in accordo con l'area di selezione corrente. Se un'applicazione modifica il valore di <strong>WIA_IPS_ORIENTATION</strong> in un valore non valido per le dimensioni di pagina attualmente selezionate, il minidriver deve modificare il valore di <strong>WIA_DPS_PAGE_SIZE</strong> impostando una dimensione di pagina supportata dal nuovo valore di orientamento.</p>
<p>Se un'applicazione imposta <strong>la WIA_DPS_PAGE_SIZE</strong> proprietà su WIA_PAGE_CUSTOM, l'area di selezione corrente non è interessata. Il minidriver WIA deve ottenere il layout dell'immagine corrente, a partire dalle impostazioni correnti WIA_IPS_XPOS <a href="-wia-wiaitempropscanneritem.md"><strong>e</strong></a> <strong>WIA_IPS_YPOS</strong> proprietà. Se l'impostazione delle dimensioni della pagina determina un'area di selezione esterna al letto dello scanner, il minidriver deve modificare automaticamente i valori delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> impostandole su impostazioni valide. Se le <strong>proprietà WIA_DPS_PAGE_SIZE</strong> <strong>e WIA_IPS_ORIENTATION</strong> sono impostate contemporaneamente e non sono valide quando vengono applicate in combinazione, il minidriver dovrebbe non riuscire le impostazioni dell'applicazione restituisce un errore in <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvValidateItemProperties.</a> .</p>
<p>I quattro esempi seguenti illustrano scenari <strong>WIA_DPS_PAGE_SIZE</strong> diversi.</p>
<ol>
<li>Il driver segnala le impostazioni.</li>
<li>Un'applicazione imposta <strong>la WIA_DPS_PAGE_SIZE</strong> proprietà su WIA_PAGE_LETTER.</li>
<li>Un'applicazione imposta la <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> proprietà su LANSCAPE.</li>
<li>Un'applicazione modifica <a href="-wia-wiaitempropscanneritem.md"><strong>la WIA_IPS_XEXTENT</strong></a> proprietà in un valore più piccolo.</li>
</ol>
<p><strong>Esempio 1: il minidriver segnala le impostazioni</strong></p>
<p>Nell'esempio seguente il minidriver imposta un'area di selezione personalizzata prima che un'applicazione imposta le proprietà WIA. In questo caso, l'area di selezione rappresenta l'intera struttura bi flat.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Esempio 2: un'applicazione imposta la</strong> <strong>WIA_DPS_PAGE_SIZE</strong>proprietà<strong>su WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Esempio 3: Un'applicazione imposta la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>proprietà WIA_IPS_ORIENTATION</strong></a>su<strong>LANSCAPE</strong>  </p>
<p>Il letto fisico deve essere in grado di acquisire una pagina originariamente con orientamento orizzontale.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<p><strong>Esempio 4: un'applicazione modifica la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>proprietà WIA_IPS_XEXTENT</strong></a>a un valore più<strong>piccolo</strong>  </p>
<p>Nell'esempio seguente, in un'applicazione la <a href="-wia-wiaitempropscanneritem.md"><strong>proprietà WIA_IPS_XEXTENT</strong></a> viene impostata su 1000. Il minidriver deve presupporre che il nuovo valore contenuto in <strong>WIA_IPS_XEXTENT</strong> non <strong></strong> sia più valido per la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> e quindi modificare WIA_DPS_PAGE_SIZE in WIA_PAGE_CUSTOM. Il minidriver deve anche modificare <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<td ><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la larghezza della pagina corrente selezionata, in migliaia di pollice. Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina analizzata. Se le impostazioni dell'extent sono diverse dalle dimensioni di pagina note, questa proprietà restituisce la larghezza della pagina la cui WIA_DPS_PAGE_SIZE <strong>è</strong> impostata su WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> deve essere sincronizzato con il valore di <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, che indica la larghezza, in pixel, della pagina da analizzare. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene il numero corrente di pagine da acquisire da un feed di documenti automatico. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso: Lettura/Scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (da zero al numero massimo di pagine che l'alimentatore di documenti può contenere)</p>
<p>Un'applicazione legge questa proprietà per determinare la capacità di pagina dell'alimentatore di documenti. L'applicazione imposta anche questa proprietà sul numero di pagine da analizzare.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se la modalità duplex è abilitata (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> è impostato su FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> è ancora uguale al numero di pagine da analizzare.
</blockquote>
</div>
<div>
 
</div>
<p>Un foglio di carta conterrà automaticamente due pagine se DUPLEX è abilitato, anche se il lato posteriore della pagina è vuoto.</p>
<p>Impostando <strong>WIA_DPS_PAGES</strong> su 1, uno scanner elabora uno dei lati della pagina. È consigliabile che se uno scanner non è in grado di analizzare solo un lato di una pagina in modalità <strong>duplex,</strong> il valore valido di WIA_DPS_PAGES per il membro Inc della struttura WIA_PROPERTY_INFO deve essere modificato in 2. Questo valore segnala all'applicazione che deve richiedere pagine in multipli di due. Il valore zero indica che <em>tutte le</em> pagine attualmente caricate nell'alimentatore di documenti devono essere analizzate.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td ><p>Specifica il colore della pistoiera nella parte posteriore del foglio da analizzare. Questa proprietà è facoltativa per gli scanner con una pistocca. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Il formato delle informazioni sul colore è <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD.</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica la modalità di anteprima per un dispositivo. Un'applicazione imposta questa proprietà per impostare il dispositivo in modalità di anteprima.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le due costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>L'applicazione eseguirà un'analisi finale.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>L'applicazione eseguirà un'analisi in anteprima.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td ><p>Contiene un valore che indica se lo scanner memorizza nella cache le pagine in un buffer dello scanner prima di inviarle all'applicazione.</p>
<p>Il valore zero disabilita l'analisi in avanti e nessuna pagina verrà analizzata in anticipo. Eseguendo normali trasferimenti di dati sull'elemento con analisi anticipata memorizzata nel buffer, vengono recuperate le pagine memorizzate nel buffer. Le proprietà WIA non possono essere modificate durante un'operazione di analisi. Questa proprietà è facoltativa.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows 7 e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Indica l'origine di input (flatbed, feeder automatico di documenti o adattatore di analisi fil) da cui eseguire l'analisi o la posizione di archiviazione da cui trasferire i dati.</p>
<p>Un evento di analisi notifica all'applicazione che l'utente ha avviato un'analisi, ma l'evento non fornisce il nome dell'elemento WIA che rappresenta l'origine di input. Il gestore eventi dell'applicazione può eseguire una query sulla proprietà WIA_DPS_SCAN_AVAILABLE_ITEM dell'elemento radice per ottenere il nome dell'elemento di origine di input.</p>
<p>Tipo: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'ID servizio di un dispositivo scanner di servizi Web. Il mini driver WIA 2.0 crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la registrazione, o il rilevamento dell'allineamento e dei bordi, per i documenti posizionati sul piano bi flat. Il minidriver crea e gestisce questa proprietà. Questa proprietà indica il modo in cui il foglio viene posizionato orizzontalmente sulla testa di scansione di un ricevitore o di uno scanner a fogli. La proprietà viene usata per stimare la posizione di un documento nell'elemento head di digitalizzazione.</p>
<p>Per gli scanner che supportano più di una testina di analisi, questa proprietà è relativa alla testa di analisi in primo piano. Questa proprietà è obbligatoria per gli scanner a foglio, a scorrimento e a mano.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Il foglio è posizionato a sinistra rispetto alla testa di scansione.</td>
</tr>
<tr class="even">
<td>CENTRATO</td>
<td>Il foglio è centrato sulla testa di scansione.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Il foglio è posizionato a destra rispetto alla testa di scansione.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica se un elemento richiede un controllo di anteprima visualizzato all'utente. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le due costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Mostra un controllo di anteprima all'utente, perché questo dispositivo può eseguire un'anteprima.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Non mostrare un controllo di anteprima all'utente, perché questo dispositivo non può eseguire un'anteprima.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Usato dal servizio WIA per informare il mini driver sul nome dell'account utente (incluso il nome di dominio di rete, se applicabile) della sessione in cui è in esecuzione l'applicazione WIA corrente.</p>
<p>Si tratta di una proprietà dell'elemento radice, gestita dal servizio WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la registrazione, o l'allineamento verticale e il rilevamento dei bordi, per i documenti posizionati sul piano flat. Il minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide con questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>Il documento è giustificato in alto.</td>
</tr>
<tr class="even">
<td>CENTRATO</td>
<td>La carta è centrata.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>Il documento è giustificato in basso.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vedere anche</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica l'altezza massima, in migliaia di pollice, che viene analizzata sull'asse verticale (Y) dalla piana di uno scanner bi flat alla risoluzione corrente. Questa proprietà si applica anche agli alimentatori automatici di documenti, che spostano i fogli nella piana di uno scanner bi flat per l'analisi. Questa proprietà è obbligatoria per gli scanner con un pistoid. Altri tipi di scanner implementeranno invece <strong>la WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> proprietà .</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata con Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica l'altezza massima, in migliaia di pollice, che viene analizzata sull'asse verticale (Y) da un ricevitore o da uno scanner di alimentazione a fogli alla risoluzione corrente. Questa proprietà si applica anche agli alimentatori di documenti automatici che estraeno i fogli senza spostare i fogli nella piana di uno scanner a piatte. Questa proprietà è obbligatoria per gli scanner con alimentazione a fogli. Gli scanner con scorrimento e mano non devono implementare questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
