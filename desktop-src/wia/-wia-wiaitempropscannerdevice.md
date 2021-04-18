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
# <a name="scanner-device-property-constants"></a>Costanti della proprietà del dispositivo dello scanner

I dispositivi hardware Windows Image Acquisition (WIA) dispongono di valori di proprietà archiviati nel registro di sistema di Windows. Per altre informazioni, vedere [**costanti della proprietà del dispositivo comune**](-wia-wiaitempropcommondevice.md). Le seguenti costanti della proprietà del dispositivo, con le relative stringhe associate, sono specifiche per gli scanner di immagini digitali.

Il prefisso "WIA \_ DPS \_ " indica una proprietà del dispositivo per i dispositivi dello scanner e rappresenta la convenzione di denominazione usata in C/C++. Per finalità di scripting queste costanti usano il prefisso "ScannerDevice" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



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
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Questa proprietà è supportata solo in Windows Vista e versioni successive.
</blockquote>
<br/> Contiene un identificatore di istanza di funzione univoco per un dispositivo scanner di servizi Web. Questo identificatore rappresenta il servizio Web sul dispositivo dello scanner con cui comunica il mini driver WIA. Non è necessario che venga creato alcun presupposto sul formato di questo identificatore. Il mini driver WIA crea e gestisce questa proprietà. <br/> Le applicazioni WIA possono usare il valore di WIA_DPS_DEVICE_ID per trovare, usando l'API di individuazione delle funzioni, l'oggetto istanza della funzione che rappresenta il dispositivo di scanner dei servizi Web usato nella sessione WIA 2,0 corrente.<br/> Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td style="text-align: left;">Riservato, non usare.<br/> Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;">Riservato, non usare.<br/> Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td style="text-align: left;">Contiene le funzionalità dello scanner. Minidriver crea e gestisce questa proprietà. <br/> Un'applicazione legge questa proprietà per determinare se lo scanner ha un piano, un alimentatore di documenti o un duplex installato. Questa proprietà viene inoltre utilizzata per definire ulteriormente le funzionalità installate.<br/> Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Nella tabella seguente vengono descritte le costanti valide solo per Windows 7.<br/> 
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
<p>Nella tabella seguente vengono descritte le costanti valide solo per Windows 7 e Windows Vista.</p>
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
<td>Il dispositivo supporta la configurazione avanzata di analisi duplex. Usare WIA_IPS_DUPLEX_SETTINGS per passare dall'uso di configurazioni duplex di base e avanzate.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>Lo scanner è in grado di rilevare quando la scheda trasparenza/film è pronta per l'analisi.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>Lo scanner è in grado di rilevare quando sono presenti documenti nella risorsa di archiviazione interna.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>Lo scanner è dotato di una scheda di analisi trasparente/film.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>Lo scanner è dotato di un dispositivo di archiviazione immagini interno.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Nella tabella seguente vengono descritte le costanti valide per Windows XP o versioni successive.</p>
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
<td>Lo scanner è in grado di rilevare un documento nel feeder.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>Lo scanner è in grado di rilevare un documento sulla piastra piana.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>Lo scanner è in grado di rilevare un documento nel Feeder solo analizzando.</td>
</tr>
<tr class="even">
<td>DUP</td>
<td>Lo scanner ha un duplex.</td>
</tr>
<tr class="odd">
<td>FEED</td>
<td>Per lo scanner è installato un gestore di documenti automatico.</td>
</tr>
<tr class="even">
<td>PIATTO</td>
<td>Lo scanner ha una piastra piana.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Nella tabella seguente vengono descritte le costanti valide solo per Windows XP. Questi valori sono stati deprecati per Windows 7 e Windows Vista e non devono essere usati.</p>
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
<td>Lo scanner è in grado di rilevare una richiesta di analisi duplex da parte dell'utente.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>Lo scanner è in grado di stabilire quando è installato il duplex.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>Lo scanner è in grado di stabilire quando viene installato il feeder automatico del documento.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'origine e la modalità di acquisizione dello scanner corrente. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare l'origine di acquisizione corrente dello scanner o per scrivere questa proprietà per impostare l'origine e la modalità dello scanner. Inoltre, le applicazioni usano questa proprietà per abilitare e disabilitare la funzionalità di duplex.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>La tabella seguente contiene le dieci costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEEDER</td>
<td>Eseguire l'analisi usando il feeder del documento.</td>
</tr>
<tr class="even">
<td>PIANALE</td>
<td>Eseguire l'analisi usando il piano.</td>
</tr>
<tr class="odd">
<td>DUPLEX</td>
<td>Eseguire l'analisi usando le operazioni di duplex.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Consente l'inserimento automatico del documento successivo dopo un'analisi.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Eseguire prima l'analisi della parte anteriore del documento. Questo valore è valido quando si imposta DUPLEX.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Eseguire prima la scansione della parte posteriore del documento. Questo valore è valido quando si imposta DUPLEX.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Esegue l'analisi solo dell'oggetto front. Questo valore è valido quando si imposta DUPLEX.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Eseguire la scansione solo della parte posteriore. Questo valore è valido quando si imposta DUPLEX.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Esegue l'analisi della pagina successiva del documento.</td>
</tr>
<tr class="even">
<td>Prefeed</td>
<td>Abilitare la modalità pre-feed. Pre-posizionare il documento successivo durante l'analisi.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td style="text-align: left;"><p>Contiene lo stato corrente del piano, del feeder di documenti o del duplex installato dello scanner. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare se il dispositivo scanner è pronto per essere utilizzato. Si tratta di un modo ideale per verificare se la carta si trova nel feeder prima di acquisire un'immagine.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. Un asterisco * indica che il flag non è supportato in Windows Vista o versioni successive. Il simbolo <strong>V</strong> indica che il flag è supportato solo in Windows Vista e versioni successive. </p>
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
<td>Il piano è pronto per l'uso.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>Lo scanner ha un documento sulla piastra piana.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>Il duplex è abilitato e pronto per l'uso.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>La copertura del letto flat è attiva.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>Il percorso carta è coperto e impedisce il corretto funzionamento.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Un documento è bloccato nel Feeder del documento.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>La scheda trasparenza è installata e pronta per l'utilizzo.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>Il dispositivo di archiviazione interno è pronto.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>Lo spazio di archiviazione è pieno e non è possibile caricare operazioni.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Si è verificata una condizione di feed multiplo (in genere con un PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Si è verificato un errore che richiede l'intervento dell'utente sul dispositivo.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>Lo scanner non è pronto a causa di un problema lamp.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td style="text-align: left;"><p>Contiene tutti i caratteri validi che un'applicazione può usare per creare stringhe di approvazione valide. Un approvatore è una stampante installata in uno scanner che stampa un SMS in ogni pagina analizzata. Minidriver deve convalidare l'impostazione della proprietà <strong>WIA_DPS_ENDORSER_STRING</strong> in base al set di caratteri valido in questa proprietà. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td style="text-align: left;"><p>Contiene una stringa che deve essere approvata (in altre parole, stampata) in ogni pagina analizzata da minidriver. Un'applicazione imposta questa proprietà utilizzando il set di caratteri valido indicato nella proprietà <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> . Il minidriver deve avallare i documenti solo se in questa proprietà è impostata una stringa. Una stringa vuota indica che la funzionalità dell'approvatore è disabilitata.</p>
<p>Poiché è responsabilità del driver interpretare la stringa dell'approvatore, il driver può utilizzare caratteri speciali in <strong>WIA_DPS_ENDORSER_STRING</strong>. Tuttavia, solo le applicazioni capirebbero questi caratteri.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Un driver che supporta la proprietà <strong>WIA_DPS_ENDORSER_STRING</strong> deve supportare il seguente elenco di token. </p>
<table>
<thead>
<tr class="header">
<th>token</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE $</td>
<td>Data nel formato AAAA/MM/GG.</td>
</tr>
<tr class="even">
<td>$DAY $</td>
<td>Il giorno nel formato gg.</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>Mese dell'anno nel formato MM.</td>
</tr>
<tr class="even">
<td>$PAGE _COUNT $</td>
<td>Numero di pagine trasferite.</td>
</tr>
<tr class="odd">
<td>$TIME $</td>
<td>Ora del giorno nel formato HH: MM: SS.</td>
</tr>
<tr class="even">
<td>$YEAR $</td>
<td>Anno nel formato aaaa.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;"><p>Riservato, non usare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo in Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'indirizzo SOAP di un dispositivo scanner di servizi Web. Il mini driver WIA 2,0 crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la registrazione, o allineamento orizzontale, per i documenti posizionati sulla superficie piana. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>Il documento viene lasciato giustificato.</td>
</tr>
<tr class="even">
<td>CENTRATO</td>
<td>Il documento è centrato.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Il documento è giustificato a destra.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vedere anche</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica la larghezza massima, in millesimi di pollice, sottoposta a scansione nell'asse orizzontale (X) dalla piastra di uno scanner piano alla risoluzione corrente. Questa proprietà si applica anche ai feeder di documenti automatici che spostano i fogli sulla piastra di uno scanner per la scansione. Questa proprietà è obbligatoria per gli scanner con un piatto. Per gli altri tipi di scanner viene invece implementata la proprietà <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica la larghezza massima, in millesimi di pollice, che viene analizzata nell'asse orizzontale (X) da uno scanner di feed di fogli o palmari alla risoluzione corrente. Questa proprietà si applica anche ai feeder di documenti automatici che eseguono l'analisi senza trasferire i fogli alla piastra di uno scanner. Questa proprietà è obbligatoria per gli scanner a foglio, a scorrimento e con alimentazione manuale.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il tempo massimo per l'analisi di una singola pagina con le impostazioni delle proprietà correnti, in millisecondi. Questa proprietà viene letta da un'applicazione per stimare il tempo necessario per l'analisi di una pagina. Questa operazione è utile quando si determinano le condizioni di un dispositivo che ha smesso di rispondere. Minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene le dimensioni orizzontali fisiche della pagina più piccola che il feeder di documenti dello scanner è in grado di analizzare, in millesimi di pollice. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vedere anche</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene le dimensioni verticali fisiche della pagina più piccola che il feeder di documenti dello scanner è in grado di analizzare, in millesimi di pollice. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Vedere anche</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Risoluzione ottica orizzontale. Risoluzione ottica orizzontale più elevata supportata in DPI. Questa proprietà è un singolo valore. Non si tratta di un elenco di tutte le risoluzioni che possono essere generate dal dispositivo. Piuttosto, si tratta della risoluzione dell'ottica del dispositivo. Minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Risoluzione ottica verticale. Risoluzione ottica verticale massima supportata in DPI. Questa proprietà è un singolo valore. Non si tratta di un elenco di tutte le risoluzioni generate dal dispositivo. Piuttosto, si tratta della risoluzione dell'ottica del dispositivo. Minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'impostazione di orientamento corrente. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione imposta la proprietà <strong>WIA_DPS_ORIENTATION</strong> per definire l'orientamento originale di una pagina o di un'immagine da acquisire. Per informazioni sull'utilizzo di WIA_DPS_ORIENTATION, vedere <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabella seguente include le quattro costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Defination</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ORIZZONTALE</td>
<td>rotazione in senso antiorario di 90 gradi, relativa all'orientamento verticale.</td>
</tr>
<tr class="even">
<td>VERTICALE</td>
<td>0 gradi.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>rotazione in senso antiorario di 180 gradi, relativa all'orientamento verticale.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>rotazione in senso antiorario di 270 gradi, relativa all'orientamento verticale.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Vedere anche</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td style="text-align: left;"><p>Colore utilizzato per il riempimento quando non sono disponibili dati di immagine sufficienti per riempire un buffer richiesto. Questa proprietà viene implementata per gli scanner che riempiono il buffer. Questa proprietà è facoltativa per tutti gli scanner. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Il formato delle informazioni sul colore è <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'altezza, in millesimi di pollice, della pagina attualmente selezionata. Minidriver crea e gestisce la proprietà <strong>WIA_DPS_PAGE_HEIGHT</strong> . Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione. Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica l'altezza della pagina la cui proprietà <strong>WIA_DPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM (valore della proprietà <strong>WIA_DPS_PAGE_SIZE</strong> ). <strong>WIA_DPS_PAGE_HEIGHT</strong> deve essere sincronizzato con <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, che indica l'altezza, in pixel, della pagina da analizzare.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la dimensione della pagina attualmente selezionata per essere analizzata. Per selezionare le dimensioni della pagina da analizzare, questa proprietà viene impostata da un'applicazione. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide per questa proprietà. </p>
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
<td>8267 X 11692 (orientamento verticale)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definito dai valori delle proprietà <strong>WIA_DPS_PAGE_HEIGHT</strong> e <strong>WIA_DPS_PAGE_WIDTH</strong></td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientamento verticale)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Il valore della proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> determina l'orientamento della pagina attualmente selezionata. Le proprietà <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> segnalano le dimensioni della pagina, in millesimi di pollice. Si noti che queste proprietà devono essere concordate con <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, che contengono le dimensioni della pagina in pixel. I valori validi di tipo WIA_PROP_LIST devono dipendere da impostazioni valide della proprietà <strong>WIA_IPS_ORIENTATION</strong> . Se il dispositivo non è in grado di analizzare documenti orientati al paesaggio con un'impostazione WIA_PAGE_A4, WIA_PAGE_A4 non deve essere visualizzato nell'elenco di valori validi per la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> è impostato su paesaggio.</p>
<p>Se un'applicazione imposta <strong>WIA_DPS_PAGE_SIZE</strong> su un valore diverso da WIA_PAGE_CUSTOM, minidriver deve modificare i valori di <strong>WIA_DPS_PAGE_WIDTH</strong> e <strong>WIA_DPS_PAGE_HEIGHT</strong> alle dimensioni della pagina in millesimi di pollice. Deve anche modificare i valori delle <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> e <strong>WIA_IPS_YEXTENT</strong> alle dimensioni della pagina in pixel.</p>
<p>Se un'impostazione di extent (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> o <strong>WIA_IPS_YEXTENT</strong>) viene modificata in un valore che non corrisponde all'impostazione della dimensione della pagina corrente, minidriver deve modificare il valore della proprietà <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM. Il minidriver deve anche modificare <strong>WIA_DPS_PAGE_WIDTH</strong> o <strong>WIA_DPS_PAGE_HEIGHT</strong> in base alla nuova impostazione dell'extent.</p>
<p>Se <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> è impostato su paesaggio, le impostazioni dell'extent verranno &quot; invertite. &quot; Se, ad esempio, un'applicazione imposta <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_A4, minidriver deve impostare <strong>WIA_DPS_PAGE_WIDTH</strong> su 11692 e <strong>WIA_DPS_PAGE_HEIGHT</strong> su 8267. Il minidriver deve inoltre impostare <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> di conseguenza. Si noti che se <strong>WIA_DPS_PAGE_SIZE</strong> è impostato su WIA_PAGE_CUSTOM, l'impostazione dell'orientamento non viene utilizzata per determinare le dimensioni dell'extent della pagina da analizzare.</p>
<p>Il minidriver è responsabile di garantire che la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> sia concordata con l'area di selezione corrente. Se un'applicazione modifica il valore di <strong>WIA_IPS_ORIENTATION</strong> a uno non valido per le dimensioni di pagina attualmente selezionate, minidriver deve modificare il valore di <strong>WIA_DPS_PAGE_SIZE</strong> in base a una dimensione di pagina supportata dal nuovo valore di orientamento.</p>
<p>Se un'applicazione imposta la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_CUSTOM, l'area di selezione corrente non è interessata. Il minidriver WIA dovrebbe ottenere il layout dell'immagine corrente, a partire dalle impostazioni correnti delle proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> e <strong>WIA_IPS_YPOS</strong> . Se l'impostazione delle dimensioni di pagina produce un'area di selezione esterna al letto dello scanner, il minidriver deve modificare automaticamente i valori delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> in impostazioni valide. Se le proprietà <strong>WIA_DPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> sono impostate contemporaneamente e non sono valide se applicate in combinazione, il minidriver deve avere esito negativo sulle impostazioni dell'applicazione restituendo un errore in <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>. .</p>
<p>Nei quattro esempi seguenti vengono illustrati scenari di <strong>WIA_DPS_PAGE_SIZE</strong> diversi.</p>
<ol>
<li>Il driver segnala le impostazioni.</li>
<li>Un'applicazione imposta la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> su WIA_PAGE_LETTER.</li>
<li>Un'applicazione imposta la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> su paesaggio.</li>
<li>Un'applicazione modifica la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> in un valore più piccolo.</li>
</ol>
<p><strong>Esempio 1: minidriver segnala le impostazioni</strong></p>
<p>Nell'esempio seguente minidriver imposta un'area di selezione personalizzata prima che un'applicazione imposti le proprietà WIA. In questo caso, l'area di selezione rappresenta l'intero piano.</p>
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
<p><strong>Esempio 2: un'applicazione imposta la</strong> <strong></strong><strong>Proprietà WIA_DPS_PAGE_SIZE su WIA_PAGE_LETTER</strong>  </p>
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
<p><strong>Esempio 3: un'applicazione imposta la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Proprietà WIA_IPS_ORIENTATION su paesaggio</strong>  </p>
<p>Il letto fisico deve essere in grado di acquisire una pagina originariamente con orientamento orizzontale.</p>
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
<p><strong>Esempio 4: un'applicazione modifica la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>Proprietà WIA_IPS_XEXTENT in un valore più piccolo</strong>  </p>
<p>Nell'esempio seguente un'applicazione modifica la proprietà <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> in 1000. Il minidriver deve presupporre che il nuovo valore contenuto in <strong>WIA_IPS_XEXTENT</strong> non sia più valido per la proprietà <strong>WIA_DPS_PAGE_SIZE</strong> e pertanto debba modificare <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM. Il minidriver deve anche modificare <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la larghezza della pagina corrente selezionata, in millesimi di pollice. Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione. Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica la larghezza della pagina la cui proprietà <strong>WIA_DPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> deve essere sincronizzato con il valore di <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, che indica la larghezza, in pixel, della pagina da analizzare. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene il numero corrente di pagine da acquisire da un feeder di documenti automatico. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero per il numero massimo di pagine che possono essere mantenute dal feeder del documento)</p>
<p>Un'applicazione legge questa proprietà per determinare la capacità della pagina del feeder del documento. L'applicazione imposta anche questa proprietà sul numero di pagine che verranno analizzate.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se è abilitata la modalità duplex (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> è impostata su Feeder | DUPLEX), <strong>WIA_DPS_PAGES</strong> è ancora uguale al numero di pagine da analizzare.
</blockquote>
</div>
<div>
 
