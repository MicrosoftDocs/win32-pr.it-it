---
title: XML Writer
description: Il writer XML è un'API per la emissione di XML. Un writer XML scrive un nodo XML alla volta, ma sono disponibili API helper aggiuntive per semplificare la scrittura di una sequenza di nodi.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Servizi Web writer XML per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75b7937ac6d8f6e9daff40289dd34729eaf235f203a02b91b5d1af3632049b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026059"
---
# <a name="xml-writer"></a>XML Writer

Il writer XML è un'API per la emissione di XML. Un writer XML scrive un nodo [XML](xml-node.md) alla volta, ma sono disponibili API helper aggiuntive per semplificare la scrittura di una sequenza di nodi.


Sono supportati i tipi di output del writer seguenti:

-   [**Buffer in memoria di byte codificati**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Un flusso**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Buffer [XML](xml-buffer.md)

Con il writer XML vengono utilizzati i callback seguenti:

-   [**CALLBACK DINAMICO \_ \_ DELLE STRINGHE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**CALLBACK DI WS \_ PULL \_ BYTES \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**CALLBACK DI WS \_ PUSH \_ BYTES \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**CALLBACK DI SCRITTURA WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Con il writer XML vengono utilizzate le enumerazioni seguenti:

-   [**WS \_ CHARSET**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**TIPO DI \_ CODIFICA WS XML \_ \_ \_ WRITER**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**TIPO DI \_ OUTPUT WS XML \_ \_ \_ WRITER**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**ID PROPRIETÀ WRITER XML WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

Con il writer XML vengono utilizzate le funzioni seguenti:

-   [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**WsCreateWriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**WsFreeWriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**WsGetPrefixFromNamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**WsGetWriterProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**WsPullBytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**WsPushBytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**WsSetOutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**WsWriteArray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**WsWriteBytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**WsWriteChars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**WsWriteEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**WsWriteEndCData**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**WsWriteEndElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**WsWriteQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**WsWriteStartCData**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**WsWriteStartElement**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**WsWriteText**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**WsWriteValue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**WsWriteXmlnsAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

Con il writer XML viene utilizzato l'handle seguente:

-   [WS \_ XML \_ WRITER](ws-xml-writer.md)

Con il writer XML vengono utilizzate le strutture seguenti:

-   [**CODIFICA \_ BINARIA WS XML \_ \_ \_ WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**OUTPUT DEL \_ BUFFER DEL \_ \_ WRITER XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**CODIFICA WS \_ XML \_ \_ WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**CODIFICA \_ MTOM WS XML \_ \_ \_ WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**OUTPUT DEL WRITER XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**PROPRIETÀ DEL WRITER XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**PROPRIETÀ WS \_ XML \_ \_ WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**OUTPUT DEL \_ FLUSSO DEL WRITER XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**CODIFICA DEL \_ TESTO WS XML \_ \_ \_ WRITER**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




