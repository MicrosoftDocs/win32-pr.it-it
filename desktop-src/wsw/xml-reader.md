---
title: Lettore XML
description: Il lettore XML è un cursore su un'origine di input di XML. Al suo nucleo, un lettore XML legge un nodo XML alla volta, ma sono disponibili API helper aggiuntive per semplificare la lettura di una sequenza di nodi.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Servizi Web Reader XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474657"
---
# <a name="xml-reader"></a>Lettore XML

Il lettore XML è un cursore su un'origine di input di XML. Al suo nucleo, un lettore XML legge un [nodo XML](xml-node.md) alla volta, ma sono disponibili API helper aggiuntive per semplificare la lettura di una sequenza di nodi.


Sono supportati i tipi di input Reader seguenti:

-   [**Un buffer in memoria di byte codificati**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Un flusso**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Un [buffer XML](xml-buffer.md)

### <a name="security"></a>Sicurezza

Il lettore verificherà che gli attributi presenti in un elemento siano univoci. Il tempo necessario per eseguire questa convalida è una funzione del numero di attributi sull'elemento che può essere pari a quello degli [**\_ \_ \_ \_ \_ attributi max della proprietà Reader di WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Di conseguenza, l'elaborazione di documenti di grandi dimensioni quando la **\_ \_ \_ proprietà \_ Max \_ del lettore XML WS** è impostata su un valore elevato può presentare un'opportunità di attacco Denial of Service.

Il lettore eseguirà il mapping dei prefissi agli spazi dei nomi per ogni elemento e attributo. Il tempo necessario per eseguire questo mapping è una funzione del numero di attributi xmlns nell'ambito, che può avere dimensioni pari alla [**\_ \_ \_ proprietà \_ Max \_ del lettore XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Pertanto, l'elaborazione di documenti di grandi dimensioni quando questa proprietà è impostata su un valore elevato può presentare un'opportunità per un attacco Denial of Service.

Sebbene il lettore garantisca che il documento segua la specifica grammaticale del codice XML e che i relativi aspetti siano all'interno delle quote specificate, il contenuto del documento deve essere considerato non attendibile quando provengono da un'origine non attendibile. Gli utenti del lettore dovrebbero controllare tutti i nomi di elementi e attributi e gli spazi dei nomi usando [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)o ispezionando manualmente i [**nodi**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).

Di seguito sono riportate alcune altre situazioni da considerare:

-   È possibile che gli elementi previsti siano mancanti
-   È possibile che vengano visualizzati elementi imprevisti
-   È possibile che gli attributi previsti siano mancanti
-   È possibile che vengano visualizzati attributi imprevisti
-   Gli elementi possono apparire come elementi vuoti
-   Gli spazi vuoti possono essere visualizzati in posizioni non previste

Gli utenti del lettore non devono allocare memoria basata semplicemente sui valori letti dal documento. Si consideri, ad esempio, il documento XML seguente:

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

L'allocazione di una matrice basata esclusivamente sul presupposto che un certo numero di elementi seguirebbe un potenziale vettore di attacco. In questo caso, l'utente del lettore deve allocare in modo incrementale la memoria mentre gli elementi vengono visualizzati.

Il lettore XML non supporta la definizione DTD. Non è necessario che l'utente del lettore si occupi della verifica della DTD.

Il callback seguente viene utilizzato con i reader XML:

-   [**\_callback di lettura WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Con i reader XML vengono utilizzate le enumerazioni seguenti:

-   [**\_tipo di \_ codifica del lettore XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_tipo di \_ input del lettore XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**\_ \_ \_ ID proprietà lettore XML \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Con i reader XML vengono utilizzate le funzioni seguenti:

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

Con i reader XML viene utilizzato l'handle seguente:

-   [\_lettore XML \_ WS](ws-xml-reader.md)

Con i reader XML vengono utilizzate le strutture seguenti:

-   [**\_ \_ \_ codifica binaria del lettore XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**\_ \_ input buffer del lettore XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**\_codifica del \_ lettore \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**\_ \_ input lettore XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**\_ \_ codifica MTOM del lettore XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**\_proprietà del \_ lettore \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**\_proprietà del \_ lettore \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**\_ \_ input flusso del lettore XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**\_codifica del \_ testo del lettore XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




