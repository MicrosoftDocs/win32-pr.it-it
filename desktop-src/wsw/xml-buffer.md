---
title: Buffer XML
description: Un buffer XML fornisce un efficiente archivio in memoria per i dati XML arbitrari.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Servizi Web del buffer XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963575"
---
# <a name="xml-buffer"></a>Buffer XML

Un buffer XML fornisce un efficiente archivio in memoria per i dati XML arbitrari.


Per leggere i dati da un buffer XML, usare un [lettore XML](xml-reader.md) e chiamare [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) con il buffer XML. Il lettore verrà posizionato all'inizio del documento.

Per inserire i dati in un buffer, utilizzare un [writer XML](xml-writer.md) e chiamare [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) con il buffer XML. Il writer verrà posizionato alla fine del documento.

Una volta impostato un reader su un buffer XML, oltre a tutte le API del lettore XML, è possibile utilizzare [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) per spostarsi nel lettore attraverso il documento. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) e [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) possono essere usati anche per registrare una posizione nel documento e tornare in seguito.

Una volta che un writer è stato impostato su un buffer XML, oltre a tutte le API del writer XML, è possibile utilizzare [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) per spostarsi nel writer tramite il documento. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) possono essere usati anche per registrare una posizione nel documento e tornare in seguito. Il writer inserisce sempre i dati prima del nodo su cui è posizionato.

I nodi possono essere eliminati dal buffer XML ottenendo la posizione del nodo usando [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) o [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e quindi chiamando [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) con tale posizione. Per gli elementi, questo eliminerà l'elemento, tutti i relativi elementi figlio, incluso il corrispondente elemento End.

Una posizione è rappresentata dal valore [**della \_ \_ \_ posizione del nodo WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). Le posizioni sono specifiche di un determinato buffer XML e sono valide solo finché il buffer XML è valido.

Con i buffer XML vengono utilizzate le enumerazioni seguenti:

-   [**WS \_ \_ -Sposta in**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**\_ID della \_ proprietà del buffer WS XML \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Con i buffer XML vengono utilizzate le funzioni seguenti:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

Con i buffer XML viene utilizzato l'handle seguente:

-   [\_buffer WS XML \_](ws-xml-buffer.md)

Con i buffer XML vengono utilizzate le strutture seguenti:

-   [**\_ \_ Proprietà buffer WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**\_posizione del \_ nodo WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




