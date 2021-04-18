---
description: Nel morphing del codice di aggiornamento della cella della vita, sono state individuate diverse linee guida per la scrittura di applicazioni di rete ad alte prestazioni.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Procedure consigliate per le applicazioni interattive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307047"
---
# <a name="best-practices-for-interactive-applications"></a><span data-ttu-id="c1093-103">Procedure consigliate per le applicazioni interattive</span><span class="sxs-lookup"><span data-stu-id="c1093-103">Best Practices for Interactive Applications</span></span>

<span data-ttu-id="c1093-104">Nel morphing del codice di aggiornamento della cella della vita, sono state individuate diverse linee guida per la scrittura di applicazioni di rete ad alte prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c1093-104">In morphing the Life cell update code, several guidelines for writing high performance network applications have been uncovered.</span></span> <span data-ttu-id="c1093-105">Di seguito sono riportate alcune strategie generali da applicare durante la scrittura di questi tipi di applicazioni:</span><span class="sxs-lookup"><span data-stu-id="c1093-105">Some general strategies to apply when writing these types of applications are:</span></span>

-   <span data-ttu-id="c1093-106">Rendere il flusso di dati quanto più possibile, anziché andare in blocchi.</span><span class="sxs-lookup"><span data-stu-id="c1093-106">Make the data stream as much as possible, rather than going in chunks.</span></span>
-   <span data-ttu-id="c1093-107">Usare alcune transazioni di grandi dimensioni anziché molte più piccole.</span><span class="sxs-lookup"><span data-stu-id="c1093-107">Use a few large transactions rather than many small ones.</span></span> <span data-ttu-id="c1093-108">Anche le transazioni di grandi dimensioni possono essere trasmesse in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="c1093-108">Large transactions can also be efficiently streamed.</span></span>
-   <span data-ttu-id="c1093-109">Riconoscere che la rete è una risorsa lenta e non affidabile e sviluppa ogni applicazione per ridurre al minimo la dipendenza sulla rete.</span><span class="sxs-lookup"><span data-stu-id="c1093-109">Recognize that the network is a slow, unreliable resource and develop each application to minimize its reliance on the network.</span></span>
-   <span data-ttu-id="c1093-110">Usare una rappresentazione ben progettata dei dati in rete.</span><span class="sxs-lookup"><span data-stu-id="c1093-110">Use a well-architected representation of the data on the network.</span></span> <span data-ttu-id="c1093-111">La rappresentazione dei dati deve essere indipendente dall'architettura del computer, non contenere FAT ed eventualmente essere compressa.</span><span class="sxs-lookup"><span data-stu-id="c1093-111">The data representation should be computer-architecture agnostic, contain no fat, and possibly be compressed.</span></span>
-   <span data-ttu-id="c1093-112">Durante l'inizializzazione e l'arresto, non fare in modo che l'utente attenda che la rete venga avviata o arrestata.</span><span class="sxs-lookup"><span data-stu-id="c1093-112">During initialization and shutdown, do not make the user wait for the network to start up or shut down.</span></span> <span data-ttu-id="c1093-113">L'inizializzazione correlata alla rete potrebbe richiedere un tempo relativamente lungo.</span><span class="sxs-lookup"><span data-stu-id="c1093-113">Network related initialization could take a relatively long time.</span></span> <span data-ttu-id="c1093-114">Separare il codice di rete non critico.</span><span class="sxs-lookup"><span data-stu-id="c1093-114">Separate the noncritical network code.</span></span>
-   <span data-ttu-id="c1093-115">Gestire gli errori in base al relativo effetto.</span><span class="sxs-lookup"><span data-stu-id="c1093-115">Handle errors as appropriate to their impact.</span></span> <span data-ttu-id="c1093-116">Non tutti gli errori sono di importanza critica.</span><span class="sxs-lookup"><span data-stu-id="c1093-116">Not all errors are critical.</span></span> <span data-ttu-id="c1093-117">Implementare i meccanismi di ripristino e fornire commenti e suggerimenti degli utenti non intrusivi.</span><span class="sxs-lookup"><span data-stu-id="c1093-117">Implement recovery mechanisms and provide nonintrusive user feedback.</span></span>
-   <span data-ttu-id="c1093-118">Utilizzare RPC (Remote Procedure Call) solo quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="c1093-118">Use remote procedure calls (RPC) only when appropriate.</span></span> <span data-ttu-id="c1093-119">Il protocollo RPC è sincrono in Windows Me/98 e produce sempre un protocollo loquace e FAT quando viene usato per inviare piccole quantità di dati.</span><span class="sxs-lookup"><span data-stu-id="c1093-119">RPC is synchronous on Windows Me/98 and always results in chatty, fat protocols when used to send small amounts of data.</span></span>
-   <span data-ttu-id="c1093-120">Misurare l'overhead di rete con netstat; è possibile che si sorprenda la divulgazione delle misurazioni.</span><span class="sxs-lookup"><span data-stu-id="c1093-120">Measure your network overhead using Netstat; you may be surprised at what your measurements reveal.</span></span>
-   <span data-ttu-id="c1093-121">Testare l'applicazione in un'ampia gamma di reti, in particolare per le reti lente o soggette a perdita.</span><span class="sxs-lookup"><span data-stu-id="c1093-121">Test the application on a variety of networks, especially slow or loss-prone networks.</span></span> <span data-ttu-id="c1093-122">Reti LAN wireless, modem e reti private virtuali (VPN) su Internet sono ottime reti per i test.</span><span class="sxs-lookup"><span data-stu-id="c1093-122">Wireless LAN networks, modems, and virtual private networks (VPN) over the Internet are good networks for testing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1093-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1093-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1093-124">Applicazioni Windows Sockets a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="c1093-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



