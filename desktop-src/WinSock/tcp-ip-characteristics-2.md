---
description: TCP/IP dispone di caratteristiche che consentono al protocollo di funzionare come requisito di implementazione standardizzato.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Caratteristiche TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882605"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="50dba-103">Caratteristiche TCP/IP</span><span class="sxs-lookup"><span data-stu-id="50dba-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="50dba-104">TCP/IP dispone di caratteristiche che consentono al protocollo di funzionare come requisito di implementazione standardizzato.</span><span class="sxs-lookup"><span data-stu-id="50dba-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="50dba-105">Queste caratteristiche possono essere combinate con scelte di sviluppo che comportano una riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="50dba-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="50dba-106">L'effetto di queste caratteristiche TCP/IP su un'applicazione dipende dal fatto che l'applicazione sia transazionale o in streaming.</span><span class="sxs-lookup"><span data-stu-id="50dba-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="50dba-107">Le applicazioni transazionali sono interessate dal sovraccarico necessario per l'attivazione e la terminazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="50dba-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="50dba-108">Ad esempio, ogni volta che viene stabilita una connessione su una rete Ethernet, devono essere inviati tre pacchetti di circa 60 byte e circa un RTT è necessario per lo scambio.</span><span class="sxs-lookup"><span data-stu-id="50dba-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="50dba-109">Quando si verifica la chiusura di una connessione, vengono scambiati quattro pacchetti.</span><span class="sxs-lookup"><span data-stu-id="50dba-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="50dba-110">Per ogni connessione. un'applicazione che apre e chiude le connessioni spesso comporta questo sovraccarico a ogni occorrenza.</span><span class="sxs-lookup"><span data-stu-id="50dba-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="50dba-111">Un altro aspetto di TCP/IP è l' *avvio lento*, che viene eseguito ogni volta che viene stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="50dba-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="50dba-112">Slow-Start è un limite artificiale per il numero di segmenti di dati che è possibile inviare prima che venga ricevuto il riconoscimento di tali segmenti.</span><span class="sxs-lookup"><span data-stu-id="50dba-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="50dba-113">Slow-Start è progettato per limitare la congestione della rete.</span><span class="sxs-lookup"><span data-stu-id="50dba-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="50dba-114">Quando viene stabilita una connessione su Ethernet, a prescindere dalle dimensioni della finestra del ricevitore, una trasmissione di 4 KB può richiedere fino a 3-4 RTT a causa dell'avvio lento.</span><span class="sxs-lookup"><span data-stu-id="50dba-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="50dba-115">Un'ottimizzazione TCP/IP denominata algoritmo Nagle può anche limitare la velocità di trasferimento dei dati su una connessione.</span><span class="sxs-lookup"><span data-stu-id="50dba-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="50dba-116">L'algoritmo Nagle è progettato per ridurre il sovraccarico del protocollo per le applicazioni che inviano piccole quantità di dati, ad esempio Telnet, che invia un singolo carattere alla volta.</span><span class="sxs-lookup"><span data-stu-id="50dba-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="50dba-117">Anziché inviare immediatamente un pacchetto con un numero elevato di dati di intestazione e dati, lo stack attende più dati dall'applicazione o un riconoscimento prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="50dba-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="50dba-118">I riconoscimenti ritardati, comunemente noti come *ACK ritardati*, sono inoltre progettati in TCP/IP per consentire un piggybacking più efficiente dei riconoscimenti quando i dati restituiti sono imminenti dall'applicazione sul lato ricevente.</span><span class="sxs-lookup"><span data-stu-id="50dba-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="50dba-119">Sfortunatamente, se questi dati non sono imminenti e il lato di invio è in attesa di un riconoscimento, possono verificarsi ritardi di circa 200 millisecondi per invio.</span><span class="sxs-lookup"><span data-stu-id="50dba-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="50dba-120">Quando una connessione TCP viene chiusa, le risorse di connessione nel nodo che ha avviato la chiusura vengono inserite in uno stato di attesa, denominato tempo di attesa, per evitare il danneggiamento dei dati se i pacchetti duplicati vengono sospesi nella rete.</span><span class="sxs-lookup"><span data-stu-id="50dba-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="50dba-121">In questo modo si garantisce che entrambe le estremità siano finite con la connessione.</span><span class="sxs-lookup"><span data-stu-id="50dba-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="50dba-122">Questo può causare l'esaurimento delle risorse richieste per connessione, ad esempio la RAM e le porte, quando le applicazioni aprono e chiudono spesso le connessioni.</span><span class="sxs-lookup"><span data-stu-id="50dba-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="50dba-123">Oltre a essere interessati dall'ACK ritardato e da altri schemi di prevenzione della congestione, le applicazioni di streaming possono anche essere influenzate da una dimensione della finestra di ricezione predefinita troppo piccola nell'estremità ricevente.</span><span class="sxs-lookup"><span data-stu-id="50dba-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50dba-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50dba-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50dba-125">Comportamento dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="50dba-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="50dba-126">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="50dba-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="50dba-127">Algoritmo Nagle</span><span class="sxs-lookup"><span data-stu-id="50dba-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



