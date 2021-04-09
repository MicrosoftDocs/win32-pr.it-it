---
title: Procedura di compilazione generale
description: Pagina di navigazione per il processo di creazione di un'applicazione client/server mediante RPC (Remote Procedure Call).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044589"
---
# <a name="general-build-procedure"></a><span data-ttu-id="afab0-103">Procedura di compilazione generale</span><span class="sxs-lookup"><span data-stu-id="afab0-103">General Build Procedure</span></span>

<span data-ttu-id="afab0-104">Il processo per la creazione di un'applicazione client/server con Microsoft RPC è il seguente:</span><span class="sxs-lookup"><span data-stu-id="afab0-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="afab0-105">Sviluppare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="afab0-105">Develop the interface.</span></span>
-   <span data-ttu-id="afab0-106">Sviluppare il server che implementa l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="afab0-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="afab0-107">Sviluppare il client che utilizza l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="afab0-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="afab0-108">Nella figura seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="afab0-108">The following figure illustrates these steps.</span></span>

![processo per la creazione di un'applicazione client-server utilizzando Microsoft RPC](images/appdev.png)

<span data-ttu-id="afab0-110">È possibile e comune sviluppare applicazioni client e server simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="afab0-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="afab0-111">Poiché i programmi client e server dipendono dall'interfaccia, tuttavia, l'interfaccia tra di essi deve essere sviluppata prima che il client e il server vengano sviluppati, come illustrato nel diagramma precedente.</span><span class="sxs-lookup"><span data-stu-id="afab0-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="afab0-112">In questa sezione vengono illustrati i passaggi necessari per la compilazione di un'applicazione client/server con RPC.</span><span class="sxs-lookup"><span data-stu-id="afab0-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="afab0-113">Le informazioni vengono presentate negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="afab0-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="afab0-114">Sviluppo dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="afab0-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="afab0-115">Sviluppo del server</span><span class="sxs-lookup"><span data-stu-id="afab0-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="afab0-116">Sviluppo del client</span><span class="sxs-lookup"><span data-stu-id="afab0-116">Developing the Client</span></span>](developing-the-client.md)

 

 




