---
title: Modello di esecuzione
description: Modello di esecuzione
ms.assetid: 1947eb24-3a55-4d30-924e-93f2eed2c7b6
keywords:
- OpenGL, modello di esecuzione
- modello di esecuzione OpenGL
- OpenGL, modello client/server
- modello client/server OpenGL
- OpenGL, trasparente per la rete
- framebuffer, modello di esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86012912f9bd963da0489b83cc4a5c1e7e1722ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955731"
---
# <a name="execution-model"></a><span data-ttu-id="835be-109">Modello di esecuzione</span><span class="sxs-lookup"><span data-stu-id="835be-109">Execution Model</span></span>

<span data-ttu-id="835be-110">Il modello per l'interpretazione dei comandi OpenGL è client/server.</span><span class="sxs-lookup"><span data-stu-id="835be-110">The model for interpretation of OpenGL commands is client/server.</span></span> <span data-ttu-id="835be-111">Il codice dell'applicazione (il client) rilascia i comandi, che vengono interpretati ed elaborati da OpenGL (il server).</span><span class="sxs-lookup"><span data-stu-id="835be-111">Application code (the client) issues commands, which are interpreted and processed by OpenGL (the server).</span></span> <span data-ttu-id="835be-112">Il server può funzionare o meno nello stesso computer del client.</span><span class="sxs-lookup"><span data-stu-id="835be-112">The server may or may not operate on the same computer as the client.</span></span> <span data-ttu-id="835be-113">In questo senso, OpenGL è trasparente per la rete.</span><span class="sxs-lookup"><span data-stu-id="835be-113">In this sense, OpenGL is network-transparent.</span></span> <span data-ttu-id="835be-114">Un server può gestire diversi contesti OpenGL, ciascuno dei quali è uno stato di OpenGL incapsulato.</span><span class="sxs-lookup"><span data-stu-id="835be-114">A server can maintain several OpenGL contexts, each of which is an encapsulated OpenGL state.</span></span> <span data-ttu-id="835be-115">Un client può connettersi a uno di questi contesti.</span><span class="sxs-lookup"><span data-stu-id="835be-115">A client can connect to any one of these contexts.</span></span> <span data-ttu-id="835be-116">Il protocollo di rete richiesto può essere implementato aumentando un protocollo già esistente, ad esempio quello del sistema Windows X, oppure usando un protocollo indipendente.</span><span class="sxs-lookup"><span data-stu-id="835be-116">The required network protocol can be implemented by augmenting an already existing protocol (such as that of the X Window System) or by using an independent protocol.</span></span> <span data-ttu-id="835be-117">Non è stato fornito alcun comando OpenGL per ottenere l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="835be-117">No OpenGL commands are provided for obtaining user input.</span></span>

<span data-ttu-id="835be-118">Il sistema Windows che alloca le risorse framebuffer controlla infine gli effetti dei comandi OpenGL sul framebuffer.</span><span class="sxs-lookup"><span data-stu-id="835be-118">The window system that allocates framebuffer resources ultimately controls the effects of OpenGL commands on the framebuffer.</span></span> <span data-ttu-id="835be-119">Sistema Windows:</span><span class="sxs-lookup"><span data-stu-id="835be-119">The window system:</span></span>

-   <span data-ttu-id="835be-120">Determina a quali parti del framebuffer OpenGL può accedere in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="835be-120">Determines which portions of the framebuffer OpenGL may access at any given time.</span></span>
-   <span data-ttu-id="835be-121">Comunica con OpenGL come sono strutturate le parti.</span><span class="sxs-lookup"><span data-stu-id="835be-121">Communicates to OpenGL how those portions are structured.</span></span>

<span data-ttu-id="835be-122">Non sono pertanto disponibili comandi OpenGL per la configurazione del framebuffer o l'inizializzazione di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="835be-122">Therefore, there are no OpenGL commands to configure the framebuffer or initialize OpenGL.</span></span> <span data-ttu-id="835be-123">La configurazione del buffer dei frame viene eseguita all'esterno di OpenGL insieme al sistema Windows; L'inizializzazione di OpenGL viene eseguita quando il sistema della finestra alloca una finestra per il rendering OpenGL.</span><span class="sxs-lookup"><span data-stu-id="835be-123">Frame buffer configuration is done outside of OpenGL in conjunction with the window system; OpenGL initialization takes place when the window system allocates a window for OpenGL rendering.</span></span>

 

 




