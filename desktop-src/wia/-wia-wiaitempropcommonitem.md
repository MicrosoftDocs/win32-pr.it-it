---
description: Le costanti di proprietà del dispositivo seguenti devono essere supportate da tutte le interfacce IWiaItem, IWiaItem2 e IWiaDrvItem Interface, a meno che non diversamente indicato nelle descrizioni.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Costanti comuni delle proprietà degli elementi WIA (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6cf9c102e5ba9732369604bea21876af66ca525b596736521e92e59e52ddf9e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207528"
---
# <a name="common-wia-item-property-constants"></a>Costanti comuni delle proprietà degli elementi WIA

Le costanti di proprietà del dispositivo seguenti devono essere supportate da tutte le interfacce [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) e [IWiaDrvItem Interface,](https://msdn.microsoft.com/library/ms793976.aspx) a meno che non diversamente indicato nelle descrizioni.

Il prefisso "WIA IPA" indica una proprietà elemento per tutti i dispositivi ed è la convenzione di denominazione usata \_ \_ in C/C++. A scopo di scripting, queste costanti usano il prefisso "Picture" e fanno parte del tipo enumerato [WiaItemPropertyId.](-wia-wiaitempropertyid.md) Il nome del membro corrispondente dell'enumerazione di script viene visualizzato tra parentesi accanto al nome della costante C/C++ nell'elenco seguente.



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
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td style="text-align: left;">Questo flag controlla l'accesso all'elemento, nonché se l'elemento viene eliminato.<br/> Obbligatorio per tutti gli elementi di WIA 2.0.<br/> Tipo: <strong>VT_I4</strong>; Lettura/scrittura o sola lettura, a seconda della possibilità dell'elemento di modificare i diritti di accesso. Valori validi: WIA_PROP_FLAG<br/> Nella tabella seguente sono riportati i cinque flag validi per questa proprietà.<br/> 
<table>
<thead>
<tr class="header">
<th>Diritto di accesso</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>L'elemento ha accesso in sola lettura.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>L'elemento ha accesso in sola scrittura.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>L'elemento ha accesso di sola eliminazione.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td style="text-align: left;"><p>Questa proprietà è riservata da per un uso futuro e non viene implementata al momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il numero di bit per canale per l'immagine. Il minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi immagine archiviati o abilitati per l'acquisizione di WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Contiene le dimensioni del buffer, in byte, utilizzate durante un trasferimento di dati. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione può leggere questa proprietà per determinare le dimensioni del buffer specificate dal driver per i trasferimenti di dati. Il servizio WIA legge anche questa proprietà per allocare memoria per il minidriver durante il trasferimento dei dati</p>
<p>Facoltativo per tutti gli elementi WIA 2.0 abilitati per il trasferimento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
La <strong>WIA_IPA_BUFFER_SIZE</strong> contiene la quantità minima di dati che un'applicazione può richiedere in qualsiasi momento. Maggiore è la dimensione del buffer, maggiori saranno le richieste al dispositivo. In questo modo il dispositivo può sembrare lento e non risponde, può rallentare le prestazioni complessive del sistema e può utilizzare risorse eccessive. Le dimensioni del buffer troppo piccole possono rallentare le prestazioni del trasferimento dei dati richiedendo molte richieste più piccole. Scegliere una dimensione del buffer ragionevole considerando le dimensioni tipiche di una richiesta di dati al dispositivo e bilanciando il numero di richieste rispetto alle dimensioni di tali richieste.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il numero di byte in una riga di analisi dell'immagine. Il minidriver crea e gestisce questa proprietà.</p>
<p>Facoltativo per tutti gli elementi di WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il numero di canali per pixel per l'immagine. Il minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi immagine archiviati o abilitati per l'acquisizione di WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td style="text-align: left;"><p>Questa proprietà è riservata da per un uso futuro e non viene implementata al momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il tipo di compressione corrente utilizzato. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare il tipo di compressione dell'immagine o imposta questa proprietà per configurare l'impostazione di compressione.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le costanti valide per questa proprietà. Il <strong>simbolo V</strong> indica che la costante è supportata solo in Windows Vista e versioni successive. È disponibile solo tramite <a href="-wia-iwiaitem2.md"><strong>l'interfaccia IWiaItem2.</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Tipo di compressione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Nessuna compressione. Per <strong>altre informazioni,</strong> vedere Nota.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Modalità di compressione automatica. Per <strong>altre informazioni,</strong> vedere Nota.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>Compressione RLE4</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>Compressione RLE8</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>Compressione gruppo 3</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Compressione gruppo 4</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>Compressione JPEG.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>Compressione JBIG.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>Compressione JPEG 2000.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>Compressione PNG.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>Quando questa proprietà è WIA_COMPRESSION_NONE e WIA_IPA_FORMAT è WiaImgFmt_PDFA o WiaImgFmt_XPS; quindi WIA_COMPRESSION_NONE indica che la modalità di compressione non è definita e che lo scanner deve decidere una modalità.</p>
<p>WIA_COMPRESSION_AUTO è un nuovo valore di proprietà definito per la WIA_IPA_COMPRESSION proprietà . Questo valore è valido per tutti gli elementi dell'origine dati immagine programmabili, inclusi Flatbed e Feeder. Quando questo valore è supportato dal mini driver WIA, il client dell'applicazione WIA può impostare WIA_IPA_COMPRESSION per abilitare il rilevamento automatico della modalità di compressione nel dispositivo. WIA_COMPRESSION_AUTO può funzionare con e senza che il colore automatico completo sia supportato o abilitato (WIA_DATA_AUTO e WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO è particolarmente utile con formati di file di trasferimento che supportano più tipi di dati e profondità di bit, ad esempio WiaImgFmt_RAW. Per altre informazioni sui formati di file di trasferimento, vedere WIA_IPA_FORMAT in questa tabella.</p>
<p>È opportuno che il mini driver WIA sosporti WIA_COMPRESSION_AUTO. Quando è supportato, il mini driver WIA non deve mai impostarlo come valore predefinito per WIA_IPA_COMPRESSION; solo l'applicazione WIA può impostare questo valore.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'impostazione del tipo di dati corrente per il dispositivo. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare il tipo di dati dell'immagine. Un'applicazione scrive questa proprietà per impostare il tipo di dati corrente dell'immagine che sta per essere trasferita.</p>
<p>Questa proprietà è obbligatoria per tutti gli elementi di WIA 2.0. Deve essere di lettura/scrittura per tutti gli elementi abilitati per l'acquisizione di WIA 2.0 e di sola lettura per gli elementi di archiviazione WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso per i sistemi operativi Windows Vista: questa proprietà è Di sola lettura per le fotocamere e Lettura/Scrittura per gli scanner. Accesso per Windows Vista e versioni successive: questa proprietà è di sola lettura per gli elementi WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE e lettura/scrittura per tutte le altre categorie di elementi WIA 2.0; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono presenti le sei costanti valide con quando <strong>WIA_IPA_FORMAT</strong> è impostata su WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Tipo di dati</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Valido per tutti gli elementi dell'origine dati immagine programmabili, inclusi Flatbed e Feeder. Quando questo valore è supportato dal mini driver WIA, il client dell'applicazione WIA può impostare WIA_IPA_DATATYPE per abilitare il rilevamento automatico del colore nel dispositivo. Quando WIA_DATA_AUTO è impostato, il mini driver WIA deve aggiornare WIA_IPA_DEPTH nello stesso elemento a WIA_DEPTH_AUTO (che deve essere un valore supportato se il dispositivo supporta il colore automatico).<br/> Si tratta di un valore facoltativo, ma è obbligatorio quando WIA_DEPTH_AUTO è supportato per WIA_IPA_DEPTH.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>I dati di analisi sono di colore rosso, verde, blu (RGB). Il formato a colori completo viene descritto usando le proprietà WIA seguenti: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>Uguale a WIA_DATA_COLOR ad eccezione del fatto che i dati vengono dithering usando il modello dithering attualmente selezionato.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>Uguale a WIA_DATA_COLOR ad eccezione del fatto che il valore soglia viene usato durante l'analisi dei dati. I valori di colore <a href="https://msdn.microsoft.com/library/ms796233.aspx">sul WIA_IPS_THRESHOLD</a> vengono convertiti in luminosità completa; I colori sotto questo valore vengono convertiti in nero.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>I dati di analisi vengono dithering usando il modello dithering attualmente selezionato.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>I dati di analisi rappresentano l'intensità. La tavolozza è una scala di grigi fissa con spazi uguali con una profondità specificata <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> proprietà .</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>La soglia è di un bit per pixel di dati in bianco e nero. I dati sul valore corrente di <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> vengono convertiti in bianco; I dati in questo valore vengono convertiti in nero.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La <strong>WIA_IPA_DATATYPE</strong> viene usata anche per descrivere il tipo di trasferimento di dati RAW da usare quando l'applicazione imposta WiaImgFmt_RAW. Il driver deve impostare la <strong>proprietà WIA_IPA_DATATYPE</strong> su un elenco di valori consentiti da cui l'applicazione può selezionarne uno.</p>
<p>Se il dispositivo può essere impostato su un solo valore, creare un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido.</p>
<p>Controllare la <a href="https://msdn.microsoft.com/library/ms795935.aspx">proprietà WIA_IPA_DEPTH</a> per determinare la profondità in bit. Questa proprietà contiene in genere un singolo valore per le fotocamere.</p>
<p>Nella tabella seguente sono elencate le costanti valide con WIA_IPA_DATATYPE <strong>quando</strong> <strong>WIA_IPA_FORMAT</strong> è impostato su WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Tipo di dati</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>I dati di analisi rappresentano l'intensità. La tavolozza è una scala di grigi fissa, con uguale spazio con una profondità specificata dalla <a href="https://msdn.microsoft.com/library/ms795935.aspx">proprietà</a> WIA_IPA_DEPTH. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 1.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>I dati di analisi si trova nello spazio colori BGR (blu-verde-rosso). Il formato a colori completo viene descritto usando le seguenti proprietàWIA: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>I dati di analisi si trova nello spazio colore ciano-magenta-giallo (CMY). Il formato a colori completo viene descritto usando le stesse proprietà WIA di WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>I dati di analisi si trova nello spazio colore ciano-magenta-giallo-nero (CMYK). Il formato a colori completo viene descritto usando le stesse proprietà WIA di WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 4.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>I dati di analisi si trova nello spazio colore rosso-verde-blu (RGB). Il formato a colori completo viene descritto usando le stesse proprietà WIA di WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>I dati di analisi si trova nello spazio di colore luminance-blue difference-red difference (YUV). Il formato a colori completo viene descritto usando le stesse proprietà WIA di WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>I dati di analisi si trova nello spazio di colore luminance-blue difference-red difference-black (YUVK). Il formato a colori completo viene descritto usando le stesse proprietà WIA di WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> deve essere impostato su 4.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH contiene l'impostazione della profondità in bit di un'immagine. Il minidriver crea e gestisce questa proprietà. Un'applicazione legge questa proprietà per determinare l'impostazione della profondità in bit dell'immagine. L'applicazione potrebbe anche essere in grado di impostare questo valore sulla profondità in bit desiderata.</p>
<p>Se il dispositivo può essere impostato su un solo valore, creare un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> e inserire il valore valido.</p>
<p>Questa proprietà è obbligatoria per tutti gli elementi di WIA 2.0. Deve essere di lettura/scrittura per tutti gli elementi abilitati per l'acquisizione di WIA 2.0 e di sola lettura per gli elementi di archiviazione WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso per i sistemi operativi Windows Vista: Lettura/Scrittura; Accesso per Windows Vista e versioni successive: questa proprietà è di sola lettura per gli elementi WIA_CATEGORY_FOLDER e WIA_CATEGORY_FINISHED_FILE e lettura/scrittura per tutte le altre categorie di elementi WIA 2.0; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO è definito come 0 bit per pixel ed è un nuovo valore di proprietà definito per l'WIA_IPA_DEPTH. Questo valore è valido per tutti gli elementi dell'origine dati immagine programmabili, inclusi Flatbed e Feeder. Quando WIA_DEPTH_AUTO è supportato dal mini driver WIA, il client dell'applicazione WIA può impostare WIA_IPA_DEPTH su questo valore, per abilitare il rilevamento automatico del colore nel dispositivo. Quando WIA_DEPTH_AUTO è impostato, il mini driver WIA deve aggiornare WIA_IPA_DATATYPE nello stesso elemento a WIA_DATA_AUTO (che deve essere un valore supportato, se il dispositivo supporta il colore automatico).</p>
<p>WIA_DEPTH_AUTO è un valore facoltativo, ma diventa obbligatorio quando WIA_DATA_AUTO è supportato per WIA_IPA_DATATYPE.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'estensione del nome file per un formato di file specifico. Il minidriver crea e gestisce questa proprietà.</p>
<p>Facoltativo per tutti gli elementi WIA 2.0 abilitati per il trasferimento.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Il driver aggiorna questa proprietà per riflettere il valore corrente della <a href="https://msdn.microsoft.com/library/ms796440.aspx">proprietà</a> WIA_IPA_FORMAT proprietà .</p>
<p>Ad esempio, se <strong>WIA_IPA_FORMAT</strong> è WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> deve essere <strong>jpg.</strong> Se <strong>WIA_IPA_FORMAT</strong> è WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION deve essere BMP.</p>
<div class="alert">
<blockquote>
[!Note]<br />
L'estensione del nome file non include il punto.
</blockquote>
</div>
<div>
 
</div>
<p>Questa proprietà è consigliata per i driver che supportano i formati standard ed è necessaria per i driver che implementano formati definiti dall'utente. Informa l'applicazione dell'estensione di file corretta da usare durante il trasferimento di file in formato privato. Ad esempio, se A. Datum Corporation ha creato un driver WIA che ha trasferito un file in un nuovo formato, la società potrebbe specificare &quot; un'estensione adc &quot; . Ciò consente alle applicazioni di trasferire dati in tale formato in un file e di creare un nome file, ad esempio <em>myfile.adc,</em>utile per altri utenti che comprendono la nuova estensione.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il formato corrente dell'immagine che sta per essere trasferita.</p>
<p>Un'applicazione legge questa proprietà per determinare il formato dell'immagine che sta per ricevere. Un'applicazione scrive questa proprietà per impostare il formato. Questa proprietà dipende dalla proprietà <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> proprietà . Il minidriver crea e gestisce questa proprietà.</p>
<p>Se il dispositivo può essere impostato su <a href="-wia-property-attributes.md"></a> un solo valore, creare un WIA_PROP_LIST e inserire il valore valido.</p>
<p>Tipo: <strong>CLSID</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono elencate le costanti valide per questa proprietà. L'asterisco * indica che la costante non è supportata in Windows Vista. È disponibile solo tramite <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>l'interfaccia IWiaItem.</strong></a> Il doppio asterisco ** indica che la costante non è supportata in Windows Server 2003 o Windows Vista. Il <strong>simbolo V</strong> indica che la costante è supportata solo in Windows Vista e versioni successive. È disponibile solo tramite <a href="-wia-iwiaitem2.md"><strong>l'interfaccia IWiaItem2.</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Formato</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>Formato audio AIFF</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>Formato audio MP3</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>Formato audio WAV</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>Formato audio WMA</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF**</td>
<td>Formato video ASF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI**</td>
<td>Formato video AVI</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Windows bitmap con un file di intestazione</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF*</td>
<td>Formato del file di immagine della fotocamera</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>Formato di stampa DPOF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metafile Windows esteso</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>File eseguibile</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Formato di file scambiabile</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>Formato FlashPix</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>Formato immagine GIF</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>Formato HTML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows formato di file dell'icona</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>Formato JBIG (Joint Bi-level Image Experts Group).</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Formato compresso JPEG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>Formato compresso JPEG 2000</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>Formato compresso JPEG 2000</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows bitmap senza un file di intestazione</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Formato PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG**</td>
<td>Formato video MPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato di file Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Formato di file Apple</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>Formato PNG W3C</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Formato non elaborato solo per i trasferimenti di dati</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Formato RGB non elaborato</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Formato di file di testo RTF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>File script</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>File di testo</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>Codifica UNICODE a 16 bit</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows metafile</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>File XML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>Formato del pacchetto XPS</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Quando questa proprietà è WiaImgFmt_PDFA o WiaImgFmt_XPS e WIA_IPA_COMPRESSION è WIA_COMPRESSION_NONE; quindi il secondo valore indica che la modalità di compressione non è definita e che lo scanner deve decidere una modalità.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il nome completo dell'elemento (il nome dell'elemento insieme alle informazioni sul percorso). Il nome completo dell'elemento corrisponde al parametro <em>bstrFullItemName</em> della funzione dell'utilità del servizio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem.</a> Un'applicazione legge questa proprietà per determinare l'elemento attualmente in uso e la posizione dell'elemento nell'albero degli elementi. Ogni elemento deve avere un nome univoco. Le applicazioni usano in genere il nome completo dell'elemento per cercare gli elementi nell'albero degli elementi. Il servizio WIA crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi di WIA 2.0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td style="text-align: left;"><p>Questa proprietà è riservata per un uso futuro e non viene implementata in questo momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il nome ICM profilo personalizzato necessario per decodificare correttamente l'immagine. Un'applicazione legge questa proprietà per determinare il profilo ICM da usare durante l'elaborazione dell'immagine. Il servizio WIA crea e gestisce questa proprietà in base alla voce ICMProfiles nel file di installazione del driver.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td style="text-align: left;"><p>Supportato solo in Windows Vista e versioni successive.</p>
<p>Gli elementi WIA 2.0 sono raggruppati in categorie che definiscono come deve essere trattato o usato <a href="-wia-iwiaitem2.md"><strong>un elemento IWiaItem2.</strong></a> Ad esempio, se l'elemento rappresenta un feeder, l'applicazione deve aspettarsi che contenga le proprietà obbligatorie dell'alimentatore di documenti e funzioni come un feeder di documenti. Se l'elemento rappresenta un file completato, un'applicazione WIA 2.0 deve considerarlo in questo modo, presupponendo che i dati siano statici e si trovino nel dispositivo. Le regole per ogni elemento verranno definite nei singoli documenti di specifica.</p>
<p>Obbligatorio per tutti gli elementi WIA 2.0.</p>
<p>Tipo: <strong>VT_CLSID</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-wia2-itemcategoryguids.md"><strong>GUID categoria elemento</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td style="text-align: left;"><p>Contiene i flag descrittivi per un elemento WIA. I flag di elemento sono gli stessi del <em>parametro lObjectFlags</em> della funzione dell'utilità del servizio <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem.</a> Il servizio WIA crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare i valori descrittivi del flag dell'elemento.</p>
<p>Tipo: <strong>VT_I4</strong> accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportati i flag validi per questa proprietà. Un asterisco * indica che il flag non è supportato in Windows Vista o versioni successive. È disponibile solo tramite <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>l'interfaccia IWiaItem.</strong></a> Un doppio asterisco ** indica che il flag non è supportato in Windows Server 2003 o Windows Vista o versioni successive. Il <strong>simbolo V</strong> indica che il flag è supportato solo in Windows Vista e versioni successive. È disponibile solo tramite <a href="-wia-iwiaitem2.md"><strong>l'interfaccia IWiaItem2.</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Contrassegno</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>Questo elemento supporta il <strong>metodo IWiaItem::AnalyzeItem</strong> (descritto nella documentazione di Platform SDK). Questo elemento supporta anche la generazione automatica di elementi figlio. Questa funzionalità è utile per il rilevamento dell'area o la scomposizione della pagina.</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>Questo elemento supporta l'audio. Questo flag è valido solo per gli elementi per cui è impostato anche il flag <strong>WiaItemTypeFile.</strong></td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>Solo per le cartelle. Questo flag indica che le immagini in questa cartella sono state prelevate in una sequenza temporale continua.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>Questo elemento è contrassegnato per l'eliminazione, questo elemento è stato eliminato, questo elemento non esiste o il contenuto di questo elemento non è valido.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>Questo elemento è un file di documento in uno dei formati di documento contenuti <strong>WIA_IPA_FORMAT</strong> proprietà . Questi formati includono quelli per i file non di immagine, ad esempio .txt, .htm e .doc file.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDevice</td>
<td>Questo elemento rappresenta un dispositivo connesso.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDisconnected</td>
<td>Questo elemento rappresenta un dispositivo disconnesso.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFile</td>
<td>L'elemento supporta i trasferimenti di file.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>L'elemento è una cartella.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>L'elemento non è inizializzato o è stato eliminato.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>Questo elemento è stato generato da un'applicazione o dal driver.</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>Questo elemento supporta gli allegati e attualmente contiene allegati.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanorama*</td>
<td>Questo elemento rappresenta un'immagine panoramica orizzontale. Questo flag è valido solo per gli elementi per cui è impostato anche il flag <strong>WiaItemTypeFolder.</strong></td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>L'elemento è un file di immagine. Questo flag è valido solo per gli elementi per cui è impostato anche il flag <strong>WiaItemTypeFile.</strong></td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>L'elemento è un'origine dati programmabile e segue un set di regole di configurazione predefinite basate su <strong>WIA_IPA_ITEM_CATEGORY</strong>.</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>Questo elemento è l'elemento radice, che è l'elemento padre di tutti gli elementi di funzionalità supportati dal dispositivo.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>Questo flag indica spazio di archiviazione aggiuntivo per gli elementi delle cartelle. I driver WIA specificano gli elementi in termini di immagini e cartelle. Non esistono proprietà WIA che descrivono le caratteristiche di un elemento di archiviazione, ad esempio lo spazio di archiviazione rimanente, la velocità di scrittura o il tipo di supporto. È possibile aggiungere proprietà specifiche del fornitore che espongono queste informazioni. Queste proprietà sono accessibili solo alle applicazioni o alle estensioni scritte per riconoscerle.</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>Questo elemento può essere usato per trasferire i dati.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTwainCapabilityPassThrough</td>
<td>Questo tipo indica che il dispositivo WIA è in grado di ricevere i dati delle funzionalità TWAIN dal livello di compatibilità TWAIN. Se questo tipo è impostato, qualsiasi funzionalità TWAIN non compresa dal livello di compatibilità TWAIN verrà passata al driverWIA. Questo valore è valido solo per l'elemento radice.</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>Questo elemento supporta lo streaming di video.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanorama*</td>
<td>Questo elemento rappresenta un'immagine panoramica verticale. Questo flag è valido solo per gli elementi per cui è impostato anche il flag <strong>WiaItemTypeFolder.</strong></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Alcuni di questi flag sono obbligatori o facoltativi per gli elementi WIA 2.0, in base alla categoria dell'elemento, come illustrato in questa tabella.</p>

<table>
<thead>
<tr class="header">
<th>Categoria dell'elemento</th>
<th>Obbligatoria</th>
<th>Facoltativo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>WiaItemTypeRoot WiaItemTypeFolder</td>
<td>WiaItemTypeDevice WiaItemTypeDisconnected</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (se sono supportati più elementi delle aree di analisi, questo flag è facoltativo solo per l WIA_CATEGORY_FLATBED radice.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (se WIA_CATEGORY_FEEDER_FRONT e WIA_CATEGORY_FEEDER_BACK sono presenti elementi, questo flag è facoltativo solo per l'WIA_CATEGORY_FEEDER radice.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (radice)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>Nessuno</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (elementi figlio)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>Nessuno</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>WiaItemTypeStorage WiaItemTypeFolder</td>
<td>WiaItemTypeDeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>WiaItemTypeFile WiaItemTypeTransfer</td>
<td>WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il nome dell'elemento. Un'applicazione legge questa proprietà per determinare l'elemento attualmente in uso. Ogni elemento ha un nome univoco. Il servizio WIA crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi WIA 2.0.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Contiene le dimensioni correnti, in byte, dei dati associati all'elemento. Il minidriver crea e gestisce questa proprietà.</p>
<p>Contains è la dimensione totale dei dati trasferiti. Se questo valore è zero, significa che il minidriver non ha informazioni sulla dimensione esatta dei dati. Questo è comune per i dati compressi. Un'applicazione legge questo valore per determinare le dimensioni dell'acquisizione prima che venga verificata. Il servizio WIA legge questa proprietà per facilitare l'allocazione della memoria per i trasferimenti di dati. Per altre informazioni, vedere Trasferimento di dati in un'applicazione <a href="https://msdn.microsoft.com/library/ms792198.aspx">WIA</a> se la proprietà è impostata su zero e TYMED è configurato per un trasferimento di file, il servizio WIA non alloca memoria per il minidriver WIA.</p>
<p>Obbligatorio per tutti gli elementi WIA 2.0 abilitati per il trasferimento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td style="text-align: left;"><p>Contiene l'ora in cui l'immagine è stata acquisita in origine. Il minidriver crea e gestisce questa proprietà. Questa proprietà deve essere segnalata come vettore di otto valori <strong>WORD</strong> sotto forma di struttura SYSTEMTIME (descritta nella documentazione di Platform SDK).</p>
<p>Facoltativo per tutti gli elementi WIA 2.0.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> accesso: Lettura/Scrittura o Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td style="text-align: left;"><p>Supportato solo in Windows Vista e versioni successive.</p>
<p>Specifica il numero di elementi archiviati nell'WIA_CATEGORY_FOLDER elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Specifica la dimensione minima del buffer utilizzata nei trasferimenti di dati. Se il trasferimento dei dati viene eseguito tramite un meccanismo di callback, il valore della proprietà può essere ridotto fino a 64 KB. Tuttavia, se il trasferimento è su file, il valore della proprietà è il numero di byte necessari per trasferire una pagina di dati alla volta. Il minidriver crea e gestisce questa proprietà WIA.</p>
<p>Facoltativo per tutti gli elementi WIA 2.0 abilitati per il trasferimento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il numero di righe contenute nell'immagine (altezza verticale dell'immagine in pixel). Il minidriver crea e gestisce questa proprietà.</p>
<p>Facoltativo per tutti gli elementi WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il numero di pixel in ogni riga dell'immagine (larghezza dell'immagine in pixel). Il minidriver crea e gestisce questa proprietà.</p>
<p>Facoltativo per tutti gli elementi WIA 2.0.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td style="text-align: left;"><p>Questa proprietà non è supportata in Windows Vista e versioni successive.</p>
<p>Contiene le opzioni di creazione di un pacchetto di dati immagine. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare le opzioni di creazione di un pacchetto di immagini o imposta le opzioni di creazione di un pacchetto di immagini corrente.</p>
<p>Tipo: <strong>VT_I4</strong>; Accesso: Lettura/Scrittura; Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Se il dispositivo può essere impostato su un solo valore, creare un WIA_PROP_LIST e inserire il valore valido.</p>
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
<td>WIA_PACKED_PIXEL</td>
<td>I dati dell'immagine sono in formato packed pixel.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>I dati dell'immagine sono in formato planare.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contiene il formato preferito per le immagini che questo minidriver trasferisce. Il minidriver crea e gestisce questa proprietà.</p>
<p>Obbligatorio per tutti gli elementi WIA 2.0 abilitati per il trasferimento.</p>
<p>Tipo: <strong>CLSID</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td style="text-align: left;"><p>Specifica un CLSID che rappresenta un set di valori di proprietà del dispositivo. Se un driver di dispositivo implementa questa funzionalità, le applicazioni usano questa proprietà per determinare se il dispositivo supporta un set di valori.</p>
<p>Tipo: <strong>CLSID</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le 12 costanti valide con questa proprietà.</p>

<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Definizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Bitmap MicrosoftWindows con un file di intestazione</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Metafile Windows esteso</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Formato di file scambiabile</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>Formato FlashPix</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>Formato immagine GIF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows formato di file dell'icona</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Formato compresso JPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Formato di file Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>Formato PNG W3C</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows bitmap senza un file di intestazione</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows metafile</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Supportato solo in Windows Vista e versioni successive.</p>
<p>Contiene il numero di bit in ogni canale. Questa proprietà deve essere segnalata come vettore di tutti i valori BYTE quanti sono i canali, dove il primo BYTE corrisponde al numero di bit nel primo canale, il secondo byte al numero di bit nel secondo canale e così via. Devono essere presenti tutte le voci quante sono i canali in base WIA_IPA_CHANNELS_PER_PIXEL. Il driver imposta tale proprietà quando l'applicazione passa a WiaImgFmt_RAW. Per i sottotipi noti, sono presenti tutte le voci elencate nella tabella in WIA_IPA_RAW_SUBTYPE.</p>
<p>Tipo: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td style="text-align: left;"><p>Questa proprietà è riservata da per un uso futuro e non viene implementata al momento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td style="text-align: left;"><p>Specifica se eliminare le pagine delle proprietà generali per gli elementi nel dispositivo.</p>
<p>Questa proprietà è disponibile in Windows XP e versioni successive.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Sola lettura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Nella tabella seguente sono riportate le costanti valide per questa proprietà. L'asterisco * indica che la costante non è valida con Windows Vista e versioni successive. È disponibile solo tramite <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>l'interfaccia IWiaItem.</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL*</td>
<td>Eliminare la pagina delle proprietà generale dell'elemento per una fotocamera.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Eliminare la pagina delle proprietà generale dell'elemento per uno scanner.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td style="text-align: left;"><p>Questa proprietà contiene l'impostazione del metodo di trasferimento. Il minidriver crea e gestisce questa proprietà.</p>
<p>Un'applicazione legge questa proprietà per determinare il metodo di trasferimento dei dati del minidriver.</p>
<p>Obbligatorio per tutti gli elementi WIA 2.0 abilitati per il trasferimento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Nella tabella seguente sono riportate le costanti valide per questa proprietà. L'asterisco * indica costanti non valide con Windows Vista e versioni successive. Sono disponibili solo tramite <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>l'interfaccia IWiaItem.</strong></a></p>

<table>
<thead>
<tr class="header">
<th>Tipo di trasferimento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK*</td>
<td>Trasferire un'immagine in memoria, in bande.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK*</td>
<td>Trasferire più immagini in memoria, in bande.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Trasferire un'immagine in un file.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Trasferire un'immagine in un file.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Supportato solo in Windows Vista e versioni successive.</p>
<p>Specifica il numero di byte da caricare per un elemento.</p>
<p>Tipo: <strong>VT_I4</strong>, Accesso: Lettura/Scrittura, Valori validi: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




