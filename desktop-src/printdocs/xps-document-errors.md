---
description: Nella tabella seguente sono elencati tutti i valori HRESULT che possono essere restituiti dai metodi dell'API documento XPS.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: Errori relativi ai documenti XPS (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226899"
---
# <a name="xps-document-errors"></a>Errori del documento XPS

Nella tabella seguente sono elencati tutti i valori **HRESULT** che possono essere restituiti dai metodi dell'API documento XPS. Si noti che non tutti i metodi restituiscono tutti i valori restituiti elencati in questa tabella.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice/valore restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </dl></td>
<td>L'interfaccia dispone già di un proprietario.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </dl></td>
<td>Le dimensioni della casella di spurgo non sono compatibili con le dimensioni della pagina.<br/> Il valore della larghezza della casella di spurgo deve essere maggiore o uguale alla larghezza della pagina, più il valore assoluto della coordinata x dell'origine della casella di spurgo. Il valore di altezza della casella di spurgo deve essere maggiore o uguale all'altezza della pagina più il valore assoluto della coordinata y dell'origine della casella di spurgo. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </dl></td>
<td>Un elemento <strong>PathGeometry</strong> contiene un set di figure di percorso specificate con l'attributo <strong>Figures</strong> o con un elemento <strong>PathFigure</strong> figlio. Le figure di percorso di una geometria non possono avere sia l'attributo <strong>figure</strong> che un elemento <strong>PathFigure</strong> figlio. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </dl></td>
<td>Un elemento <strong>ResourceDictionary</strong> che specifica un dizionario risorse remoto nell'attributo di <strong>origine</strong> non deve contenere elementi figlio di definizione di risorsa.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </dl></td>
<td>Il valore della posizione del cursore non è in ordine. I valori del percorso devono essere ordinati in ordine crescente. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </dl></td>
<td>Le interruzioni del punto di inserimento sono state specificate per una stringa vuota. in alternativa, l'indice di salto del cursore ha superato la lunghezza della stringa Unicode. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </dl></td>
<td>Un valore di colore non è compreso nell'intervallo.<br/> Per <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> tipi di colore, il valore del canale alfa deve essere maggiore o uguale a 0,0 e minore o uguale a + 1,0.<br/> Per <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> tipi di colore, <strong>channelValues [0]</strong> che rappresenta il valore del canale alfa deve essere maggiore o uguale a 0,0 e minore o uguale a + 1,0. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </dl></td>
<td>Un oggetto visivo in un dizionario risorse ha l'attributo <strong>Name</strong> , che non può essere specificato negli elementi figlio di un elemento <strong>ResourceDictionary</strong> .<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </dl></td>
<td>Un oggetto con questo nome esiste già nel dizionario.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </dl></td>
<td>Un oggetto con questo nome di chiave esiste già nel dizionario.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </dl></td>
<td>Riservato.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </dl></td>
<td>Il rettangolo della casella di sfiato contiene uno o più valori non validi. Vedere la descrizione del parametro per i valori validi. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </dl></td>
<td>Il rettangolo della casella di contenuto contiene uno o più valori non validi. Vedere la descrizione del parametro per i valori validi. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </dl></td>
<td>La stringa del tipo di contenuto non è valida.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </dl></td>
<td>Valore <strong>float</strong> non valido. È un valore NAN (infinito).<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </dl></td>
<td>L'URI del tipo di carattere non è valido, probabilmente perché contiene frammenti vuoti o caratteri non validi.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </dl></td>
<td>La lingua specificata non è valida o non è formattata correttamente.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </dl></td>
<td>Il nome della chiave di ricerca fa riferimento a un oggetto che non è il tipo corretto per la chiamata; Se, ad esempio, il metodo restituisce un pennello ma il nome della chiave di ricerca fa riferimento a un oggetto Geometry.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </dl></td>
<td>Il markup letto contiene un elemento o un attributo che non è conforme alla <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">specifica del documento XML</a>.<br/>
<blockquote>
[!Note]<br />
Per rappresentare i valori a virgola mobile, XPS OM usa il tipo di dati <strong>float</strong> anziché <strong>Double</strong>. Se un documento XPS dispone di un elemento con dati a virgola mobile che non rientra in un valore <strong>float</strong> , questo errore viene restituito quando tale valore viene rilevato durante la deserializzazione.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </dl></td>
<td>La stringa passata non è un nome valido, in base alla specifica del documento XML. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </dl></td>
<td>Riservato.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </dl></td>
<td>Le dimensioni della pagina contengono un valore di dimensione della pagina non valido. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </dl></td>
<td>In base alla <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">specifica del documento XML</a>, la stringa della chiave di ricerca non è valida.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </dl></td>
<td>Il tipo di immagine di anteprima non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </dl></td>
<td>È stato trovato un markup XML non corretto o formattato in modo errato.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </dl></td>
<td>In una o più strutture <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> un elemento è fuori sequenza. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </dl></td>
<td>I mapping dei glifi superano il numero di indici di glifi.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </dl></td>
<td>Errore nei mapping dei glifi.<br/> Se la stringa Unicode è vuota, questo errore indica che è stato definito anche il mapping di un glifo. I mapping dei glifi non devono essere definiti se la stringa Unicode è vuota.<br/> Se la stringa Unicode non è vuota, questo errore indica che è stato definito un mapping del glifo per i glifi al di fuori della stringa Unicode. Non è possibile definire i mapping dei glifi per i glifi che non rientrano nella lunghezza della stringa Unicode.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </dl></td>
<td>Il parametro del profilo colori è <strong>null</strong>, ma è previsto un profilo colori. Quando il tipo di colore è XPS_COLOR_TYPE_CONTEXT, è necessario un profilo colori. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </dl></td>
<td>Una pagina si riferisce a risorse eliminabili, ma non specifica un nome di parte DiscardControl.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </dl></td>
<td><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter:: AddPage</strong></a> è stato chiamato prima di <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter:: StartNewDocument</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </dl></td>
<td>Il pacchetto non contiene un FixedDocumentSequence.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </dl></td>
<td>L'interfaccia <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> richiede un URI del tipo di carattere, ma non ne è stato specificato uno.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </dl></td>
<td>L'interfaccia <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> senza una stringa Unicode non specifica alcun indici di glifi. Un'interfaccia <strong>IXpsOMGlyphs</strong> deve specificare una stringa Unicode o una matrice di indici di glifi.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </dl></td>
<td>Non è stato possibile trovare una risorsa immagine per il pennello immagine.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </dl></td>
<td>La risorsa remota ha un oggetto imprevisto.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </dl></td>
<td>La pagina non è stata denominata; lo stato della destinazione del collegamento ipertestuale può essere impostato solo se la pagina ha un nome.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </dl></td>
<td>FixedDocument non contiene parti FixedPage. Un documento XPS deve contenere almeno una parte FixedPage.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </dl></td>
<td>Il riferimento alla pagina non dispone di una pagina corrispondente.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </dl></td>
<td>Non è stato fatto riferimento A una parte di destinazione richiesta.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </dl></td>
<td>Non è stato specificato alcun flusso per la risorsa.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </dl></td>
<td>Impossibile trovare la parte FixedDocument a cui fa riferimento il FixedDocumentSequence. Un documento XPS deve contenere almeno un FixedDocument.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </dl></td>
<td>Impossibile trovare la parte FixedPage a cui fa riferimento FixedDocument. Un documento XPS deve contenere almeno una parte FixedPage.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </dl></td>
<td>La parte della destinazione della relazione non è presente nella relazione del pacchetto.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </dl></td>
<td>Nessun attributo <strong>x:Key</strong> specificato per la risorsa.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </dl></td>
<td>La risorsa a cui fa riferimento la pagina o il contenuto del dizionario remoto non esiste come relazione di pagina.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </dl></td>
<td>Il tipo di carattere limitato a cui si fa riferimento non è stato specificato nella chiamata a <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter:: StartNewDocument</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </dl></td>
<td>Il numero di voci della matrice di dati del segmento è inferiore a quello della matrice dei tipi di segmento. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un FixedDocumentSequence a un pacchetto che ne contiene già uno. Un documento XPS deve contenere solo una parte FixedDocumentSequence.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un ticket di stampa a livello di documento a un FixedDocument che ne contiene già uno. Un FixedDocument in un documento XPS può contenere un solo ticket di stampa a livello di documento.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un ticket di stampa a livello di processo a un FixedDocumentSequence che ne contiene già uno. FixedDocumentSequence in un documento XPS può contenere un solo ticket di stampa a livello di processo.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un ticket di stampa a livello di pagina a un elemento FixedPage che ne contiene già uno. Un elemento FixedPage in un documento XPS può contenere un solo ticket di stampa a livello di pagina.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </dl></td>
<td>La raccolta di tipi di carattere con restrizioni contiene una voce di tipo carattere limitata ripetuta. Ogni voce del tipo di carattere può essere presente solo una volta nella raccolta.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </dl></td>
<td>Una risorsa con tale nome di parte esiste già.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un'immagine di anteprima a un pacchetto che ne contiene già uno. Un documento XPS può contenere una sola immagine di anteprima a livello di pacchetto.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un'immagine di anteprima a livello di pagina a un elemento FixedPage che ne contiene già uno. Un FixedPage in un documento XPS può contenere una sola immagine di anteprima a livello di pagina.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </dl></td>
<td>Una voce contiene un valore negativo, ma deve contenere un valore non negativo. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </dl></td>
<td>È stato effettuato un tentativo di aggiungere un riferimento a un dizionario remoto a un dizionario remoto. Un dizionario remoto non può fare riferimento A un altro dizionario remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </dl></td>
<td>Un puntatore a interfaccia non punta a un'implementazione di interfaccia riconosciuta. L'implementazione personalizzata delle interfacce API per documenti XPS non è supportata.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </dl></td>
<td>La raccolta di arresti sfumatura ha meno di due arresti. Una raccolta di arresti sfumati deve avere almeno due cursori sfumatura.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </dl></td>
<td>La stringa di testo è stata specificata come orientata lateralmente e da destra a sinistra. Se il testo è orientato lateralmente, non può avere un livello BiDi che è un valore dispari (da destra a sinistra). Analogamente, se il livello BiDi è un valore dispari, il testo non può essere orientato lateralmente.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </dl></td>
<td>I mapping dei glifi non corrispondono al contenuto della stringa Unicode.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </dl></td>
<td>Il writer del pacchetto non è stato chiuso prima del rilascio.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </dl></td>
<td>Una relazione fa riferimento a una parte esterna al documento XPS. Tutto il contenuto di cui eseguire il rendering in un documento XPS deve essere contenuto nel documento XPS.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </dl></td>
<td>Riservato.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </dl></td>
<td><em>Riservato</em>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </dl></td>
<td>Si è verificato un overflow <strong>size_t</strong> durante un tentativo di copia di una stringa in un nuovo buffer.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </dl></td>
<td>Sono presenti più indici di glifo rispetto ai punti di codice Unicode. Se non sono presenti mapping di glifi, il numero di indici di glifi deve essere minore o uguale al numero di punti di codice Unicode.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </dl></td>
<td>Si è verificato un errore grave e il contenuto di XPS OM potrebbe non essere ripristinabile. Alcuni componenti di XPS OM potrebbero ancora essere utilizzabili, ma sarà necessario verificarli prima di essere utilizzati ulteriormente. Poiché lo stato di XPS OM non può essere stimato dopo la restituzione di questo errore, tutti i componenti di XPS OM devono essere rilasciati e rimossi.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </dl></td>
<td>Un profilo colori era presente quando non ne era previsto uno. Un profilo colori è consentito solo quando il tipo di colore è <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </dl></td>
<td>La destinazione di una relazione non è il tipo previsto dal contesto della relazione. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </dl></td>
<td>Il tipo di relazione non è stato riconosciuto.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </dl></td>
<td>La raccolta di tipi di carattere con restrizioni contiene un tipo di carattere senza restrizioni.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </dl></td>
<td>Riservato.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </dl></td>
<td>Una geometria del percorso che non si trova in un dizionario risorse ha un attributo <strong>x:Key</strong> specificato. Le geometrie del percorso che non sono in un dizionario risorse non possono avere un attributo <strong>x:Key</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Alcuni metodi dell'API Document XPS effettuano chiamate all'API di creazione [pacchetti](/previous-versions/windows/desktop/opc/packaging) . Per informazioni sui valori restituiti dell'API di creazione pacchetti, vedere errori di creazione [pacchetti](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma solo per le applicazioni desktop di Windows Vista \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma solo per le \[ app desktop Windows server 2008\]<br/> |
| Intestazione<br/>                   | <dl> <dt>Xpsobjectmodel. h</dt> </dl>                                       |
| IDL<br/>                      | <dl> <dt>XpsObjectModel. idl</dt> </dl>                                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione degli errori in COM](../com/error-handling-in-com.md)
</dt> </dl>

 

