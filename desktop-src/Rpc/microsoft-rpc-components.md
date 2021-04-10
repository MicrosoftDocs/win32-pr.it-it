---
title: Componenti RPC
description: Componenti RPC (Remote Procedure Call).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC, descrizione, componenti di RPC (Remote Procedure Call)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955524"
---
# <a name="rpc-components"></a><span data-ttu-id="941dd-104">Componenti RPC</span><span class="sxs-lookup"><span data-stu-id="941dd-104">RPC Components</span></span>

<span data-ttu-id="941dd-105">RPC include i componenti principali seguenti:</span><span class="sxs-lookup"><span data-stu-id="941dd-105">RPC includes the following major components:</span></span>

-   <span data-ttu-id="941dd-106">Compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="941dd-106">MIDL compiler</span></span>
-   <span data-ttu-id="941dd-107">Librerie e file di intestazione della fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="941dd-107">Run-time libraries and header files</span></span>
-   <span data-ttu-id="941dd-108">Nome provider di servizi (a volte definito Locator)</span><span class="sxs-lookup"><span data-stu-id="941dd-108">Name service provider (sometimes referred to as the Locator)</span></span>
-   <span data-ttu-id="941dd-109">Mapper di endpoint (noto anche come Mapper della porta)</span><span class="sxs-lookup"><span data-stu-id="941dd-109">Endpoint mapper (sometimes referred to as the port mapper)</span></span>

<span data-ttu-id="941dd-110">Nel modello RPC è possibile specificare formalmente un'interfaccia per le procedure remote utilizzando una lingua progettata a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="941dd-110">In the RPC model, you can formally specify an interface to the remote procedures using a language designed for this purpose.</span></span> <span data-ttu-id="941dd-111">Questo linguaggio è denominato linguaggio di definizione dell'interfaccia o IDL.</span><span class="sxs-lookup"><span data-stu-id="941dd-111">This language is called the Interface Definition Language, or IDL.</span></span> <span data-ttu-id="941dd-112">L'implementazione Microsoft di questo linguaggio è denominata Microsoft Interface Definition Language o MIDL.</span><span class="sxs-lookup"><span data-stu-id="941dd-112">The Microsoft implementation of this language is called the Microsoft Interface Definition Language, or MIDL.</span></span>

<span data-ttu-id="941dd-113">Dopo aver creato un'interfaccia, è necessario passarla tramite il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="941dd-113">After you create an interface, you must pass it through the MIDL compiler.</span></span> <span data-ttu-id="941dd-114">Questo compilatore genera gli stub che convertono le chiamate di procedure locali in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="941dd-114">This compiler generates the stubs that translate local procedure calls into remote procedure calls.</span></span> <span data-ttu-id="941dd-115">Gli stub sono funzioni segnaposto che eseguono chiamate alle funzioni della libreria di runtime, che gestiscono la chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="941dd-115">Stubs are placeholder functions that make the calls to the run-time library functions, which manage the remote procedure call.</span></span> <span data-ttu-id="941dd-116">Il vantaggio di questo approccio è che la rete diventa quasi completamente trasparente per l'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="941dd-116">The advantage of this approach is that the network becomes almost completely transparent to your distributed application.</span></span> <span data-ttu-id="941dd-117">Il programma client chiama le procedure locali; il lavoro di trasformarli in chiamate remote viene eseguito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="941dd-117">Your client program calls what appear to be local procedures; the work of turning them into remote calls is done for you automatically.</span></span> <span data-ttu-id="941dd-118">Tutto il codice che converte i dati, accede alla rete e recupera i risultati vengono generati automaticamente dal compilatore MIDL ed è invisibile all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="941dd-118">All the code that translates data, accesses the network, and retrieves results is generated for you by the MIDL compiler and is invisible to your application.</span></span>

 

 




