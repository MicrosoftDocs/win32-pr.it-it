---
title: Panoramica sul livello del canale
description: Il livello del canale fornisce un'astrazione del canale di trasporto e dei messaggi inviati sul canale.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Panoramica dei servizi Web di livello canale per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104569664"
---
# <a name="channel-layer-overview"></a><span data-ttu-id="53f9e-106">Panoramica sul livello del canale</span><span class="sxs-lookup"><span data-stu-id="53f9e-106">Channel Layer Overview</span></span>

<span data-ttu-id="53f9e-107">Il livello del canale fornisce un'astrazione del canale di trasporto e dei messaggi inviati sul canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="53f9e-108">Include anche funzioni per la serializzazione dei tipi di dati C da e verso strutture SOAP.</span><span class="sxs-lookup"><span data-stu-id="53f9e-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="53f9e-109">Il livello del canale consente il controllo completo delle comunicazioni per mezzo di [messaggi](message.md) costituiti da dati inviati o ricevuti e contenenti corpi e intestazioni e [canali](channel.md) che astraggono i protocolli di scambio dei messaggi e forniscono proprietà per la personalizzazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="53f9e-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="53f9e-110">Message</span><span class="sxs-lookup"><span data-stu-id="53f9e-110">Message</span></span>

<span data-ttu-id="53f9e-111">Un [messaggio](message.md) è un oggetto che incapsula i dati di rete, in particolare i dati trasmessi o ricevuti in rete.</span><span class="sxs-lookup"><span data-stu-id="53f9e-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="53f9e-112">La struttura del messaggio è definita da SOAP, con un set discreto di intestazioni e un corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="53f9e-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="53f9e-113">Le intestazioni vengono inserite in un buffer di memoria e il corpo del messaggio viene letto o scritto usando un'API di flusso.</span><span class="sxs-lookup"><span data-stu-id="53f9e-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![Diagramma che mostra l'intestazione e il corpo di un messaggio.](images/messageenvelope.png)

