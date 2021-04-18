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
# <a name="scanner-wia-item-property-constants"></a>Costanti della proprietà elemento WIA dello scanner

Le costanti seguenti specificano il set valido di proprietà degli elementi dello scanner WIA (Windows Image Acquisition).

Il prefisso "WIA \_ IP \_ " indica una proprietà Item per i dispositivi scanner e rappresenta la convenzione di denominazione usata in C/C++. Per finalità di scripting queste costanti usano il prefisso "ScannerPicture" e fanno parte del tipo enumerato [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Il nome del membro corrispondente da tale enumerazione dello script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



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
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
<br/> Attiva o disattiva l'inclinazione automatica.<br/> Facoltativo solo per WIA_CATEGORY_FEEDER.<br/> Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> La tabella seguente contiene le costanti valide per questa proprietà. 
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>Attivare l'inclinazione automatica.</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>Disattiva la deasimmetria automatica.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </dl></td>
<td style="text-align: left;"><p>Valori di luminosità dell'immagine disponibili nello scanner.</p>
<p>Contiene l'impostazione della luminosità hardware corrente per il dispositivo. Un'applicazione imposta questa proprietà sul valore di luminosità dell'hardware. Minidriver crea e gestisce questa proprietà.</p>
<p>I valori devono essere mappati in un intervallo compreso tra-1000 e 1000, dove 1000 corrisponde alla luminosità massima, 0 corrisponde alla luminosità normale e-1000 corrisponde alla luminosità minima.</p>
<p>Obbligatorio per tutti gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM. Facoltativo, ma consigliato, per WIA_CATEGORY_FINISHED_FILE elementi che supportano le anteprime.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'impostazione di contrasto hardware corrente per un dispositivo. Un'applicazione imposta questa proprietà sul valore di contrasto dell'hardware. Minidriver crea e gestisce questa proprietà.</p>
<p>I valori devono essere mappati in un intervallo compreso tra-1000 e 1000, dove-1000 corrisponde al contrasto minimo, 0 corrisponde al contrasto normale e 1000 corrisponde al contrasto massimo.</p>
<p>Obbligatorio per tutti gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM. Facoltativo, ma consigliato, per WIA_CATEGORY_FINISHED_FILE elementi che supportano le anteprime.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </dl></td>
<td style="text-align: left;"><p>Contiene le impostazioni relative allo scopo corrente. Minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM. Non è supportata per gli elementi WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER.</p>
<p>Tipo: accesso <strong>VT_I4</strong> : lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>Il driver li usa per impostare le proprietà dell'elemento in base all'uso previsto dell'immagine da parte dell'applicazione. Questo potrebbe includere, ad esempio, la qualità massima, le dimensioni minime e così via.</p>
<p>Il driver sceglie la profondità del bit, espressa in punti per pollice, e le altre impostazioni che determina sono appropriate per lo scopo selezionato. Spetta all'applicazione leggere le impostazioni correnti per determinare quali proprietà sono state modificate. Un'applicazione imposta questa proprietà per impostare automaticamente le proprietà WIA per finalità di acquisizione specifiche. Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>Un'applicazione imposta questa proprietà per impostare automaticamente le proprietà WIA per finalità di acquisizione specifiche</p>
<div class="alert">
<blockquote>
[!Note]<br />
I flag possono essere combinati con un <strong>operatore OR</strong> bit per bit, ma un'immagine non può essere sia di scala di grigi che di colore.
</blockquote>
</div>
<div>
 
</div>
<p>Questa proprietà è obbligatoria per tutti gli scanner.</p>
<p>La tabella seguente contiene i flag del tipo di immagine e le relative definizioni. Questi flag vengono usati per impostare il tipo di immagine desiderato: colore, scala di grigi e così via.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flag del tipo di immagine previsto</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>Valore predefinito. Non è stato specificato alcun preventivo.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>L'applicazione intende preparare il dispositivo per un'analisi dei colori.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>L'applicazione intende preparare il dispositivo per un'analisi in scala di grigi.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>L'applicazione intende preparare il dispositivo per la scansione del testo.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>Maschera per tutti i flag di tipo immagine.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La tabella seguente contiene i flag di qualità e dimensioni e le relative definizioni. Questi flag vengono usati per impostare il livello di qualità desiderato.</p>

<table>
<thead>
<tr class="header">
<th>Flag di qualità/dimensioni immagine previsti</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>L'applicazione intende preparare il dispositivo per l'analisi di un'immagine che risulta in un'analisi di piccole dimensioni.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>L'applicazione intende preparare il dispositivo per l'analisi di un'immagine di alta qualità.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>Questo flag è una maschera per tutti i flag di dimensione/qualità.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>L'applicazione intende preparare il dispositivo per l'analisi di un'anteprima.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene il numero di pixel nella direzione x da WIA_IPS_XPOS alla coordinata x dell'angolo superiore dell'immagine da dependere. Viene quindi descritto, in combinazione con WIA_IPS_DESKEW_Y, in cui i due angoli superiori dell'immagine asimmetrica si trovano all'interno del rettangolo di delimitazione definito da WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT. la proprietà viene implementata dal driver dello scanner se supporta la deasimmetria.</p>
<p>I valori validi per WIA_IPS_DESKEW_X devono essere compresi tra 0 e (WIA_IPS_XEXTENT-1). Il valore 0 indica che non deve essere eseguita alcuna disasimmetria.</p>
<p>Questa proprietà è facoltativa per gli elementi delle categorie WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e non è disponibile per WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementi.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene il numero di pixel nella direzione y da WIA_IPS_YPOS alla coordinata y dell'angolo più a sinistra dell'immagine da dependere. Viene quindi descritto, in combinazione con WIA_IPS_DESKEW_X, in cui i due angoli superiori dell'immagine asimmetrica si trovano all'interno del rettangolo di delimitazione definito da WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT e WIA_IPS_YEXTENT. Questa proprietà viene implementata dal driver dello scanner se supporta la deasimmetria.</p>
<p>I valori validi per WIA_IPS_DESKEW_Y devono essere compresi tra 0 e (WIA_IPS_YEXTENT-1). Il valore 0 indica che non deve essere eseguita alcuna disasimmetria.</p>
<p>Questa proprietà è facoltativa per gli elementi delle categorie WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM; e non è disponibile per WIA_CATEGORY_FINISHED_FILE o WIA_CATEGORY_FOLDER elementi.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'origine e la modalità di acquisizione dello scanner corrente. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare l'origine di acquisizione corrente dello scanner o per scrivere questa proprietà per impostare l'origine e la modalità dello scanner. Inoltre, le applicazioni usano questa proprietà per abilitare e disabilitare la funzionalità di duplex.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DUPLEX</td>
<td>Eseguire l'analisi usando le operazioni di duplex. Analizza entrambi i lati del documento usando le impostazioni comuni configurate per l'elemento del feeder (WIA_CATEGORY_FEEDER). Non è possibile impostare entrambi DUPLEX e ADVANCE_DUPLEX.</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>Eseguire l'analisi usando le singole impostazioni configurate per ogni elemento del feeder figlio (WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK). Non è possibile impostare entrambi DUPLEX e ADVANCE_DUPLEX.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Eseguire prima l'analisi della parte anteriore del documento. Questo valore è valido quando si imposta DUPLEX o ADVANCED_DUPLEX.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Eseguire prima la scansione della parte posteriore del documento. Questo valore è valido quando si imposta DUPLEX o ADVANCED_DUPLEX.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Esegue l'analisi solo dell'oggetto front.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Eseguire la scansione solo della parte posteriore. Questo valore è valido quando si imposta DUPLEX o ADVANCED_DUPLEX.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Abilita la specifica di un particolare allegato di analisi della pellicola quando ne sono presenti più di uno.</p>
<p>Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FILM quando sono presenti più elementi di analisi del film. Se il dispositivo supporta solo un elemento del film dello scanner radice, questa proprietà è facoltativa.</p>
<p>Tipo: <strong>VT_BSTR</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Valori consentiti: BSTR deve avere il formato @ResourceBinary ,- <ResourceID> per consentire la localizzazione perché questa stringa verrebbe esposta all'utente tramite l'interfaccia utente di analisi dei film.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Consente la configurazione dell'analisi del film corrente.</p>
<p>Questa proprietà è obbligatoria per l'elemento WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>Esegue l'analisi della diapositiva di un colore.</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>Esegue l'analisi di un colore negativo.</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>Cerca un valore negativo nero e bianco.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td style="text-align: left;"><p>Riservato per un utilizzo futuro e non è implementato in questo momento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica il numero di elementi archiviati nell'elemento WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Attiva o disattiva la lampada dello scanner.</p>
<p>Facoltativo per gli elementi WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e consigliati per WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>Accendere la lampada.</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>Spegnere la lampada.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Imposta il tempo massimo di conservazione della lampada quando lo scanner non viene utilizzato.</p>
<p>Facoltativo per gli elementi WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER e WIA_CATEGORY_FILM e consigliati per WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_UI4</strong>, accesso: lettura/scrittura, valori validi: 0-0xFFF secondi</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica la larghezza massima, in millesimi di pollice, che viene analizzata nell'asse orizzontale (X) in corrispondenza della risoluzione corrente. È possibile che si tratta della larghezza del feeder del foglio o del letto di analisi, in base al tipo di elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica l'altezza massima, in millesimi di pollice, che viene analizzata nell'asse verticale (Y) in corrispondenza della risoluzione corrente. Può trattarsi dell'altezza del feeder del foglio o del letto di analisi, in base al tipo di elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica la larghezza minima, in millesimi di pollice, che viene analizzata nell'asse orizzontale (X) in corrispondenza della risoluzione corrente.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica l'altezza minima, in millesimi di pollice, che viene analizzata nell'asse verticale (Y) in corrispondenza della risoluzione corrente.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </dl></td>
<td style="text-align: left;"><p>Riservato per un utilizzo futuro e non è implementato in questo momento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Risoluzione ottica orizzontale. Risoluzione ottica orizzontale più elevata supportata in DPI. Questa proprietà è un singolo valore. Non si tratta di un elenco di tutte le risoluzioni che possono essere generate dal dispositivo. Piuttosto, si tratta della risoluzione dell'ottica del dispositivo. Minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli elementi.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Risoluzione ottica verticale. Risoluzione ottica verticale massima supportata in DPI. Questa proprietà è un singolo valore. Non si tratta di un elenco di tutte le risoluzioni generate dal dispositivo. Piuttosto, si tratta della risoluzione dell'ottica del dispositivo. Minidriver crea e gestisce questa proprietà. Questa proprietà è obbligatoria per tutti gli elementi.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </dl></td>
<td style="text-align: left;"><p>Specifica l'orientamento corrente dei documenti da analizzare. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione imposta questa proprietà per definire l'orientamento originale di una pagina o di un'immagine da acquisire. Per informazioni sull'utilizzo di WIA_IPS_ORIENTATION, vedere <strong>WIA_IPS_PAGE_SIZE</strong>.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION si riferisce alla posizione del documento da analizzare sul letto o sul feeder dello scanner. Si tratta dell'orientamento del documento relativo alla direzione dell'analisi. WIA_IPS_ROTATION fa riferimento alla rotazione applicata all'immagine dopo che è stata eseguita l'analisi, appena prima che l'immagine venga trasferita nell'applicazione.
</blockquote>
</div>
<div>
 
</div>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabella seguente include le quattro costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VERTICALE</td>
<td>0 gradi.</td>
</tr>
<tr class="even">
<td>ORIZZONTALE</td>
<td>rotazione in senso antiorario di 90 gradi, relativa all'orientamento verticale.</td>
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

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la dimensione della pagina attualmente impostata per essere analizzata. Un'applicazione imposta questa proprietà per selezionare le dimensioni della pagina da analizzare. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Per le costanti che possono essere usate con questa proprietà, vedere le <a href="-wia-wia2-pagesizeconstants.md"><strong>costanti di dimensione della pagina WIA 2,0</strong></a>. Si noti che queste dimensioni non fisse, in particolare: </p>
<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>Definito dai valori delle proprietà <strong>WIA_IPS_PAGE_HEIGHT</strong> e <strong>WIA_IPS_PAGE_WIDTH</strong> .</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>Le dimensioni della pagina vengono determinate automaticamente dal dispositivo.</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>Dimensioni di pagina personalizzate le cui dimensioni sono già note all'applicazione e al driver di dispositivo.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Il valore della proprietà <strong>WIA_IPS_ORIENTATION</strong> determina l'orientamento della pagina attualmente selezionata. Le proprietà <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> segnalano le dimensioni della pagina, in millesimi di pollice. Queste proprietà devono essere concordate con <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong>, che contengono le dimensioni della pagina in pixel.</p>
<div class="alert">
<blockquote>
[!Note]<br />
I valori validi di tipo WIA_PROP_LIST dipendono da impostazioni valide della proprietà <strong>WIA_IPS_ORIENTATION</strong> . Se, ad esempio, il dispositivo non è in grado di analizzare documenti orientati al paesaggio con un'impostazione WIA_PAGE_A4, WIA_PAGE_A4 non è un valore valido per la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> quando <strong>WIA_IPS_ORIENTATION</strong> è impostato su orizzontale.
</blockquote>
</div>
<div>
 
</div>
<p>Se un'applicazione imposta <strong>WIA_IPS_PAGE_SIZE</strong> su un valore diverso da tre nella tabella precedente, il minidriver deve regolare i valori di <strong>WIA_IPS_PAGE_WIDTH</strong> e <strong>WIA_IPS_PAGE_HEIGHT</strong> alle dimensioni della pagina in millesimi di pollice. Deve anche modificare i valori delle <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> alle dimensioni della pagina in pixel.</p>
<p>Se un'impostazione di extent (<strong>WIA_IPS_XEXTENT</strong> o <strong>WIA_IPS_YEXTENT</strong>) viene modificata in un valore che non corrisponde all'impostazione della dimensione della pagina corrente, minidriver deve modificare il valore della proprietà <strong>WIA_IPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM. Il minidriver deve anche modificare <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> o <strong>WIA_IPS_PAGE_HEIGHT</strong> in base alla nuova impostazione dell'extent.</p>
<p>Se <strong>WIA_IPS_ORIENTATION</strong> è impostato su orizzontale, le impostazioni dell'extent verranno scambiate rispetto ai valori usuali. Se, ad esempio, un'applicazione imposta <strong>WIA_IPS_PAGE_SIZE</strong> su WIA_PAGE_A4, minidriver imposta <strong>WIA_IPS_PAGE_WIDTH</strong> su 11692 e <strong>WIA_IPS_PAGE_HEIGHT</strong> su 8267. Il minidriver deve anche modificare <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> di conseguenza.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> è impostato su WIA_PAGE_CUSTOM, l'impostazione dell'orientamento non viene utilizzata per determinare le dimensioni dell'extent della pagina da analizzare.
</blockquote>
</div>
<div>
 
</div>
<p>Il minidriver è responsabile di garantire che la proprietà <strong>WIA_IPS_ORIENTATION</strong> sia concordata con l'area di selezione corrente. Se un'applicazione modifica il valore di <strong>WIA_IPS_ORIENTATION</strong> a uno non valido per le dimensioni di pagina attualmente selezionate, minidriver deve modificare il valore di <strong>WIA_IPS_PAGE_SIZE</strong> in base a una dimensione di pagina supportata dal nuovo valore di orientamento.</p>
<p>Se un'applicazione imposta la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> su WIA_PAGE_CUSTOM, l'area di selezione corrente non è interessata. Il minidriver WIA dovrebbe ottenere il layout dell'immagine corrente, a partire dalle impostazioni correnti delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> . Se l'impostazione delle dimensioni della pagina produce un'area di selezione esterna al letto dello scanner, il minidriver deve modificare automaticamente i valori delle proprietà <strong>WIA_IPS_XPOS</strong> e <strong>WIA_IPS_YPOS</strong> in impostazioni valide. Se le proprietà <strong>WIA_IPS_PAGE_SIZE</strong> e <strong>WIA_IPS_ORIENTATION</strong> sono impostate contemporaneamente e non sono valide se applicate in combinazione, il minidriver deve avere esito negativo sulle impostazioni dell'applicazione restituendo un errore in <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvvalidateitemproperties</a>.</p>
<p>Nei quattro esempi seguenti vengono illustrati scenari di <strong>WIA_IPS_PAGE_SIZE</strong> diversi.</p>
<ol>
<li>Il driver segnala le impostazioni.</li>
<li>Un'applicazione imposta la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> su WIA_PAGE_LETTER.</li>
<li>Un'applicazione imposta la proprietà <strong>WIA_IPS_ORIENTATION</strong> su Landscape.</li>
<li>Un'applicazione modifica la proprietà <strong>WIA_IPS_XEXTENT</strong> in un valore più piccolo.</li>
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
<p><strong>Esempio 2: un'applicazione imposta la</strong> <strong></strong><strong>Proprietà WIA_IPS_PAGE_SIZE su WIA_PAGE_LETTER</strong>  </p>
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
<p><strong>Esempio 3: un'applicazione imposta la</strong> <strong></strong><strong>Proprietà WIA_IPS_ORIENTATION su Landscape</strong>  </p>
<p>Il letto fisico deve essere in grado di acquisire una pagina originariamente con orientamento orizzontale.</p>
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
<p><strong>Esempio 4: un'applicazione modifica la</strong> <strong></strong> <strong>Proprietà WIA_IPS_XEXTENT in un valore più piccolo</strong></p>
<p>Nell'esempio seguente un'applicazione modifica la proprietà <strong>WIA_IPS_XEXTENT</strong> in 1000. Il minidriver deve presupporre che il nuovo valore contenuto in <strong>WIA_IPS_XEXTENT</strong> non sia più valido per la proprietà <strong>WIA_IPS_PAGE_SIZE</strong> e pertanto debba modificare <strong>WIA_IPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM. Il minidriver deve anche modificare <strong>WIA_IPS_PAGE_WIDTH</strong>.</p>
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
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene l'altezza, in millesimi di pollice, della pagina attualmente selezionata. Minidriver crea e gestisce la proprietà <strong>WIA_IPS_PAGE_HEIGHT</strong> . Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione. Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica l'altezza della pagina la cui proprietà <strong>WIA_IPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM (valore della proprietà <strong>WIA_IPS_PAGE_SIZE</strong> ). <strong>WIA_IPS_PAGE_HEIGHT</strong> deve essere sincronizzato con <strong>WIA_IPS_XEXTENT</strong>, che indica l'altezza, in pixel, della pagina da analizzare.</p>
<p>Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FEEDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene la larghezza della pagina corrente selezionata, in millesimi di pollice. Un'applicazione legge questa proprietà per determinare le dimensioni fisiche della pagina sottoposta a scansione. Se le impostazioni dell'extent sono diverse dalle dimensioni note della pagina, questa proprietà indica la larghezza della pagina la cui proprietà <strong>WIA_IPS_PAGE_SIZE</strong> è impostata su WIA_PAGE_CUSTOM. <strong>WIA_IPS_PAGE_WIDTH</strong> deve essere sincronizzato con il valore di <strong>WIA_IPS_XEXTENT</strong>, che indica la larghezza, in pixel, della pagina da analizzare. Minidriver crea e gestisce questa proprietà.</p>
<p>Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FEEDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Contiene il numero corrente di pagine da acquisire da un feeder di documenti automatico. Minidriver crea e gestisce questa proprietà.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> questo valore è pari a zero fino al numero massimo di pagine che lo scanner è in grado di analizzare. Il valore è ALL_PAGES (= 0) se lo scanner è in grado di eseguire un'analisi continua.</p>
<p>Un'applicazione legge questa proprietà per determinare la capacità della pagina del feeder del documento. L'applicazione imposta anche questa proprietà sul numero di pagine che verranno analizzate.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Se è abilitata la modalità duplex (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> è impostata su Feeder | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> è ancora uguale al numero di pagine da analizzare.
</blockquote>
</div>
<div>
 
</div>
<p>Un foglio di carta conterrà automaticamente due pagine se DUPLEX è abilitato, anche se il lato posteriore della pagina è vuoto.</p>
<p>Se si imposta <strong>WIA_IPS_PAGES</strong> su 1, lo scanner elabora un lato della pagina. Se uno scanner non è in grado di eseguire l'analisi di un solo lato di una pagina in modalità duplex, è consigliabile modificare il valore <strong>WIA_IPS_PAGES</strong> per il membro Inc del membro range della struttura WIA_PROPERTY_INFO su 2. Questo valore segnala all'applicazione che deve richiedere le pagine in multipli di due. Il valore ALL_PAGES (= 0) indica che <em>tutte le</em> pagine attualmente caricate nel Feeder del documento devono essere analizzate.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'impostazione corrente per i pixel bianco e nero. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questo valore per determinare il valore di bianco o nero (a seconda di ciò che l'applicazione sta eseguendo).</p>
<p>Obbligatorio per tutti gli elementi di acquisizione abilitati o archiviati; ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso: lettura/scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Se il dispositivo può essere impostato su un solo valore, creare un tipo di WIA_PROP_LIST e inserire il valore valido al suo interno.</p>
<p>Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PHOTO_WHITE_0</td>
<td>Il bianco è 0 e il nero è 1.</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>Il bianco è 1 e il nero è 0.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Indica la modalità di anteprima per un dispositivo. Un'applicazione imposta questa proprietà per posizionare il dispositivo in modalità di anteprima.</p>
<p>Questa proprietà è obbligatoria per gli elementi WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM, facoltativo per l'elemento WIA_CATEGORY_FEEDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. </p>
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
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica se l'immagine di anteprima esistente può essere aggiornata durante un'anteprima dell'immagine, in risposta a una modifica apportata alle proprietà WIA_IPA_DATATYPE o WIA_IPA_DEPTH.</p>
<p>Questa proprietà è facoltativa per tutti gli elementi abilitati per l'acquisizione che supportano le analisi di anteprima; ovvero WIA_IPS_PREVIEW è supportato con WIA_PREVIEW_SCAN. Sono inclusi gli elementi di tipo WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. </p>
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>È possibile aggiornare l'immagine esistente.</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>È necessario eseguire un'altra analisi di anteprima perché non è possibile aggiornare l'immagine esistente.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'impostazione di rotazione corrente, se implementata. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione imposta questa proprietà per indicare al driver la quantità (se presente) di ruotare l'immagine prima che il driver la restituisca all'applicazione.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION si riferisce alla posizione del documento da analizzare sul letto o sul feeder dello scanner. Si tratta dell'orientamento del documento relativo alla direzione dell'analisi. WIA_IPS_ROTATION fa riferimento alla rotazione applicata all'immagine dopo che è stata eseguita l'analisi, appena prima che l'immagine venga trasferita nell'applicazione.
</blockquote>
</div>
<div>
 
</div>
<p>Il minidriver WIA è responsabile della rotazione dei dati dell'immagine prima di inviarli nuovamente all'applicazione. L'applicazione è responsabile del controllo delle intestazioni di immagine per visualizzare i valori appena ruotati.</p>
<p>Esiste una notevole confusione sulla risoluzione dell'effetto della rotazione sull'area di selezione dell'immagine corrente (definita dalle proprietà <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> e <strong>WIA_IPS_YEXTENT</strong> ).</p>
<p><em>Area di selezione</em> si riferisce all'area selezionata sul letto dello scanner fisico da cui viene acquisita un'immagine. <strong>WIA_IPS_ROTATION</strong> non modifica l'area di selezione. Il driver applica una rotazione in senso antiorario in base a <strong>WIA_IPS_ROTATION</strong> solo dopo che il driver ha acquisito l'area di selezione appropriata. <strong>WIA_IPS_ROTATION</strong> influisce sulle dimensioni dell'immagine di output, quindi tali dimensioni devono essere riflesse nell'intestazione dei dati dell'immagine risultante.</p>
<p>Facoltativo per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Sono definite le costanti di rotazione seguenti.</p>

<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VERTICALE</td>
<td>Il driver non effettuerà la rotazione dell'immagine.</td>
</tr>
<tr class="even">
<td>ORIZZONTALE</td>
<td>Il driver TImpossibile ruota l'immagine di 90 gradi in senso antiorario.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Il driver ruota l'immagine di 180 gradi in senso antiorario.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Il driver ruota l'immagine di 270 gradi in senso antiorario.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica se l'applicazione deve utilizzare il filtro di segmentazione del driver per l'analisi in più aree. È necessario implementare WIA_IPS_SEGMENTATION per gli elementi WIA_CATEGORY_FLATBED e WIA_CATEGORY_FILM se supportano la creazione di elementi figlio con un filtro di segmentazione o se il driver crea elementi figlio per i frame fissi.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le due costanti valide per questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>L'applicazione deve usare il filtro di segmentazione per l'analisi in più aree.</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>Il driver crea gli elementi figlio per l'analisi in più aree. Questa situazione si verifica in genere se lo scanner usa frame fissi a questo scopo.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
È possibile che un driver includa un filtro di segmentazione, ma che ancora WIA_IPS_SEGMENTATION sia impostato su WIA_DONT_USE_SEGMENTATION_FILTER per uno degli elementi (ad esempio, l'elemento WIA_CATEGORY_FILM). Questa situazione può verificarsi se lo scanner usa frame fissi per l'analisi dei film, ma non per l'analisi regolare dagli elementi WIA_CATEGORY_FLATBED.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
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
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Indica se un elemento necessita di un controllo anteprima visualizzato per l'utente. Minidriver crea e gestisce questa proprietà.</p>
<p>Facoltativo per tutti gli elementi abilitati per il trasferimento. Si tratta in genere solo di elementi delle categorie WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e WIA_CATEGORY_FINISHED_FILE.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La tabella seguente contiene le costanti valide per questa proprietà. </p>
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
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica se l'applicazione (o i filtri) può creare elementi figlio sotto l'elemento corrente.</p>
<p>Facoltativo per tutte le categorie di elementi abilitati per il trasferimento: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM e persino WIA_CATEGORY_FOLDER. Se l'archiviazione non supporta il caricamento di nuovi elementi, questa proprietà non deve essere supportata o supportata con il valore <strong>false</strong> .</p>
<p>Gli elementi che supportano WIA_IPS_SEGMENTATION e WIA_USE_SEGMENTATION_FILTER devono supportare anche WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION e devono essere impostati su <strong>true</strong>.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <strong>true</strong> e <strong>false</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica il valore in scala di grigi che determina se un pixel verrà convertito in bianco o nero quando un'immagine viene convertita in monocromatico. I pixel al di sopra della soglia diventano bianchi. I pixel al di sotto della soglia diventano bianchi.</p>
<p>Questa proprietà è obbligatoria per gli elementi di acquisizione che supportano le analisi con 1 BPP e la cui proprietà WIA_IPA_DATATYPE è impostata su WIA_DATA_THRESHOLD.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica se il driver è in grado di trasferire più elementi figlio in una singola chiamata di trasferimento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>L'unico valore possibile per questa proprietà è WIA_TRANSFER_CHILDREN_SINGLE_SCAN. Se questo flag è impostato, il driver è in grado di trasferire più elementi figlio in una singola chiamata di trasferimento. Se il flag non è impostato, il servizio WIA scorre gli elementi figlio in modo ricorsivo e quindi trasferisce ciascuno di tali elementi.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Specifica il numero di byte da caricare per l'elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </dl></td>
<td style="text-align: left;"><p>Specifica il tempo di riscaldamento massimo, in millisecondi, necessario per il dispositivo prima di avviare l'operazione di analisi. Minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione può leggere questa proprietà per determinare il tempo massimo di riscaldamento del dispositivo. Può quindi presentare una finestra di &quot; dialogo in attesa del dispositivo per il riscaldamento &quot; , per informare l'utente che è possibile che si verifichi un'attesa o una pausa prima che succeda qualcosa.</p>
<p>Questa proprietà è obbligatoria per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la larghezza corrente, in pixel, dell'immagine selezionata da acquisire. Un'applicazione imposta questa proprietà per contrassegnare la larghezza di un'area di selezione da acquisire. Questa proprietà deve essere conforme alla proprietà <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . Minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la coordinata x, in pixel, dell'angolo superiore sinistro dell'immagine selezionata. Un'applicazione imposta questa proprietà per contrassegnare l'angolo superiore sinistro dell'area di selezione. Minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la risoluzione orizzontale corrente, in pixel per pollice, per il dispositivo. Un'applicazione imposta questa proprietà per impostare la risoluzione orizzontale. Minidriver crea e gestisce questa proprietà.</p>
<p>Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno. Questo è anche un caso in cui un'impostazione di risoluzione dipende da un'altra soluzione. (La risoluzione verticale può dipendere dalla risoluzione orizzontale).</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Imposta il ridimensionamento orizzontale, in percentuale, che può essere applicato alle immagini analizzate all'interno del dispositivo dello scanner o del relativo driver.</p>
<p>Questa proprietà è facoltativa per tutti gli elementi abilitati per l'acquisizione. ovvero elementi di tipo WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</p>
<p>I valori possono essere compresi tra 1 e massimo VT_I4 (0xFFFF). 100, ad esempio, non prevede alcun ridimensionamento, 050 indica il ridimensionamento fino al 50% della dimensione originale e 200 indica il ridimensionamento fino al 200% delle dimensioni originali.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'altezza corrente, in pixel, dell'immagine selezionata da acquisire. Un'applicazione imposta questa proprietà per contrassegnare l'altezza di un'area di selezione. Questa proprietà deve essere conforme al valore della proprietà <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . Minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </dl></td>
<td style="text-align: left;"><p>Coordinata y corrente, espressa in pixel, dell'angolo superiore sinistro dell'immagine selezionata. Un'applicazione imposta questa proprietà per contrassegnare l'angolo superiore sinistro dell'area di selezione. Minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </dl></td>
<td style="text-align: left;"><p>Contiene la risoluzione verticale corrente, in pixel per pollice, per il dispositivo. Un'applicazione imposta questa proprietà per impostare la risoluzione verticale. Minidriver crea e gestisce questa proprietà.</p>
<p>Se il dispositivo può essere impostato su un solo valore, creare un tipo di <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido al suo interno. Questo è anche un caso in cui un'impostazione di risoluzione dipende da un'altra soluzione. La risoluzione orizzontale può dipendere dalla risoluzione verticale.</p>
<p>Obbligatorio per tutti gli elementi abilitati per l'acquisizione. ovvero gli elementi delle categorie: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE e WIA_CATEGORY_FILM. Non è supportata per gli elementi WIA_CATEGORY_FOLDER.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Questa proprietà è supportata solo da Windows Vista e versioni successive.
</blockquote>
</div>
<div>
 
</div>
<p>Imposta il ridimensionamento verticale, in percentuale, che può essere applicato alle immagini analizzate all'interno del dispositivo dello scanner o del relativo driver.</p>
<p>Questa proprietà è facoltativa per tutti gli elementi abilitati per l'acquisizione. ovvero elementi di tipo WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK e WIA_CATEGORY_FILM.</p>
<p>Tipo: <strong>VT_I4</strong>, accesso: lettura/scrittura o sola lettura, valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE.</p>
<p>I valori possono essere compresi tra 1 e massimo VT_I4 (0xFFFF). 100, ad esempio, non prevede alcun ridimensionamento, 050 indica il ridimensionamento fino al 50% della dimensione originale e 200 indica il ridimensionamento fino al 200% delle dimensioni originali.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




