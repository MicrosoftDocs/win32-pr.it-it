---
title: Protocollo di caricamento BITS
description: Questa sezione descrive il protocollo di rete per i tipi di processo di caricamento BITS e di caricamento-risposta.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708143"
---
# <a name="bits-upload-protocol"></a><span data-ttu-id="a088a-103">Protocollo di caricamento BITS</span><span class="sxs-lookup"><span data-stu-id="a088a-103">BITS Upload Protocol</span></span>

<span data-ttu-id="a088a-104">Questa sezione descrive il protocollo di rete per i tipi di processo di caricamento BITS e di caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="a088a-104">This section describes the network protocol for BITS upload and upload-reply job types.</span></span> <span data-ttu-id="a088a-105">Il protocollo di caricamento BITS è sovrapposto alla parte superiore di HTTP 1,1 e usa molte delle intestazioni HTTP esistenti e definisce nuove intestazioni.</span><span class="sxs-lookup"><span data-stu-id="a088a-105">The BITS upload protocol is layered on top of HTTP 1.1 and uses many of the existing HTTP headers and defines new headers.</span></span> <span data-ttu-id="a088a-106">Il protocollo di caricamento BITS supporta un singolo file di caricamento per sessione.</span><span class="sxs-lookup"><span data-stu-id="a088a-106">The BITS upload protocol supports a single upload file per session.</span></span>

<span data-ttu-id="a088a-107">BITS usa i pacchetti per descrivere le richieste client e le risposte del server.</span><span class="sxs-lookup"><span data-stu-id="a088a-107">BITS uses packets to describe client requests and server responses.</span></span> <span data-ttu-id="a088a-108">L'intestazione BITS-Packet-Type specifica il tipo di pacchetto da inviare.</span><span class="sxs-lookup"><span data-stu-id="a088a-108">The BITS-Packet-Type header specifies the type of packet being sent.</span></span> <span data-ttu-id="a088a-109">Ogni pacchetto contiene intestazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="a088a-109">Each packet contains specific headers.</span></span> <span data-ttu-id="a088a-110">BITS usa il \_ verbo Post bits per identificare i pacchetti di caricamento BITS.</span><span class="sxs-lookup"><span data-stu-id="a088a-110">BITS uses the BITS\_POST verb to identify BITS upload packets.</span></span> <span data-ttu-id="a088a-111">I pacchetti di risposta usano sempre il tipo di pacchetto ACK che sta per confermare.</span><span class="sxs-lookup"><span data-stu-id="a088a-111">Response packets always use the Ack packet type which stands for acknowledge.</span></span> <span data-ttu-id="a088a-112">Il pacchetto ACK viene inviato nel contesto della richiesta precedente; può essere presente una sola richiesta in attesa alla volta.</span><span class="sxs-lookup"><span data-stu-id="a088a-112">The Ack packet is sent in the context of the previous request; there can be only one outstanding request at one time.</span></span>

<span data-ttu-id="a088a-113">Per i processi di caricamento-risposta, BITS usa questo protocollo per caricare il file, ma non usa questo protocollo per inviare la risposta al client.</span><span class="sxs-lookup"><span data-stu-id="a088a-113">For upload-reply jobs, BITS uses this protocol to upload the file but does not use this protocol to send the reply to the client.</span></span> <span data-ttu-id="a088a-114">Al contrario, il server BITS invia il percorso del file di risposta al client e il client crea un processo di download BITS per scaricare il file di risposta.</span><span class="sxs-lookup"><span data-stu-id="a088a-114">Instead, the BITS server sends the location of the reply file to the client and the client creates a BITS download job to download the reply file.</span></span>

<span data-ttu-id="a088a-115">Usare il protocollo di caricamento per sostituire il client BITS o il software server con la propria implementazione.</span><span class="sxs-lookup"><span data-stu-id="a088a-115">Use the upload protocol to replace the BITS client or server software with your own implementation.</span></span> <span data-ttu-id="a088a-116">Per un elenco di pacchetti di richiesta inviati dal client BITS, vedere [pacchetti di richiesta bits](bits-request-packets.md).</span><span class="sxs-lookup"><span data-stu-id="a088a-116">For a list of request packets sent by the BITS client, see [BITS Request Packets](bits-request-packets.md).</span></span> <span data-ttu-id="a088a-117">Per un elenco di pacchetti di risposta inviati dal server BITS, vedere [pacchetti di risposta bits](bits-response-packets.md).</span><span class="sxs-lookup"><span data-stu-id="a088a-117">For a list of response packets sent by the BITS server, see [BITS Response Packets](bits-response-packets.md).</span></span>

<span data-ttu-id="a088a-118">Il client determina il modo in cui risponde a errori o pacchetti imprevisti dal server BITS.</span><span class="sxs-lookup"><span data-stu-id="a088a-118">The client determines how it responds to errors or unexpected packets from the BITS server.</span></span> <span data-ttu-id="a088a-119">Se il server riceve un pacchetto che non si aspetta, il server deve inviare un pacchetto ACK con un codice restituito 400 (richiesta non valida).</span><span class="sxs-lookup"><span data-stu-id="a088a-119">If the server receives a packet that it does not expect, the server should send an Ack packet with a 400 (Bad Request) return code.</span></span>

 

 




