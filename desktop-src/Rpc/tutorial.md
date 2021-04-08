---
title: Esercitazione
description: Questa esercitazione illustra i passaggi necessari per creare una semplice applicazione distribuita a server singolo a singolo client da un'applicazione autonoma esistente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC remote procedure call, esercitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045079"
---
# <a name="tutorial"></a><span data-ttu-id="97931-104">Esercitazione</span><span class="sxs-lookup"><span data-stu-id="97931-104">Tutorial</span></span>

<span data-ttu-id="97931-105">Questa esercitazione illustra i passaggi necessari per creare una semplice applicazione distribuita a server singolo a singolo client da un'applicazione autonoma esistente.</span><span class="sxs-lookup"><span data-stu-id="97931-105">This tutorial takes you through the steps required to create a simple, single-client, single-server distributed application from an existing standalone application.</span></span> <span data-ttu-id="97931-106">Questi passaggi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="97931-106">These steps are:</span></span>

-   <span data-ttu-id="97931-107">Crea la definizione dell'interfaccia e i file di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97931-107">Create interface definition and application configuration files.</span></span>
-   <span data-ttu-id="97931-108">Usare il compilatore MIDL per generare stub e intestazioni server e client in linguaggio C da tali file.</span><span class="sxs-lookup"><span data-stu-id="97931-108">Use the MIDL compiler to generate C-language client and server stubs and headers from those files.</span></span>
-   <span data-ttu-id="97931-109">Scrivere un'applicazione client che gestisce la connessione al server.</span><span class="sxs-lookup"><span data-stu-id="97931-109">Write a client application that manages its connection to the server.</span></span>
-   <span data-ttu-id="97931-110">Scrivere un'applicazione server contenente le procedure remote effettive.</span><span class="sxs-lookup"><span data-stu-id="97931-110">Write a server application that contains the actual remote procedures.</span></span>
-   <span data-ttu-id="97931-111">Compilare e collegare questi file alla libreria di runtime RPC per produrre l'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="97931-111">Compile and link these files to the RPC run-time library to produce the distributed application.</span></span>

<span data-ttu-id="97931-112">L'applicazione client passa una stringa di caratteri al server in una chiamata di procedura remota e il server stampa la stringa "Hello, World" nell'output standard.</span><span class="sxs-lookup"><span data-stu-id="97931-112">The client application passes a character string to the server in a remote procedure call, and the server prints the string "Hello, World" to its standard output.</span></span>

<span data-ttu-id="97931-113">I file di origine completi per questa applicazione di esempio, con codice aggiuntivo per la gestione dell'input della riga di comando e per l'output di diversi messaggi di stato all'utente, si trovano nella \\ directory Hello RPC di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="97931-113">The complete source files for this example application, with additional code to handle command-line input and to output various status messages to the user, are in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="97931-114">Questa sezione presenta le discussioni negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="97931-114">This section presents its discussion in the following topics:</span></span>

-   [<span data-ttu-id="97931-115">Applicazione autonoma</span><span class="sxs-lookup"><span data-stu-id="97931-115">The Standalone Application</span></span>](the-standalone-application.md)
-   [<span data-ttu-id="97931-116">Definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="97931-116">Defining the Interface</span></span>](defining-the-interface.md)
-   [<span data-ttu-id="97931-117">Generazione dell'UUID</span><span class="sxs-lookup"><span data-stu-id="97931-117">Generating the UUID</span></span>](generating-the-uuid.md)
-   [<span data-ttu-id="97931-118">File IDL</span><span class="sxs-lookup"><span data-stu-id="97931-118">The IDL File</span></span>](the-idl-file.md)
-   [<span data-ttu-id="97931-119">Il file ACF</span><span class="sxs-lookup"><span data-stu-id="97931-119">The ACF File</span></span>](the-acf-file.md)
-   [<span data-ttu-id="97931-120">Generazione dei file stub</span><span class="sxs-lookup"><span data-stu-id="97931-120">Generating the Stub Files</span></span>](generating-the-stub-files.md)
-   [<span data-ttu-id="97931-121">Applicazione client</span><span class="sxs-lookup"><span data-stu-id="97931-121">The Client Application</span></span>](the-client-application.md)
-   [<span data-ttu-id="97931-122">Applicazione server</span><span class="sxs-lookup"><span data-stu-id="97931-122">The Server Application</span></span>](the-server-application.md)
-   [<span data-ttu-id="97931-123">Arresto dell'applicazione server</span><span class="sxs-lookup"><span data-stu-id="97931-123">Stopping the Server Application</span></span>](stopping-the-server-application.md)
-   [<span data-ttu-id="97931-124">Compilazione e collegamento</span><span class="sxs-lookup"><span data-stu-id="97931-124">Compiling and Linking</span></span>](compiling-and-linking.md)
-   [<span data-ttu-id="97931-125">Esecuzione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="97931-125">Running the Application</span></span>](running-the-application.md)

 

 




