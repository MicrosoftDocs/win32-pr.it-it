---
title: Funzionamento di RPC
description: Gli strumenti RPC lo rendono visibile agli utenti come se un client chiamasse direttamente una procedura che si trova in un programma server remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711833"
---
# <a name="how-rpc-works"></a><span data-ttu-id="8d254-103">Funzionamento di RPC</span><span class="sxs-lookup"><span data-stu-id="8d254-103">How RPC Works</span></span>

<span data-ttu-id="8d254-104">Gli strumenti RPC lo rendono visibile agli utenti come se un client chiamasse direttamente una procedura che si trova in un programma server remoto.</span><span class="sxs-lookup"><span data-stu-id="8d254-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="8d254-105">Il client e il server dispongono ognuno dei propri spazi di indirizzi. ovvero ogni risorsa ha una propria risorsa di memoria allocata ai dati utilizzati dalla procedura.</span><span class="sxs-lookup"><span data-stu-id="8d254-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="8d254-106">Nella figura seguente viene illustrata l'architettura RPC.</span><span class="sxs-lookup"><span data-stu-id="8d254-106">The following figure illustrates the RPC architecture.</span></span>

![architettura RPC](images/prog-a11.png)

<span data-ttu-id="8d254-108">Come illustrato nella figura, l'applicazione client chiama una procedura Stub locale anziché il codice effettivo che implementa la procedura.</span><span class="sxs-lookup"><span data-stu-id="8d254-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="8d254-109">Gli stub vengono compilati e collegati con l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="8d254-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="8d254-110">Anziché contenere il codice effettivo che implementa la procedura remota, il codice stub del client:</span><span class="sxs-lookup"><span data-stu-id="8d254-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="8d254-111">Recupera i parametri richiesti dallo spazio degli indirizzi del client.</span><span class="sxs-lookup"><span data-stu-id="8d254-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="8d254-112">Converte i parametri in base alle esigenze in un formato NDR standard per la trasmissione in rete.</span><span class="sxs-lookup"><span data-stu-id="8d254-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="8d254-113">Chiama le funzioni nella libreria di runtime del client RPC per inviare la richiesta e i relativi parametri al server.</span><span class="sxs-lookup"><span data-stu-id="8d254-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="8d254-114">Il server esegue i passaggi seguenti per chiamare la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="8d254-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="8d254-115">Le funzioni della libreria run-time RPC del server accettano la richiesta e chiamano la procedura stub del server.</span><span class="sxs-lookup"><span data-stu-id="8d254-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="8d254-116">Lo stub del server recupera i parametri dal buffer di rete e li converte dal formato di trasmissione di rete al formato necessario per il server.</span><span class="sxs-lookup"><span data-stu-id="8d254-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="8d254-117">Lo stub del server chiama la procedura effettiva nel server.</span><span class="sxs-lookup"><span data-stu-id="8d254-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="8d254-118">Viene quindi eseguita la procedura remota, probabilmente generando parametri di output e un valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8d254-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="8d254-119">Al termine della procedura remota, una sequenza simile di passaggi restituisce i dati al client.</span><span class="sxs-lookup"><span data-stu-id="8d254-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="8d254-120">La procedura remota restituisce i dati allo stub del server.</span><span class="sxs-lookup"><span data-stu-id="8d254-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="8d254-121">Lo stub del server converte i parametri di output nel formato necessario per la trasmissione in rete e li restituisce alle funzioni della libreria di run-time RPC.</span><span class="sxs-lookup"><span data-stu-id="8d254-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="8d254-122">Le funzioni della libreria run-time RPC del server trasmettono i dati in rete al computer client.</span><span class="sxs-lookup"><span data-stu-id="8d254-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="8d254-123">Il client completa il processo accettando i dati in rete e restituendo la funzione chiamante.</span><span class="sxs-lookup"><span data-stu-id="8d254-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="8d254-124">La libreria di runtime RPC client riceve i valori restituiti dalla procedura remota e li restituisce allo stub client.</span><span class="sxs-lookup"><span data-stu-id="8d254-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="8d254-125">Lo stub client converte i dati dall'NDR nel formato utilizzato dal computer client.</span><span class="sxs-lookup"><span data-stu-id="8d254-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="8d254-126">Lo stub scrive i dati nella memoria del client e restituisce il risultato al programma chiamante sul client.</span><span class="sxs-lookup"><span data-stu-id="8d254-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="8d254-127">La procedura chiamante continua come se la procedura fosse stata chiamata nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="8d254-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="8d254-128">Le librerie di runtime sono disponibili in due parti: una libreria di importazione, collegata con l'applicazione e la libreria di runtime RPC, implementata come libreria di collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="8d254-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="8d254-129">L'applicazione server contiene le chiamate alle funzioni della libreria di runtime del server che registrano l'interfaccia del server e consentono al server di accettare chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="8d254-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="8d254-130">L'applicazione server contiene anche le procedure remote specifiche dell'applicazione chiamate dalle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="8d254-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