<span data-ttu-id="53f9e-115">Sebbene il modello di dati di un messaggio sia sempre il modello di dati XML, il formato wire effettivo è flessibile.</span><span class="sxs-lookup"><span data-stu-id="53f9e-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="53f9e-116">Prima che un messaggio venga trasmesso, viene codificato utilizzando una particolare codifica, ad esempio text, Binary o MTOM.</span><span class="sxs-lookup"><span data-stu-id="53f9e-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="53f9e-117">Per ulteriori informazioni sulle codifiche, vedere la pagina relativa alla [**\_ codifica WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .</span><span class="sxs-lookup"><span data-stu-id="53f9e-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![Diagramma che mostra diversi formati di codifica messaggi.](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="53f9e-119">Channel</span><span class="sxs-lookup"><span data-stu-id="53f9e-119">Channel</span></span>

<span data-ttu-id="53f9e-120">Un [canale](channel.md) è un oggetto utilizzato per inviare e ricevere messaggi in una rete tra due o più endpoint.</span><span class="sxs-lookup"><span data-stu-id="53f9e-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="53f9e-121">Ai canali sono associati dati che descrivono come [indirizzare](endpoint-address.md) il messaggio quando viene inviato.</span><span class="sxs-lookup"><span data-stu-id="53f9e-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="53f9e-122">L'invio di un messaggio su un canale è analogo al posizionamento in uno scivolo: il canale include le informazioni in cui il messaggio deve essere inserito e come ottenerlo.</span><span class="sxs-lookup"><span data-stu-id="53f9e-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![Diagramma che mostra i canali per i messaggi.](images/channelsaschute.png)

<span data-ttu-id="53f9e-124">I canali sono suddivisi in categorie in [**tipi di canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="53f9e-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="53f9e-125">Un tipo di canale specifica la direzione in cui i messaggi possono essere propagati.</span><span class="sxs-lookup"><span data-stu-id="53f9e-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="53f9e-126">Il tipo di canale indica inoltre se il canale è con sessione o con sessione.</span><span class="sxs-lookup"><span data-stu-id="53f9e-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="53f9e-127">Una sessione viene definita come metodo astratto per la correlazione dei messaggi tra due o più entità.</span><span class="sxs-lookup"><span data-stu-id="53f9e-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="53f9e-128">Un esempio di canale con sessione è un canale TCP, che usa la connessione TCP come implementazione della sessione concreta.</span><span class="sxs-lookup"><span data-stu-id="53f9e-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="53f9e-129">Un esempio di canale senza sessione è UDP, che non dispone di un meccanismo di sessione sottostante.</span><span class="sxs-lookup"><span data-stu-id="53f9e-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="53f9e-130">Sebbene HTTP disponga di connessioni TCP sottostanti, questo fatto non viene esposto direttamente tramite questa API e pertanto HTTP viene considerato anche un canale senza sessione.</span><span class="sxs-lookup"><span data-stu-id="53f9e-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![Diagramma che mostra i tipi di canale con sessione e con sessione.](images/channeltypes.png)

<span data-ttu-id="53f9e-132">Sebbene i tipi di canale descrivano la direzione e le informazioni sulla sessione per un canale, non specificano come viene implementato il canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="53f9e-133">Quale protocollo deve essere utilizzato dal canale?</span><span class="sxs-lookup"><span data-stu-id="53f9e-133">What protocol should the channel use?</span></span> <span data-ttu-id="53f9e-134">Quanto è difficile il canale per tentare di recapitare il messaggio?</span><span class="sxs-lookup"><span data-stu-id="53f9e-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="53f9e-135">Quale tipo di sicurezza viene utilizzato?</span><span class="sxs-lookup"><span data-stu-id="53f9e-135">What kind of security is used?</span></span> <span data-ttu-id="53f9e-136">Singlecast o multicast?</span><span class="sxs-lookup"><span data-stu-id="53f9e-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="53f9e-137">Queste impostazioni sono denominate "binding" del canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="53f9e-138">L'associazione è costituita dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f9e-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="53f9e-139">[**Binding di \_ canale \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)che identifica il protocollo di trasferimento da utilizzare (TCP, UDP, http, NAMEDPIPE).</span><span class="sxs-lookup"><span data-stu-id="53f9e-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="53f9e-140">[**Descrizione della \_ sicurezza \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), che specifica come proteggere il canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="53f9e-141">Set [**WS \_ Channel \_ Property**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, che specificano impostazioni facoltative aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="53f9e-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="53f9e-142">Per l'elenco delle proprietà, vedere [**\_ \_ \_ ID proprietà WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .</span><span class="sxs-lookup"><span data-stu-id="53f9e-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![Diagramma che mostra un elenco di proprietà del canale.](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="53f9e-144">Listener</span><span class="sxs-lookup"><span data-stu-id="53f9e-144">Listener</span></span>

<span data-ttu-id="53f9e-145">Per iniziare a comunicare, il client crea un oggetto canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="53f9e-146">Ma in che modo il servizio ottiene il relativo oggetto canale?</span><span class="sxs-lookup"><span data-stu-id="53f9e-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="53f9e-147">Questa operazione viene eseguita tramite la creazione di un [listener](listener.md).</span><span class="sxs-lookup"><span data-stu-id="53f9e-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="53f9e-148">La creazione di un listener richiede le stesse informazioni di binding necessarie per creare un canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="53f9e-149">Una volta creato un listener, l'applicazione può accettare canali dal listener.</span><span class="sxs-lookup"><span data-stu-id="53f9e-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="53f9e-150">Poiché l'applicazione può rimanere indietro nell'accettare i canali, i listener in genere mantengono una coda di canali pronti per l'accettazione (fino a una quota).</span><span class="sxs-lookup"><span data-stu-id="53f9e-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![Diagramma che mostra i canali nella coda dei listener.](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="53f9e-152">Avvio della comunicazione (client)</span><span class="sxs-lookup"><span data-stu-id="53f9e-152">Initiating Communication (client)</span></span>

<span data-ttu-id="53f9e-153">Per avviare la comunicazione nel client, usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-153">To initiate communication on the client, use the following sequence.</span></span>

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a><span data-ttu-id="53f9e-154">Accettazione della comunicazione (Server)</span><span class="sxs-lookup"><span data-stu-id="53f9e-154">Accepting Communication (server)</span></span>

<span data-ttu-id="53f9e-155">Per accettare le comunicazioni in ingresso nel server, usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-155">To accept incoming communications on the server, use the following sequence.</span></span>

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="53f9e-156">Invio di messaggi (client o server)</span><span class="sxs-lookup"><span data-stu-id="53f9e-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="53f9e-157">Per inviare messaggi, utilizzare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="53f9e-158">La funzione [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) non consente lo streaming e presuppone che il corpo contenga un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="53f9e-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="53f9e-159">Per evitare questi vincoli, usare la sequenza seguente anziché **WsSendMessage**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

<span data-ttu-id="53f9e-160">La funzione [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa la serializzazione per scrivere gli elementi del corpo.</span><span class="sxs-lookup"><span data-stu-id="53f9e-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="53f9e-161">Per scrivere i dati direttamente nel writer XML, usare la sequenza seguente anziché **WsWriteBody**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="53f9e-162">La funzione [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) utilizza la serializzazione per impostare le intestazioni sul buffer dell'intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="53f9e-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="53f9e-163">Per utilizzare il writer XML per scrivere un'intestazione, utilizzare la sequenza seguente anziché **WsAddCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="53f9e-164">Ricezione di messaggi (client o server)</span><span class="sxs-lookup"><span data-stu-id="53f9e-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="53f9e-165">Per ricevere i messaggi, usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-165">To receive messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

<span data-ttu-id="53f9e-166">La funzione [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) non consente lo streaming e presuppone che il corpo contenga un solo elemento e che il tipo del messaggio (azione e schema del corpo) sia noto in primo piano.</span><span class="sxs-lookup"><span data-stu-id="53f9e-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="53f9e-167">Per evitare questi vincoli, usare la sequenza seguente anziché **WsReceiveMessage**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

<span data-ttu-id="53f9e-168">La funzione [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa la serializzazione per leggere gli elementi del corpo.</span><span class="sxs-lookup"><span data-stu-id="53f9e-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="53f9e-169">Per leggere i dati direttamente dal [lettore XML](xml-reader.md), usare la sequenza seguente anziché **WsReadBody**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="53f9e-170">Le funzioni [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) utilizzano la serializzazione per ottenere le intestazioni dal buffer dell'intestazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="53f9e-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="53f9e-171">Per utilizzare il [lettore XML](xml-reader.md) per leggere un'intestazione, utilizzare la sequenza seguente anziché **WsGetCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a><span data-ttu-id="53f9e-172">Risposta richiesta (client)</span><span class="sxs-lookup"><span data-stu-id="53f9e-172">Request Reply (client)</span></span>

<span data-ttu-id="53f9e-173">L'esecuzione di una richiesta-risposta sul client può essere eseguita con la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

<span data-ttu-id="53f9e-174">La funzione [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) presuppone un singolo elemento per il corpo dei messaggi di richiesta e risposta e che il tipo del messaggio (azione e schema del corpo) sia noto come front.</span><span class="sxs-lookup"><span data-stu-id="53f9e-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="53f9e-175">Per evitare queste limitazioni, è possibile inviare manualmente il messaggio di richiesta e di risposta, come illustrato nella sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="53f9e-176">Questa sequenza corrisponde alla sequenza precedente per l'invio e la ricezione di un messaggio, eccetto laddove specificato.</span><span class="sxs-lookup"><span data-stu-id="53f9e-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a><span data-ttu-id="53f9e-177">Risposta richiesta (Server)</span><span class="sxs-lookup"><span data-stu-id="53f9e-177">Request Reply (server)</span></span>

<span data-ttu-id="53f9e-178">Per ricevere un messaggio di richiesta sul server, utilizzare la stessa sequenza descritta nella sezione precedente relativa alla ricezione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="53f9e-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="53f9e-179">Per inviare un messaggio di risposta o di errore, usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="53f9e-180">La funzione [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) presuppone un singolo elemento nel corpo e non consente lo streaming.</span><span class="sxs-lookup"><span data-stu-id="53f9e-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="53f9e-181">Per evitare queste limitazioni, usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="53f9e-182">Corrisponde alla sequenza precedente per l'invio di un messaggio, ma utilizza il [**messaggio WS \_ Reply \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) anziché il **messaggio WS \_ blank \_** durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="53f9e-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a><span data-ttu-id="53f9e-183">Modelli di scambio dei messaggi</span><span class="sxs-lookup"><span data-stu-id="53f9e-183">Message Exchange Patterns</span></span>

<span data-ttu-id="53f9e-184">Il [**\_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) impone il modello di scambio dei messaggi possibile per un canale specifico.</span><span class="sxs-lookup"><span data-stu-id="53f9e-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="53f9e-185">Il tipo supportato varia in base all'associazione, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="53f9e-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="53f9e-186">[**WS \_ L' \_ \_ associazione di canale http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta la [**\_ \_ \_ richiesta WS Channel Type**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) nel client e la **risposta del \_ \_ tipo \_ di canale WS** sul server.</span><span class="sxs-lookup"><span data-stu-id="53f9e-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="53f9e-187">[**WS \_ L' \_ \_ associazione di canale TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta la [**\_ \_ \_ \_ sessione duplex WS del tipo**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) di canale nel client e la **\_ \_ \_ \_ sessione duplex del tipo di canale WS** sul server.</span><span class="sxs-lookup"><span data-stu-id="53f9e-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="53f9e-188">[**WS \_ L' \_ \_ associazione di canale UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta il [**tipo di canale di WS \_ \_ \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) nel client e l'input del **\_ tipo di canale \_ \_ WS** sul server.</span><span class="sxs-lookup"><span data-stu-id="53f9e-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="53f9e-189">[**WS \_ L' \_ \_ associazione di canale NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta [**WS \_ Channel \_ Type \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) nell' **\_ \_ \_ input del tipo** di canale client e WS sul server.</span><span class="sxs-lookup"><span data-stu-id="53f9e-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="53f9e-190">Cicli di messaggi</span><span class="sxs-lookup"><span data-stu-id="53f9e-190">Message Loops</span></span>

<span data-ttu-id="53f9e-191">Per ogni modello di scambio di messaggi è disponibile un "ciclo" specifico che può essere usato per inviare o ricevere messaggi.</span><span class="sxs-lookup"><span data-stu-id="53f9e-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="53f9e-192">Il ciclo descrive l'ordine valido delle operazioni necessarie per l'invio e la ricezione di più messaggi.</span><span class="sxs-lookup"><span data-stu-id="53f9e-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="53f9e-193">I cicli vengono descritti sotto come produzioni di grammatica.</span><span class="sxs-lookup"><span data-stu-id="53f9e-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="53f9e-194">Il termine ' end ' è un oggetto Receive dove **WS \_ S \_ end** viene restituito (vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md)), che indica che nel canale non sono disponibili altri messaggi.</span><span class="sxs-lookup"><span data-stu-id="53f9e-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="53f9e-195">Nell'ambiente di produzione parallelo viene specificato che per Parallel (x & y) l'operazione x può essere eseguita contemporaneamente a y.</span><span class="sxs-lookup"><span data-stu-id="53f9e-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="53f9e-196">Nel client vengono usati i cicli seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f9e-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="53f9e-197">Nel server vengono usati i cicli seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f9e-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="53f9e-198">L'utilizzo [**dell' \_ \_ associazione di \_ \_ sicurezza del \_ messaggio del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sul server richiede una ricezione riuscita prima che sia consentito l'invio anche con un canale di tipo [**\_ \_ \_ \_ sessione duplex di tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="53f9e-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="53f9e-199">Dopo la prima ricezione.</span><span class="sxs-lookup"><span data-stu-id="53f9e-199">After the first receive.</span></span> <span data-ttu-id="53f9e-200">viene applicato il ciclo normale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-200">the regular loop applies.</span></span>

<span data-ttu-id="53f9e-201">Si noti che è possibile usare i canali di tipo [**WS \_ Channel \_ Type \_ Request**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) e **WS \_ Channel \_ Type \_ Reply** per inviare e ricevere messaggi unidirezionali (e il modello Request-Reply standard).</span><span class="sxs-lookup"><span data-stu-id="53f9e-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="53f9e-202">Questa operazione viene eseguita chiudendo il canale di risposta senza inviare una risposta.</span><span class="sxs-lookup"><span data-stu-id="53f9e-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="53f9e-203">In questo caso, non verrà ricevuta alcuna risposta sul canale di richiesta.</span><span class="sxs-lookup"><span data-stu-id="53f9e-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="53f9e-204">Il valore restituito di **WS \_ S \_ end** utilizzando [**l' \_ \_ associazione di \_ \_ sicurezza del \_ messaggio del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sul server richiede una ricezione riuscita prima che l'invio sia consentito anche con un canale di tipo **WS \_ Channel \_ Type \_ duplex \_ Session**.</span><span class="sxs-lookup"><span data-stu-id="53f9e-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="53f9e-205">Dopo la prima ricezione, viene applicato il ciclo normale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="53f9e-206">viene restituito, che indica che non è disponibile alcun messaggio.</span><span class="sxs-lookup"><span data-stu-id="53f9e-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="53f9e-207">I cicli client o server possono essere eseguiti in parallelo tra loro utilizzando più istanze del canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="53f9e-208">Filtro messaggi</span><span class="sxs-lookup"><span data-stu-id="53f9e-208">Message Filtering</span></span>

<span data-ttu-id="53f9e-209">Un canale server può filtrare i messaggi ricevuti che non sono destinati all'applicazione, ad esempio messaggi che stabiliscono un [contesto di sicurezza](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="53f9e-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="53f9e-210">In tal caso, **WS \_ S \_ end** verrà restituito da [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) e nessun messaggio dell'applicazione sarà disponibile sul canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="53f9e-211">Tuttavia, ciò non segnala che il client intende terminare la comunicazione con il server.</span><span class="sxs-lookup"><span data-stu-id="53f9e-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="53f9e-212">È possibile che siano disponibili altri messaggi su un altro canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-212">More messages may be available on another channel.</span></span> <span data-ttu-id="53f9e-213">Vedere [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span><span class="sxs-lookup"><span data-stu-id="53f9e-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="53f9e-214">Annullamento</span><span class="sxs-lookup"><span data-stu-id="53f9e-214">Cancellation</span></span>

<span data-ttu-id="53f9e-215">La funzione [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) viene usata per annullare i/o in sospeso per un canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="53f9e-216">Questa API non attende il completamento delle operazioni di i/o.</span><span class="sxs-lookup"><span data-stu-id="53f9e-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="53f9e-217">Per ulteriori informazioni, vedere il diagramma di stato del [**\_ canale \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) e la documentazione relativa a **WsAbortChannel** .</span><span class="sxs-lookup"><span data-stu-id="53f9e-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="53f9e-218">L'API [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) viene utilizzata per annullare i/o in sospeso per un listener.</span><span class="sxs-lookup"><span data-stu-id="53f9e-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="53f9e-219">Questa API non attende il completamento delle operazioni di i/o.</span><span class="sxs-lookup"><span data-stu-id="53f9e-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="53f9e-220">Se si interrompe un listener, verranno interrotte anche le accettazioni in sospeso.</span><span class="sxs-lookup"><span data-stu-id="53f9e-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="53f9e-221">Per ulteriori informazioni, vedere il diagramma di stato del [**\_ listener \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) e **WsAbortListener** .</span><span class="sxs-lookup"><span data-stu-id="53f9e-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="53f9e-222">TCP</span><span class="sxs-lookup"><span data-stu-id="53f9e-222">TCP</span></span>

<span data-ttu-id="53f9e-223">L' [**\_ associazione di \_ canale \_ WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su TCP.</span><span class="sxs-lookup"><span data-stu-id="53f9e-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="53f9e-224">La specifica SOAP su TCP si basa sul meccanismo di framing .NET.</span><span class="sxs-lookup"><span data-stu-id="53f9e-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="53f9e-225">La condivisione delle porte non è supportata in questa versione.</span><span class="sxs-lookup"><span data-stu-id="53f9e-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="53f9e-226">Ogni listener aperto deve usare un numero di porta diverso.</span><span class="sxs-lookup"><span data-stu-id="53f9e-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="53f9e-227">UDP</span><span class="sxs-lookup"><span data-stu-id="53f9e-227">UDP</span></span>

<span data-ttu-id="53f9e-228">L' [**\_ associazione di \_ canale \_ WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su UDP.</span><span class="sxs-lookup"><span data-stu-id="53f9e-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="53f9e-229">Il binding UDP presenta alcune limitazioni:</span><span class="sxs-lookup"><span data-stu-id="53f9e-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="53f9e-230">Non è disponibile alcun supporto per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="53f9e-230">There is no support for security.</span></span>
-   <span data-ttu-id="53f9e-231">I messaggi possono essere persi o duplicati.</span><span class="sxs-lookup"><span data-stu-id="53f9e-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="53f9e-232">È supportata una sola codifica: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span><span class="sxs-lookup"><span data-stu-id="53f9e-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="53f9e-233">I messaggi sono fondamentalmente limitati a 64K e spesso hanno una maggiore probabilità di essere persi se le dimensioni superano la MTU della rete.</span><span class="sxs-lookup"><span data-stu-id="53f9e-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="53f9e-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="53f9e-234">HTTP</span></span>

<span data-ttu-id="53f9e-235">L' [**\_ associazione di \_ canale \_ WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su http.</span><span class="sxs-lookup"><span data-stu-id="53f9e-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="53f9e-236">Per controllare le intestazioni specifiche HTTP nel client e nel server, vedere [**WS \_ http \_ message \_ mapping**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span><span class="sxs-lookup"><span data-stu-id="53f9e-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="53f9e-237">Per inviare e ricevere messaggi non SOAP sul server, utilizzare la [**codifica WS \_ \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) per la [**\_ codifica della \_ proprietà \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="53f9e-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="53f9e-238">NAMEDPIPES</span><span class="sxs-lookup"><span data-stu-id="53f9e-238">NAMEDPIPES</span></span>

<span data-ttu-id="53f9e-239">L' [**\_ associazione di \_ canale \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su named pipe, consentendo la comunicazione con il servizio Windows Communication Foundation (WCF) utilizzando NetNamedPipeBinding.</span><span class="sxs-lookup"><span data-stu-id="53f9e-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="53f9e-240">Correlazione dei messaggi di richiesta/risposta</span><span class="sxs-lookup"><span data-stu-id="53f9e-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="53f9e-241">I messaggi di richiesta/risposta sono correlati in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f9e-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="53f9e-242">La correlazione viene eseguita utilizzando il canale come meccanismo di correlazione.</span><span class="sxs-lookup"><span data-stu-id="53f9e-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="53f9e-243">Ad esempio, quando si usa il [**trasporto della versione di WS \_ Addressing \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e il [**\_ \_ \_ binding del canale WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , la risposta per il messaggio di richiesta è correlata alla richiesta dal fatto che è il corpo dell'entità della risposta http.</span><span class="sxs-lookup"><span data-stu-id="53f9e-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="53f9e-244">La correlazione viene eseguita utilizzando le intestazioni MessageID e repiù recenti.</span><span class="sxs-lookup"><span data-stu-id="53f9e-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="53f9e-245">Questo meccanismo viene utilizzato con [**WS \_ Addressing \_ versione \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e **WS \_ Addressing \_ versione \_ 0 \_ 9** (anche quando si utilizza l' [**\_ associazione di \_ canale \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span><span class="sxs-lookup"><span data-stu-id="53f9e-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="53f9e-246">In questo caso, il messaggio di richiesta include l'intestazione MessageID.</span><span class="sxs-lookup"><span data-stu-id="53f9e-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="53f9e-247">Il messaggio di risposta include un'intestazione reultimissimo con il valore dell'intestazione MessageID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="53f9e-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="53f9e-248">L'intestazione reultimissime consente al client di correlare una risposta a una richiesta inviata.</span><span class="sxs-lookup"><span data-stu-id="53f9e-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="53f9e-249">Le API di livello del canale seguenti usano automaticamente i meccanismi di correlazione appropriati basati sulla [**\_ \_ versione WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) del canale.</span><span class="sxs-lookup"><span data-stu-id="53f9e-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="53f9e-250">**WsRequestReply**</span><span class="sxs-lookup"><span data-stu-id="53f9e-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="53f9e-251">**WsSendReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="53f9e-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="53f9e-252">**WsSendFaultMessageForError**</span><span class="sxs-lookup"><span data-stu-id="53f9e-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="53f9e-253">Se queste API non vengono usate, le intestazioni possono essere aggiunte e accessibili manualmente tramite [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) o [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span><span class="sxs-lookup"><span data-stu-id="53f9e-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="53f9e-254">Canali e listener personalizzati</span><span class="sxs-lookup"><span data-stu-id="53f9e-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="53f9e-255">Se il set predefinito di associazioni di canale non soddisfa le esigenze dell'applicazione, è possibile definire un'implementazione del canale e del listener personalizzata specificando l' [**associazione di \_ \_ canale \_ WS-Custom**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) quando si crea il canale o il listener.</span><span class="sxs-lookup"><span data-stu-id="53f9e-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="53f9e-256">L'implementazione effettiva del canale/listener viene specificata come set di callback tramite [**\_ \_ \_ \_ \_ callback del canale personalizzato della proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) o proprietà del listener [**\_ \_ \_ personalizzato della \_ \_ Proprietà**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) del listener WS.</span><span class="sxs-lookup"><span data-stu-id="53f9e-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="53f9e-257">Una volta creato un canale personalizzato o un listener, il risultato è un oggetto [WS \_ Channel](ws-channel.md) o [WS \_ listener](ws-listener.md) che può essere utilizzato con le API esistenti.</span><span class="sxs-lookup"><span data-stu-id="53f9e-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="53f9e-258">Un canale e un listener personalizzati possono essere usati anche con il proxy di servizio e l' [host del servizio](service-host.md) specificando il valore di **\_ \_ \_ associazione del canale personalizzato WS** nell'enumerazione [**WS \_ Channel \_ Binding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) e la proprietà [**WS \_ Channel \_ \_ \_ \_ callback del canale personalizzato**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) e [**WS \_ listener \_ proprietà \_ \_ \_ callback personalizzate**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) proprietà del listener durante la creazione del proxy del servizio o dell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="53f9e-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="53f9e-259">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="53f9e-259">Security</span></span>

<span data-ttu-id="53f9e-260">Il canale consente di limitare la quantità di memoria utilizzata per diversi aspetti delle operazioni tramite proprietà quali:</span><span class="sxs-lookup"><span data-stu-id="53f9e-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="53f9e-261">[**WS \_ \_ \_ dimensioni massime dei \_ \_ messaggi memorizzati \_ nel buffer della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-262">[**WS \_ \_ \_ \_ \_ \_ dimensioni massime del messaggio con flusso della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-263">[**WS \_ \_ \_ dimensioni massime di \_ \_ inizio flusso \_ delle proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-264">[**WS \_ \_dimensioni del \_ \_ buffer delle \_ \_ intestazioni delle \_ \_ richieste http massime della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-265">[**WS \_ \_ \_ dimensioni massime \_ del \_ dizionario \_ della sessione della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="53f9e-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="53f9e-266">Queste proprietà hanno valori predefiniti che sono conservative e sicure per la maggior parte degli scenari.</span><span class="sxs-lookup"><span data-stu-id="53f9e-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="53f9e-267">I valori predefiniti e le eventuali modifiche devono essere valutati con attenzione da potenziali vettori di attacco che possono causare un attacco Denial of Service da un utente remoto.</span><span class="sxs-lookup"><span data-stu-id="53f9e-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="53f9e-268">Il canale consente di impostare i valori di timeout per diversi aspetti delle operazioni tramite proprietà quali:</span><span class="sxs-lookup"><span data-stu-id="53f9e-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="53f9e-269">[**WS \_ \_timeout della \_ connessione \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-270">[**WS \_ \_timeout di \_ INVIO \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-271">[**WS \_ \_timeout della \_ \_ risposta \_ di ricezione della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-272">[**WS \_ \_timeout di \_ ricezione \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-273">[**WS \_ \_timeout di \_ risoluzione \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="53f9e-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="53f9e-274">[**WS \_ \_timeout di \_ chiusura \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="53f9e-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="53f9e-275">Queste proprietà hanno valori predefiniti che sono conservative e sicure per la maggior parte degli scenari.</span><span class="sxs-lookup"><span data-stu-id="53f9e-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="53f9e-276">L'aumento dei valori di timeout aumenta l'intervallo di tempo in cui una parte remota può mantenere attiva una risorsa locale, ad esempio memoria, socket e thread che esegue l'I/O sincrono.</span><span class="sxs-lookup"><span data-stu-id="53f9e-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="53f9e-277">Un'applicazione deve valutare i valori predefiniti e prestare attenzione quando aumenta un timeout perché potrebbe aprire potenziali vettori di attacco che potrebbero causare un attacco Denial of Service da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="53f9e-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="53f9e-278">Di seguito sono riportate alcune delle altre opzioni di configurazione e considerazioni di progettazione dell'applicazione da valutare con attenzione quando si usa l'API del canale WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="53f9e-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="53f9e-279">Quando si utilizza il livello canale/listener, l'applicazione crea e accetta canali sul lato server.</span><span class="sxs-lookup"><span data-stu-id="53f9e-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="53f9e-280">Analogamente, spetta all'applicazione creare e aprire canali sul lato client.</span><span class="sxs-lookup"><span data-stu-id="53f9e-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="53f9e-281">Un'applicazione deve inserire un limite superiore per queste operazioni perché ogni canale utilizza memoria e altre risorse limitate, ad esempio i socket.</span><span class="sxs-lookup"><span data-stu-id="53f9e-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="53f9e-282">Un'applicazione deve prestare particolare attenzione quando crea un canale in risposta a qualsiasi azione attivata da una parte remota.</span><span class="sxs-lookup"><span data-stu-id="53f9e-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="53f9e-283">Spetta all'applicazione scrivere la logica per creare canali e accettarli.</span><span class="sxs-lookup"><span data-stu-id="53f9e-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="53f9e-284">Ogni canale utilizza risorse limitate, ad esempio la memoria e i socket.</span><span class="sxs-lookup"><span data-stu-id="53f9e-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="53f9e-285">Un'applicazione deve avere un limite superiore per il numero di canali che è disposto ad accettare oppure una parte remota può stabilire molte connessioni, causando la memoria insufficiente e quindi un attacco Denial of Service.</span><span class="sxs-lookup"><span data-stu-id="53f9e-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="53f9e-286">Deve inoltre ricevere attivamente messaggi da tali connessioni utilizzando un timeout ridotto.</span><span class="sxs-lookup"><span data-stu-id="53f9e-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="53f9e-287">Se non viene ricevuto alcun messaggio, si verifica il timeout dell'operazione e la connessione deve essere rilasciata.</span><span class="sxs-lookup"><span data-stu-id="53f9e-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="53f9e-288">È possibile che un'applicazione invii una risposta o un errore interpretando le intestazioni SOAP ReplyTo o FaultTo.</span><span class="sxs-lookup"><span data-stu-id="53f9e-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="53f9e-289">La procedura sicura consiste nell'onorare solo un'intestazione ReplyTo o FaultTo, che è "anonima", vale a dire che per inviare la risposta SOAP è necessario usare la connessione esistente (TCP, HTTP) o l'IP di origine (UDP).</span><span class="sxs-lookup"><span data-stu-id="53f9e-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="53f9e-290">Le applicazioni devono prestare molta attenzione durante la creazione di risorse (ad esempio un canale) per rispondere a un altro indirizzo, a meno che il messaggio non sia stato firmato da un'entità in grado di comunicare con l'indirizzo a cui viene inviata la risposta.</span><span class="sxs-lookup"><span data-stu-id="53f9e-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="53f9e-291">La convalida eseguita nel livello del canale non sostituisce l'integrità dei dati realizzata tramite la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="53f9e-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="53f9e-292">Un'applicazione deve basarsi sulle funzionalità di sicurezza di WWSAPI per garantire la comunicazione con un'entità attendibile e deve anche basarsi sulla sicurezza per garantire l'integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="53f9e-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="53f9e-293">Analogamente, sono disponibili le opzioni di configurazione del messaggio e le considerazioni di progettazione dell'applicazione da valutare con attenzione quando si usa l'API del messaggio WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="53f9e-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="53f9e-294">La dimensione dell'heap utilizzato per archiviare le intestazioni di un messaggio può essere configurata utilizzando la proprietà proprietà [**\_ \_ \_ heap \_ proprietà del messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="53f9e-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="53f9e-295">L'aumento di questo valore consente di utilizzare una quantità maggiore di memoria dalle intestazioni del messaggio, il che può comportare la memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="53f9e-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="53f9e-296">L'utente dell'oggetto messaggio deve tenere presente che le API di accesso all'intestazione sono O (n) rispetto al numero di intestazioni nel messaggio, dal momento che verificano la presenza di duplicati.</span><span class="sxs-lookup"><span data-stu-id="53f9e-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="53f9e-297">Le progettazioni che richiedono molte intestazioni in un messaggio possono causare un utilizzo eccessivo della CPU.</span><span class="sxs-lookup"><span data-stu-id="53f9e-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="53f9e-298">Il numero massimo di intestazioni in un messaggio può essere configurato utilizzando la proprietà proprietà [**\_ \_ \_ massime \_ \_ elaborate proprietà messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="53f9e-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="53f9e-299">Esiste inoltre un limite implicito basato sulle dimensioni dell'heap del messaggio.</span><span class="sxs-lookup"><span data-stu-id="53f9e-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="53f9e-300">Aumentando entrambi questi valori è possibile che siano presenti più intestazioni, che determineranno il tempo necessario per trovare un'intestazione (quando si usano le API di accesso all'intestazione).</span><span class="sxs-lookup"><span data-stu-id="53f9e-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 