</div>
<p>Un foglio di carta conterrà automaticamente due pagine se DUPLEX è abilitato, anche se il lato posteriore della pagina è vuoto.</p>
<p>Impostando <strong>WIA_DPS_PAGES</strong> su 1, uno scanner elabora uno dei lati della pagina. Se uno scanner non è in grado di eseguire l'analisi di un solo lato di una pagina in modalità duplex, è consigliabile modificare il valore <strong>WIA_DPS_PAGES</strong> valido per il membro Inc della struttura WIA_PROPERTY_INFO su 2. Questo valore segnala all'applicazione che deve richiedere le pagine in multipli di due. Un valore pari a zero indica che <em>tutte le</em> pagine attualmente caricate nel Feeder del documento devono essere analizzate.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td style="text-align: left;"><p>Specifica il colore dell'oggetto platino nella parte posteriore del foglio da analizzare. Questa proprietà è facoltativa per gli scanner con un piatto. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Il formato delle informazioni sul colore è <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica la modalità di anteprima per un dispositivo. Un'applicazione imposta questa proprietà per posizionare il dispositivo in modalità di anteprima.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>L'applicazione eseguirà un'analisi di anteprima.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td style="text-align: left;"><p>Contiene un valore che indica se lo scanner memorizza nella cache le pagine in un buffer dello scanner prima di inviarle all'applicazione.</p>
<p>Un valore pari a zero disabilita l'analisi in avanti e nessuna pagina verrà analizzata in anticipo. L'operazione di trasferimento dati normale nell'elemento Scan-Ahead memorizzato nel buffer consente di recuperare le pagine memorizzate nel buffer. Non è possibile modificare le proprietà WIA durante un'operazione di analisi. Questa proprietà è facoltativa.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> di zero al numero massimo di pagine che possono essere mantenute dal feeder del documento.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows 7 e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Indica l'origine di input (piano, alimentatore automatico di documenti o adattatore di analisi fil) da cui eseguire l'analisi o il percorso di archiviazione da cui trasferire i dati.</p>
<p>Un evento Scan notifica all'applicazione che l'utente ha avviato un'analisi, ma l'evento non fornisce il nome dell'elemento WIA che rappresenta l'origine di input. Il gestore eventi dell'applicazione può eseguire una query sulla proprietà WIA_DPS_SCAN_AVAILABLE_ITEM dell'elemento radice per ottenere il nome dell'elemento di origine di input.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> di zero al numero massimo di pagine che possono essere mantenute dal feeder del documento.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'ID servizio di un dispositivo scanner di servizi Web. Il mini driver WIA 2,0 crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la registrazione, ovvero l'allineamento e il rilevamento dei bordi, per i documenti posizionati sul piano. Minidriver crea e gestisce questa proprietà. Questa proprietà indica il modo in cui il foglio è posizionato orizzontalmente sull'inizio di un'analisi di un palmare o di uno scanner a schede. La proprietà viene usata per stimare la posizione di un documento all'interno dell'analisi.</p>
<p>Per gli scanner che supportano più intestazioni di analisi, questa proprietà è relativa alla testa dell'analisi in primo piano. Questa proprietà è obbligatoria per gli scanner a foglio, a scorrimento e con alimentazione a scorrimento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>Il foglio è posizionato a sinistra rispetto alla testa di analisi.</td>
</tr>
<tr class="even">
<td>CENTRATO</td>
<td>Il foglio è centrato sulla testa di scansione.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Il foglio è posizionato a destra rispetto alla testa di analisi.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata da Windows Vista. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indica se un elemento necessita di un controllo anteprima visualizzato per l'utente. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>Mostra un controllo anteprima per l'utente, perché questo dispositivo può eseguire un'anteprima.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Non visualizzare un controllo anteprima per l'utente, perché questo dispositivo non è in grado di eseguire un'anteprima.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Utilizzato dal servizio WIA per informare il mini-driver sul nome dell'account utente (incluso il nome di dominio di rete quando applicabile) della sessione in cui è in esecuzione l'applicazione WIA corrente.</p>
<p>Si tratta di una proprietà elemento radice, gestita dal servizio WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la registrazione, ovvero l'allineamento verticale e il rilevamento dei bordi, per i documenti posizionati sul piano. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le tre costanti valide per questa proprietà. </p>
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
<td>Il documento è giustificato in primo piano.</td>
</tr>
<tr class="even">
<td>CENTRATO</td>
<td>Il documento è centrato.</td>
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
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica l'altezza massima, in millesimi di pollice, sottoposta a scansione nell'asse verticale (Y) dalla piastra di uno scanner piano alla risoluzione corrente. Questa proprietà si applica anche ai feeder di documenti automatici, che spostano i fogli sulla piastra di uno scanner piano per l'analisi. Questa proprietà è obbligatoria per gli scanner con un piatto. Per gli altri tipi di scanner viene invece implementata la proprietà <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà non è supportata in Windows Vista e versioni successive. Usare <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica l'altezza massima, in millesimi di pollice, che viene analizzata nell'asse verticale (Y) da uno scanner di feed di fogli o palmari alla risoluzione corrente. Questa proprietà si applica anche ai feeder di documenti automatici che eseguono l'analisi senza trasferire i fogli alla piastra di uno scanner. Questa proprietà è obbligatoria per gli scanner a foglio. Gli scanner a scorrimento e con alimentazione a mano non devono implementare questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
