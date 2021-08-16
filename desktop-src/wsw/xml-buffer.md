---
title: XML Buffer
description: Un buffer XML fornisce un'archiviazione efficiente in memoria per dati XML arbitrari.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Servizi Web del buffer XML per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd4e4725f2ad3345dcef7c33b694a8e327f4d8a6c43fbce39f9c57babfa467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192337"
---
# <a name="xml-buffer"></a>XML Buffer

Un buffer XML fornisce un'archiviazione efficiente in memoria per dati XML arbitrari.


Per leggere i dati da un buffer XML, usare un [lettore XML e](xml-reader.md) chiamare [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) con il buffer XML. Il lettore verrà posizionato all'inizio del documento.

Per inserire dati in un buffer, usare un [writer XML e](xml-writer.md) chiamare [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) con il buffer XML. Il writer verrà posizionato alla fine del documento.

Dopo che un lettore è stato impostato su un buffer XML, oltre a tutte le API di lettura XML, È possibile usare [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) per spostarsi all'interno del documento. [**È anche possibile usare WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) e [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) per registrare una posizione nel documento e tornare a esso in un secondo momento.

Dopo che un writer è stato impostato su un buffer XML, oltre a tutte le API del writer XML, È possibile usare [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) per spostarsi all'interno del documento. [**È anche possibile usare WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) per registrare una posizione nel documento e tornare a esso in un secondo momento. Il writer inserisce sempre i dati prima del nodo in cui sono posizionati.

I nodi possono essere eliminati dal buffer XML ottenendo la posizione del nodo usando [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) o [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e quindi chiamando [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) con tale posizione. Per gli elementi, questo eliminerà l'elemento, tutti i relativi elementi figlio, incluso l'elemento finale corrispondente.

Una posizione è rappresentata dal valore [**WS \_ XML NODE \_ \_ POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). Le posizioni sono specifiche di un particolare buffer XML e sono valide solo se il buffer XML è valido.

Con i buffer XML vengono usate le enumerazioni seguenti:

-   [**WS \_ MOVE \_ TO**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**ID PROPRIETÀ BUFFER XML WS \_ \_ \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Con i buffer XML vengono usate le funzioni seguenti:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

Con i buffer XML viene usato l'handle seguente:

-   [WS \_ XML \_ BUFFER](ws-xml-buffer.md)

Con i buffer XML vengono usate le strutture seguenti:

-   [**PROPRIETÀ \_ DEL BUFFER XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**POSIZIONE \_ DEL NODO XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




