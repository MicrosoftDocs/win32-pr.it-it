---
title: Lettore XML
description: Lettore XML è un cursore su un'origine di input xml. Alla base, un lettore XML legge un nodo XML alla volta, ma sono disponibili API helper aggiuntive per semplificare la lettura di una sequenza di nodi.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Servizi Web di lettura XML per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a03ef961cd49c481564b6bad1ad86603c9cb576f0c8aeda1a7cd2d6d18aaeef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770871"
---
# <a name="xml-reader"></a>Lettore XML

Lettore XML è un cursore su un'origine di input xml. Alla base, un lettore XML legge un nodo [XML](xml-node.md) alla volta, ma sono disponibili API helper aggiuntive per semplificare la lettura di una sequenza di nodi.


Sono supportati i tipi di input dei lettori seguenti:

-   [**Buffer in memoria di byte codificati**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Flusso**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Buffer [XML](xml-buffer.md)

### <a name="security"></a>Sicurezza

Il lettore verificherà che gli attributi presenti in un elemento siano univoci. Il tempo necessario per eseguire questa convalida è una funzione del numero di attributi nell'elemento che può essere grande quanto [**WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Pertanto, l'elaborazione di documenti di grandi dimensioni quando **WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ ATTRIBUTES** è impostato su un valore elevato può presentare un'opportunità per un attacco Denial of Service.

Il lettore esegue il mapping dei prefissi agli spazi dei nomi per ogni elemento e attributo. Il tempo necessario per eseguire questo mapping è una funzione del numero di attributi xmlns nell'ambito che possono essere grandi quanto [**WS \_ XML READER PROPERTY MAX \_ \_ \_ \_ NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Pertanto, l'elaborazione di documenti di grandi dimensioni quando questa proprietà è impostata su un valore elevato può presentare un'opportunità per un attacco Denial of Service.

Anche se il lettore garantisce che il documento segua la specifica grammaticale di xml e che i relativi aspetti siano entro le quote specificate, il contenuto del documento deve comunque essere considerato non attendibile quando proviene da un'origine non attendibile. Gli utenti del lettore devono controllare tutti i nomi di elementi e attributi e gli spazi dei nomi [**usando WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)o controllando manualmente [**i nodi**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).

Alcune altre situazioni da considerare includono, ma non sono limitate a:

-   Gli elementi previsti potrebbero non essere presenti
-   Potrebbero essere visualizzati elementi imprevisti
-   Gli attributi previsti potrebbero non essere presenti
-   Potrebbero essere visualizzati attributi imprevisti
-   Gli elementi possono essere visualizzati come elementi vuoti
-   È possibile che gli spazi vuoti vengano visualizzati in posizioni impreviste

Gli utenti del lettore non devono allocare memoria in base ai valori letti dal documento. Si consideri ad esempio il documento XML seguente:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

L'allocazione di una matrice basata esclusivamente sul presupposto che un certo numero di elementi seguirà sarebbe un potenziale vettore di attacco. L'utente del lettore in questo caso deve invece allocare in modo incrementale la memoria quando vengono visualizzati gli elementi.

Il lettore XML non supporta la DTD. L'utente del lettore non deve riguardare la verifica DTD.

Con i lettori XML viene usato il callback seguente:

-   [**CALLBACK \_ DI LETTURA WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Con i lettori XML vengono usate le enumerazioni seguenti:

-   [**TIPO DI \_ CODIFICA LETTORE XML \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**TIPO DI \_ \_ INPUT LETTORE XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**ID PROPRIETÀ \_ LETTORE XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Con i lettori XML vengono usate le funzioni seguenti:

-   [**WsCreateReader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**WsFreeReader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**WsGetNamespaceFromPrefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**WsGetReaderNode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**WsGetReaderProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**WsReadArray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**WsReadBytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**WsReadChars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**WsReadEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**WsReadQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**WsReadStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**WsSetInput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**WsSkipNode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

Con i lettori XML viene usato l'handle seguente:

-   [LETTORE \_ XML WS \_](ws-xml-reader.md)

Con i lettori XML vengono usate le strutture seguenti:

-   [**CODIFICA \_ BINARIA LETTORE XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**INPUT DEL \_ BUFFER DEL \_ \_ LETTORE XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**CODIFICA DEL \_ \_ LETTORE XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**INPUT \_ LETTORE XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**CODIFICA \_ MTOM DEL LETTORE XML \_ \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**PROPRIETÀ \_ LETTORE XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**PROPRIETÀ \_ LETTORE XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**INPUT DEL \_ FLUSSO DEL \_ LETTORE XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**CODIFICA DEL \_ TESTO DEL \_ LETTORE XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




