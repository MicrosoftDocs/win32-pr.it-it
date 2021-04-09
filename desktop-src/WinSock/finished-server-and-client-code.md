---
description: Esecuzione del codice di esempio completo dell'applicazione server e client TCP/IP.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Esecuzione dell'esempio di codice server e client Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966681"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="9d2bf-103">Esecuzione dell'esempio di codice server e client Winsock</span><span class="sxs-lookup"><span data-stu-id="9d2bf-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="9d2bf-104">Questa sezione contiene il codice sorgente completo per le applicazioni client e server TCP/IP:</span><span class="sxs-lookup"><span data-stu-id="9d2bf-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="9d2bf-105">Codice client Winsock completo</span><span class="sxs-lookup"><span data-stu-id="9d2bf-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="9d2bf-106">Codice server Winsock completo</span><span class="sxs-lookup"><span data-stu-id="9d2bf-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="9d2bf-107">Prima di avviare l'applicazione client, è necessario avviare l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="9d2bf-108">Per eseguire il server, compilare il codice sorgente completo del server ed eseguire il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="9d2bf-109">L'applicazione server è in ascolto sulla porta TCP 27015 per la connessione di un client.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="9d2bf-110">Una volta che un client si connette, il server riceve i dati dal client e restituisce i dati restituiti al client.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="9d2bf-111">Quando il client arresta la connessione, il server arresta il socket client, chiude il socket e viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="9d2bf-112">Per eseguire il client, compilare il codice sorgente completo del client ed eseguire il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="9d2bf-113">L'applicazione client richiede che il nome del computer o dell'indirizzo IP del computer in cui è in esecuzione l'applicazione server venga passato come parametro della riga di comando quando viene eseguito il client.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="9d2bf-114">Se il client e il server vengono eseguiti nel computer di esempio, è possibile avviare il client come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9d2bf-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="9d2bf-115">**localhost client**</span><span class="sxs-lookup"><span data-stu-id="9d2bf-115">**client localhost**</span></span>

<span data-ttu-id="9d2bf-116">Il client tenta di connettersi al server sulla porta TCP 27015.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="9d2bf-117">Una volta che il client si connette, il client invia i dati al server e riceve tutti i dati inviati dal server.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="9d2bf-118">Il client chiude quindi il socket e viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="9d2bf-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d2bf-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d2bf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d2bf-120">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="9d2bf-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



