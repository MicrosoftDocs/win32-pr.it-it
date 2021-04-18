---
description: 'Esistono due tipi distinti di applicazioni di rete socket: server e client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Informazioni su server e client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307059"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="5ac5e-103">Informazioni su server e client</span><span class="sxs-lookup"><span data-stu-id="5ac5e-103">About Servers and Clients</span></span>

<span data-ttu-id="5ac5e-104">Esistono due tipi distinti di applicazioni di rete socket: server e client.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="5ac5e-105">I server e i client hanno comportamenti diversi; Pertanto, il processo di creazione di tali elementi è diverso.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="5ac5e-106">Di seguito è riportato il modello generale per la creazione di un client e un server TCP/IP di streaming.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="5ac5e-107">Server</span><span class="sxs-lookup"><span data-stu-id="5ac5e-107">Server</span></span>

1.  <span data-ttu-id="5ac5e-108">Inizializzare Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="5ac5e-109">Creare un socket.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-109">Create a socket.</span></span>
3.  <span data-ttu-id="5ac5e-110">Associare il socket.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-110">Bind the socket.</span></span>
4.  <span data-ttu-id="5ac5e-111">Ascolto sul socket per un client.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="5ac5e-112">Accettare una connessione da un client.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="5ac5e-113">Ricevere e inviare dati.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-113">Receive and send data.</span></span>
7.  <span data-ttu-id="5ac5e-114">Eseguire la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="5ac5e-115">Client</span><span class="sxs-lookup"><span data-stu-id="5ac5e-115">Client</span></span>

1.  <span data-ttu-id="5ac5e-116">Inizializzare Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="5ac5e-117">Creare un socket.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-117">Create a socket.</span></span>
3.  <span data-ttu-id="5ac5e-118">Connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-118">Connect to the server.</span></span>
4.  <span data-ttu-id="5ac5e-119">Inviare e ricevere dati.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-119">Send and receive data.</span></span>
5.  <span data-ttu-id="5ac5e-120">Eseguire la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="5ac5e-121">Alcuni passaggi sono gli stessi per un client e un server.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="5ac5e-122">Questi passaggi vengono implementati quasi esattamente allo stesso modo.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="5ac5e-123">Alcuni dei passaggi di questa guida saranno specifici del tipo di applicazione da creare.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="5ac5e-124">Primo passaggio: [creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="5ac5e-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ac5e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ac5e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ac5e-126">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="5ac5e-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



