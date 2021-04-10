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
# <a name="xml-buffer"></a><span data-ttu-id="27ae4-106">Buffer XML</span><span class="sxs-lookup"><span data-stu-id="27ae4-106">XML Buffer</span></span>

<span data-ttu-id="27ae4-107">Un buffer XML fornisce un efficiente archivio in memoria per i dati XML arbitrari.</span><span class="sxs-lookup"><span data-stu-id="27ae4-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="27ae4-108">Per leggere i dati da un buffer XML, usare un [lettore XML](xml-reader.md) e chiamare [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) con il buffer XML.</span><span class="sxs-lookup"><span data-stu-id="27ae4-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="27ae4-109">Il lettore verrà posizionato all'inizio del documento.</span><span class="sxs-lookup"><span data-stu-id="27ae4-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="27ae4-110">Per inserire i dati in un buffer, utilizzare un [writer XML](xml-writer.md) e chiamare [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) con il buffer XML.</span><span class="sxs-lookup"><span data-stu-id="27ae4-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="27ae4-111">Il writer verrà posizionato alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="27ae4-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="27ae4-112">Una volta impostato un reader su un buffer XML, oltre a tutte le API del lettore XML, è possibile utilizzare [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) per spostarsi nel lettore attraverso il documento.</span><span class="sxs-lookup"><span data-stu-id="27ae4-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="27ae4-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) e [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) possono essere usati anche per registrare una posizione nel documento e tornare in seguito.</span><span class="sxs-lookup"><span data-stu-id="27ae4-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="27ae4-114">Una volta che un writer è stato impostato su un buffer XML, oltre a tutte le API del writer XML, è possibile utilizzare [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) per spostarsi nel writer tramite il documento.</span><span class="sxs-lookup"><span data-stu-id="27ae4-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="27ae4-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) possono essere usati anche per registrare una posizione nel documento e tornare in seguito.</span><span class="sxs-lookup"><span data-stu-id="27ae4-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="27ae4-116">Il writer inserisce sempre i dati prima del nodo su cui è posizionato.</span><span class="sxs-lookup"><span data-stu-id="27ae4-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="27ae4-117">I nodi possono essere eliminati dal buffer XML ottenendo la posizione del nodo usando [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) o [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e quindi chiamando [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) con tale posizione.</span><span class="sxs-lookup"><span data-stu-id="27ae4-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="27ae4-118">Per gli elementi, questo eliminerà l'elemento, tutti i relativi elementi figlio, incluso il corrispondente elemento End.</span><span class="sxs-lookup"><span data-stu-id="27ae4-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="27ae4-119">Una posizione è rappresentata dal valore [**della \_ \_ \_ posizione del nodo WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span><span class="sxs-lookup"><span data-stu-id="27ae4-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="27ae4-120">Le posizioni sono specifiche di un determinato buffer XML e sono valide solo finché il buffer XML è valido.</span><span class="sxs-lookup"><span data-stu-id="27ae4-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="27ae4-121">Con i buffer XML vengono utilizzate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="27ae4-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="27ae4-122">**WS \_ \_ -Sposta in**</span><span class="sxs-lookup"><span data-stu-id="27ae4-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="27ae4-123">**\_ID della \_ proprietà del buffer WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="27ae4-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="27ae4-124">Con i buffer XML vengono utilizzate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="27ae4-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="27ae4-125">**WsCreateXmlBuffer**</span><span class="sxs-lookup"><span data-stu-id="27ae4-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="27ae4-126">**WsRemoveNode**</span><span class="sxs-lookup"><span data-stu-id="27ae4-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="27ae4-127">Con i buffer XML viene utilizzato l'handle seguente:</span><span class="sxs-lookup"><span data-stu-id="27ae4-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="27ae4-128">\_buffer WS XML \_</span><span class="sxs-lookup"><span data-stu-id="27ae4-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="27ae4-129">Con i buffer XML vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="27ae4-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="27ae4-130">**\_ \_ Proprietà buffer WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="27ae4-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="27ae4-131">**\_posizione del \_ nodo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="27ae4-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




