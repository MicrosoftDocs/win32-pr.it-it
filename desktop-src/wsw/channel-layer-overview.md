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
# <a name="channel-layer-overview"></a>Panoramica sul livello del canale

Il livello del canale fornisce un'astrazione del canale di trasporto e dei messaggi inviati sul canale. Include anche funzioni per la serializzazione dei tipi di dati C da e verso strutture SOAP. Il livello del canale consente il controllo completo delle comunicazioni per mezzo di [messaggi](message.md) costituiti da dati inviati o ricevuti e contenenti corpi e intestazioni e [canali](channel.md) che astraggono i protocolli di scambio dei messaggi e forniscono proprietà per la personalizzazione delle impostazioni.

## <a name="message"></a>Message

Un [messaggio](message.md) è un oggetto che incapsula i dati di rete, in particolare i dati trasmessi o ricevuti in rete. La struttura del messaggio è definita da SOAP, con un set discreto di intestazioni e un corpo del messaggio. Le intestazioni vengono inserite in un buffer di memoria e il corpo del messaggio viene letto o scritto usando un'API di flusso.

![Diagramma che mostra l'intestazione e il corpo di un messaggio.](images/messageenvelope.png)

Sebbene il modello di dati di un messaggio sia sempre il modello di dati XML, il formato wire effettivo è flessibile. Prima che un messaggio venga trasmesso, viene codificato utilizzando una particolare codifica, ad esempio text, Binary o MTOM. Per ulteriori informazioni sulle codifiche, vedere la pagina relativa alla [**\_ codifica WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .

![Diagramma che mostra diversi formati di codifica messaggi.](images/messageandencodings.png)

## <a name="channel"></a>Channel

Un [canale](channel.md) è un oggetto utilizzato per inviare e ricevere messaggi in una rete tra due o più endpoint.

Ai canali sono associati dati che descrivono come [indirizzare](endpoint-address.md) il messaggio quando viene inviato. L'invio di un messaggio su un canale è analogo al posizionamento in uno scivolo: il canale include le informazioni in cui il messaggio deve essere inserito e come ottenerlo.

![Diagramma che mostra i canali per i messaggi.](images/channelsaschute.png)

I canali sono suddivisi in categorie in [**tipi di canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Un tipo di canale specifica la direzione in cui i messaggi possono essere propagati. Il tipo di canale indica inoltre se il canale è con sessione o con sessione. Una sessione viene definita come metodo astratto per la correlazione dei messaggi tra due o più entità. Un esempio di canale con sessione è un canale TCP, che usa la connessione TCP come implementazione della sessione concreta. Un esempio di canale senza sessione è UDP, che non dispone di un meccanismo di sessione sottostante. Sebbene HTTP disponga di connessioni TCP sottostanti, questo fatto non viene esposto direttamente tramite questa API e pertanto HTTP viene considerato anche un canale senza sessione.

![Diagramma che mostra i tipi di canale con sessione e con sessione.](images/channeltypes.png)

Sebbene i tipi di canale descrivano la direzione e le informazioni sulla sessione per un canale, non specificano come viene implementato il canale. Quale protocollo deve essere utilizzato dal canale? Quanto è difficile il canale per tentare di recapitare il messaggio? Quale tipo di sicurezza viene utilizzato? Singlecast o multicast? Queste impostazioni sono denominate "binding" del canale. L'associazione è costituita dagli elementi seguenti:

-   [**Binding di \_ canale \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)che identifica il protocollo di trasferimento da utilizzare (TCP, UDP, http, NAMEDPIPE).
-   [**Descrizione della \_ sicurezza \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), che specifica come proteggere il canale.
-   Set [**WS \_ Channel \_ Property**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, che specificano impostazioni facoltative aggiuntive. Per l'elenco delle proprietà, vedere [**\_ \_ \_ ID proprietà WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .

![Diagramma che mostra un elenco di proprietà del canale.](images/channelsandbindings.png)

## <a name="listener"></a>Listener

Per iniziare a comunicare, il client crea un oggetto canale. Ma in che modo il servizio ottiene il relativo oggetto canale? Questa operazione viene eseguita tramite la creazione di un [listener](listener.md). La creazione di un listener richiede le stesse informazioni di binding necessarie per creare un canale. Una volta creato un listener, l'applicazione può accettare canali dal listener. Poiché l'applicazione può rimanere indietro nell'accettare i canali, i listener in genere mantengono una coda di canali pronti per l'accettazione (fino a una quota).

![Diagramma che mostra i canali nella coda dei listener.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Avvio della comunicazione (client)

Per avviare la comunicazione nel client, usare la sequenza seguente.

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

## <a name="accepting-communication-server"></a>Accettazione della comunicazione (Server)

Per accettare le comunicazioni in ingresso nel server, usare la sequenza seguente.

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

## <a name="sending-messages-client-or-server"></a>Invio di messaggi (client o server)

Per inviare messaggi, utilizzare la sequenza seguente.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La funzione [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) non consente lo streaming e presuppone che il corpo contenga un solo elemento. Per evitare questi vincoli, usare la sequenza seguente anziché **WsSendMessage**.

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

La funzione [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa la serializzazione per scrivere gli elementi del corpo. Per scrivere i dati direttamente nel writer XML, usare la sequenza seguente anziché **WsWriteBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

La funzione [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) utilizza la serializzazione per impostare le intestazioni sul buffer dell'intestazione del messaggio. Per utilizzare il writer XML per scrivere un'intestazione, utilizzare la sequenza seguente anziché **WsAddCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Ricezione di messaggi (client o server)

Per ricevere i messaggi, usare la sequenza seguente.

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

La funzione [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) non consente lo streaming e presuppone che il corpo contenga un solo elemento e che il tipo del messaggio (azione e schema del corpo) sia noto in primo piano. Per evitare questi vincoli, usare la sequenza seguente anziché **WsReceiveMessage**.

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

La funzione [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa la serializzazione per leggere gli elementi del corpo. Per leggere i dati direttamente dal [lettore XML](xml-reader.md), usare la sequenza seguente anziché **WsReadBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

Le funzioni [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) utilizzano la serializzazione per ottenere le intestazioni dal buffer dell'intestazione del messaggio. Per utilizzare il [lettore XML](xml-reader.md) per leggere un'intestazione, utilizzare la sequenza seguente anziché **WsGetCustomHeader**.

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

## <a name="request-reply-client"></a>Risposta richiesta (client)

L'esecuzione di una richiesta-risposta sul client può essere eseguita con la sequenza seguente.

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

La funzione [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) presuppone un singolo elemento per il corpo dei messaggi di richiesta e risposta e che il tipo del messaggio (azione e schema del corpo) sia noto come front. Per evitare queste limitazioni, è possibile inviare manualmente il messaggio di richiesta e di risposta, come illustrato nella sequenza seguente. Questa sequenza corrisponde alla sequenza precedente per l'invio e la ricezione di un messaggio, eccetto laddove specificato.

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

## <a name="request-reply-server"></a>Risposta richiesta (Server)

Per ricevere un messaggio di richiesta sul server, utilizzare la stessa sequenza descritta nella sezione precedente relativa alla ricezione dei messaggi.

Per inviare un messaggio di risposta o di errore, usare la sequenza seguente.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La funzione [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) presuppone un singolo elemento nel corpo e non consente lo streaming. Per evitare queste limitazioni, usare la sequenza seguente. Corrisponde alla sequenza precedente per l'invio di un messaggio, ma utilizza il [**messaggio WS \_ Reply \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) anziché il **messaggio WS \_ blank \_** durante l'inizializzazione.

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

## <a name="message-exchange-patterns"></a>Modelli di scambio dei messaggi

Il [**\_ \_ tipo di canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) impone il modello di scambio dei messaggi possibile per un canale specifico. Il tipo supportato varia in base all'associazione, come indicato di seguito:

-   [**WS \_ L' \_ \_ associazione di canale http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta la [**\_ \_ \_ richiesta WS Channel Type**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) nel client e la **risposta del \_ \_ tipo \_ di canale WS** sul server.
-   [**WS \_ L' \_ \_ associazione di canale TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta la [**\_ \_ \_ \_ sessione duplex WS del tipo**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) di canale nel client e la **\_ \_ \_ \_ sessione duplex del tipo di canale WS** sul server.
-   [**WS \_ L' \_ \_ associazione di canale UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta il [**tipo di canale di WS \_ \_ \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) nel client e l'input del **\_ tipo di canale \_ \_ WS** sul server.
-   [**WS \_ L' \_ \_ associazione di canale NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta [**WS \_ Channel \_ Type \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) nell' **\_ \_ \_ input del tipo** di canale client e WS sul server.

## <a name="message-loops"></a>Cicli di messaggi

Per ogni modello di scambio di messaggi è disponibile un "ciclo" specifico che può essere usato per inviare o ricevere messaggi. Il ciclo descrive l'ordine valido delle operazioni necessarie per l'invio e la ricezione di più messaggi. I cicli vengono descritti sotto come produzioni di grammatica. Il termine ' end ' è un oggetto Receive dove **WS \_ S \_ end** viene restituito (vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md)), che indica che nel canale non sono disponibili altri messaggi. Nell'ambiente di produzione parallelo viene specificato che per Parallel (x & y) l'operazione x può essere eseguita contemporaneamente a y.

Nel client vengono usati i cicli seguenti:

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

Nel server vengono usati i cicli seguenti:

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

L'utilizzo [**dell' \_ \_ associazione di \_ \_ sicurezza del \_ messaggio del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sul server richiede una ricezione riuscita prima che sia consentito l'invio anche con un canale di tipo [**\_ \_ \_ \_ sessione duplex di tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Dopo la prima ricezione. viene applicato il ciclo normale.

Si noti che è possibile usare i canali di tipo [**WS \_ Channel \_ Type \_ Request**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) e **WS \_ Channel \_ Type \_ Reply** per inviare e ricevere messaggi unidirezionali (e il modello Request-Reply standard). Questa operazione viene eseguita chiudendo il canale di risposta senza inviare una risposta. In questo caso, non verrà ricevuta alcuna risposta sul canale di richiesta. Il valore restituito di **WS \_ S \_ end** utilizzando [**l' \_ \_ associazione di \_ \_ sicurezza del \_ messaggio del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sul server richiede una ricezione riuscita prima che l'invio sia consentito anche con un canale di tipo **WS \_ Channel \_ Type \_ duplex \_ Session**. Dopo la prima ricezione, viene applicato il ciclo normale.

viene restituito, che indica che non è disponibile alcun messaggio.

I cicli client o server possono essere eseguiti in parallelo tra loro utilizzando più istanze del canale.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Filtro messaggi

Un canale server può filtrare i messaggi ricevuti che non sono destinati all'applicazione, ad esempio messaggi che stabiliscono un [contesto di sicurezza](security-context.md). In tal caso, **WS \_ S \_ end** verrà restituito da [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) e nessun messaggio dell'applicazione sarà disponibile sul canale. Tuttavia, ciò non segnala che il client intende terminare la comunicazione con il server. È possibile che siano disponibili altri messaggi su un altro canale. Vedere [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).

## <a name="cancellation"></a>Annullamento

La funzione [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) viene usata per annullare i/o in sospeso per un canale. Questa API non attende il completamento delle operazioni di i/o. Per ulteriori informazioni, vedere il diagramma di stato del [**\_ canale \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) e la documentazione relativa a **WsAbortChannel** .

L'API [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) viene utilizzata per annullare i/o in sospeso per un listener. Questa API non attende il completamento delle operazioni di i/o. Se si interrompe un listener, verranno interrotte anche le accettazioni in sospeso. Per ulteriori informazioni, vedere il diagramma di stato del [**\_ listener \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) e **WsAbortListener** .

## <a name="tcp"></a>TCP

L' [**\_ associazione di \_ canale \_ WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su TCP. La specifica SOAP su TCP si basa sul meccanismo di framing .NET.

La condivisione delle porte non è supportata in questa versione. Ogni listener aperto deve usare un numero di porta diverso.

## <a name="udp"></a>UDP

L' [**\_ associazione di \_ canale \_ WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su UDP.

Il binding UDP presenta alcune limitazioni:

-   Non è disponibile alcun supporto per la sicurezza.
-   I messaggi possono essere persi o duplicati.
-   È supportata una sola codifica: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   I messaggi sono fondamentalmente limitati a 64K e spesso hanno una maggiore probabilità di essere persi se le dimensioni superano la MTU della rete.

## <a name="http"></a>HTTP

L' [**\_ associazione di \_ canale \_ WS HTTP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su http.

Per controllare le intestazioni specifiche HTTP nel client e nel server, vedere [**WS \_ http \_ message \_ mapping**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Per inviare e ricevere messaggi non SOAP sul server, utilizzare la [**codifica WS \_ \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) per la [**\_ codifica della \_ proprietà \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>NAMEDPIPES

L' [**\_ associazione di \_ canale \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supporta SOAP su named pipe, consentendo la comunicazione con il servizio Windows Communication Foundation (WCF) utilizzando NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Correlazione dei messaggi di richiesta/risposta

I messaggi di richiesta/risposta sono correlati in uno dei due modi seguenti:

-   La correlazione viene eseguita utilizzando il canale come meccanismo di correlazione. Ad esempio, quando si usa il [**trasporto della versione di WS \_ Addressing \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e il [**\_ \_ \_ binding del canale WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , la risposta per il messaggio di richiesta è correlata alla richiesta dal fatto che è il corpo dell'entità della risposta http.
-   La correlazione viene eseguita utilizzando le intestazioni MessageID e repiù recenti. Questo meccanismo viene utilizzato con [**WS \_ Addressing \_ versione \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e **WS \_ Addressing \_ versione \_ 0 \_ 9** (anche quando si utilizza l' [**\_ associazione di \_ canale \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). In questo caso, il messaggio di richiesta include l'intestazione MessageID. Il messaggio di risposta include un'intestazione reultimissimo con il valore dell'intestazione MessageID della richiesta. L'intestazione reultimissime consente al client di correlare una risposta a una richiesta inviata.

Le API di livello del canale seguenti usano automaticamente i meccanismi di correlazione appropriati basati sulla [**\_ \_ versione WS Addressing**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) del canale.

-   [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Se queste API non vengono usate, le intestazioni possono essere aggiunte e accessibili manualmente tramite [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) o [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).

## <a name="custom-channels-and-listeners"></a>Canali e listener personalizzati

Se il set predefinito di associazioni di canale non soddisfa le esigenze dell'applicazione, è possibile definire un'implementazione del canale e del listener personalizzata specificando l' [**associazione di \_ \_ canale \_ WS-Custom**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) quando si crea il canale o il listener. L'implementazione effettiva del canale/listener viene specificata come set di callback tramite [**\_ \_ \_ \_ \_ callback del canale personalizzato della proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) o proprietà del listener [**\_ \_ \_ personalizzato della \_ \_ Proprietà**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) del listener WS. Una volta creato un canale personalizzato o un listener, il risultato è un oggetto [WS \_ Channel](ws-channel.md) o [WS \_ listener](ws-listener.md) che può essere utilizzato con le API esistenti.

Un canale e un listener personalizzati possono essere usati anche con il proxy di servizio e l' [host del servizio](service-host.md) specificando il valore di **\_ \_ \_ associazione del canale personalizzato WS** nell'enumerazione [**WS \_ Channel \_ Binding**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) e la proprietà [**WS \_ Channel \_ \_ \_ \_ callback del canale personalizzato**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) e [**WS \_ listener \_ proprietà \_ \_ \_ callback personalizzate**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) proprietà del listener durante la creazione del proxy del servizio o dell'host del servizio.

## <a name="security"></a>Sicurezza

Il canale consente di limitare la quantità di memoria utilizzata per diversi aspetti delle operazioni tramite proprietà quali:

-   [**WS \_ \_ \_ dimensioni massime dei \_ \_ messaggi memorizzati \_ nel buffer della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ \_ \_ \_ dimensioni massime del messaggio con flusso della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ dimensioni massime di \_ \_ inizio flusso \_ delle proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_dimensioni del \_ \_ buffer delle \_ \_ intestazioni delle \_ \_ richieste http massime della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ dimensioni massime \_ del \_ dizionario \_ della sessione della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Queste proprietà hanno valori predefiniti che sono conservative e sicure per la maggior parte degli scenari. I valori predefiniti e le eventuali modifiche devono essere valutati con attenzione da potenziali vettori di attacco che possono causare un attacco Denial of Service da un utente remoto.

Il canale consente di impostare i valori di timeout per diversi aspetti delle operazioni tramite proprietà quali:

-   [**WS \_ \_timeout della \_ connessione \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_timeout di \_ INVIO \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_timeout della \_ \_ risposta \_ di ricezione della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_timeout di \_ ricezione \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_timeout di \_ risoluzione \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_timeout di \_ chiusura \_ della proprietà del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Queste proprietà hanno valori predefiniti che sono conservative e sicure per la maggior parte degli scenari. L'aumento dei valori di timeout aumenta l'intervallo di tempo in cui una parte remota può mantenere attiva una risorsa locale, ad esempio memoria, socket e thread che esegue l'I/O sincrono. Un'applicazione deve valutare i valori predefiniti e prestare attenzione quando aumenta un timeout perché potrebbe aprire potenziali vettori di attacco che potrebbero causare un attacco Denial of Service da un computer remoto.

Di seguito sono riportate alcune delle altre opzioni di configurazione e considerazioni di progettazione dell'applicazione da valutare con attenzione quando si usa l'API del canale WWSAPI:

-   Quando si utilizza il livello canale/listener, l'applicazione crea e accetta canali sul lato server. Analogamente, spetta all'applicazione creare e aprire canali sul lato client. Un'applicazione deve inserire un limite superiore per queste operazioni perché ogni canale utilizza memoria e altre risorse limitate, ad esempio i socket. Un'applicazione deve prestare particolare attenzione quando crea un canale in risposta a qualsiasi azione attivata da una parte remota.
-   Spetta all'applicazione scrivere la logica per creare canali e accettarli. Ogni canale utilizza risorse limitate, ad esempio la memoria e i socket. Un'applicazione deve avere un limite superiore per il numero di canali che è disposto ad accettare oppure una parte remota può stabilire molte connessioni, causando la memoria insufficiente e quindi un attacco Denial of Service. Deve inoltre ricevere attivamente messaggi da tali connessioni utilizzando un timeout ridotto. Se non viene ricevuto alcun messaggio, si verifica il timeout dell'operazione e la connessione deve essere rilasciata.
-   È possibile che un'applicazione invii una risposta o un errore interpretando le intestazioni SOAP ReplyTo o FaultTo. La procedura sicura consiste nell'onorare solo un'intestazione ReplyTo o FaultTo, che è "anonima", vale a dire che per inviare la risposta SOAP è necessario usare la connessione esistente (TCP, HTTP) o l'IP di origine (UDP). Le applicazioni devono prestare molta attenzione durante la creazione di risorse (ad esempio un canale) per rispondere a un altro indirizzo, a meno che il messaggio non sia stato firmato da un'entità in grado di comunicare con l'indirizzo a cui viene inviata la risposta.
-   La convalida eseguita nel livello del canale non sostituisce l'integrità dei dati realizzata tramite la sicurezza. Un'applicazione deve basarsi sulle funzionalità di sicurezza di WWSAPI per garantire la comunicazione con un'entità attendibile e deve anche basarsi sulla sicurezza per garantire l'integrità dei dati.

Analogamente, sono disponibili le opzioni di configurazione del messaggio e le considerazioni di progettazione dell'applicazione da valutare con attenzione quando si usa l'API del messaggio WWSAPI:

-   La dimensione dell'heap utilizzato per archiviare le intestazioni di un messaggio può essere configurata utilizzando la proprietà proprietà [**\_ \_ \_ heap \_ proprietà del messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . L'aumento di questo valore consente di utilizzare una quantità maggiore di memoria dalle intestazioni del messaggio, il che può comportare la memoria insufficiente.
-   L'utente dell'oggetto messaggio deve tenere presente che le API di accesso all'intestazione sono O (n) rispetto al numero di intestazioni nel messaggio, dal momento che verificano la presenza di duplicati. Le progettazioni che richiedono molte intestazioni in un messaggio possono causare un utilizzo eccessivo della CPU.
-   Il numero massimo di intestazioni in un messaggio può essere configurato utilizzando la proprietà proprietà [**\_ \_ \_ massime \_ \_ elaborate proprietà messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Esiste inoltre un limite implicito basato sulle dimensioni dell'heap del messaggio. Aumentando entrambi questi valori è possibile che siano presenti più intestazioni, che determineranno il tempo necessario per trovare un'intestazione (quando si usano le API di accesso all'intestazione).

 

 




