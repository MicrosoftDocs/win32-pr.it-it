---
title: Writer XML
description: Il writer XML è un'API per la creazione di codice XML. Al suo nucleo, un writer XML scrive un nodo XML alla volta, ma sono disponibili API helper aggiuntive per semplificare la scrittura di una sequenza di nodi.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Servizi Web writer XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300691"
---
# <a name="xml-writer"></a>Writer XML

Il writer XML è un'API per la creazione di codice XML. Al suo nucleo, un writer XML scrive un [nodo XML](xml-node.md) alla volta, ma sono disponibili API helper aggiuntive per semplificare la scrittura di una sequenza di nodi.


Sono supportati i tipi di output del writer seguenti:

-   [**Un buffer in memoria di byte codificati**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Un flusso**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Un [buffer XML](xml-buffer.md)

Con il writer XML vengono utilizzati i callback seguenti:

-   [**\_ \_ callback stringa dinamica \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**CALLBACK di WS \_ pull \_ byte \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**CALLBACK di WS \_ push \_ bytes \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_callback WS Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Con il writer XML vengono utilizzate le enumerazioni seguenti:

-   [**\_set di caratteri WS**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**\_tipo di codifica WS XML \_ writer \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**\_tipo di \_ output del writer XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**\_ID della \_ proprietà del writer XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

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

Il seguente handle viene utilizzato con il writer XML:

-   [\_writer XML \_ WS](ws-xml-writer.md)

Con il writer XML vengono utilizzate le strutture seguenti:

-   [**\_ \_ \_ codifica binaria WS writer XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**\_ \_ output buffer del writer XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**\_codifica WS XML \_ writer \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**\_ \_ codifica MTOM del writer XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**\_output del \_ writer \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**\_proprietà del \_ writer \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**WS \_ - \_ writer XML ( \_ proprietà)**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**\_output del \_ flusso del writer XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**\_ \_ \_ codifica testo WS XML \_ writer**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




