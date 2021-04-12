---
title: Uso di eventi con chiamate asincrone
description: Uso di eventi con chiamate asincrone
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows Media Format SDK, eventi con chiamate asincrone
- Windows Media Format SDK, eventi di chiamata asincrona
- eventi, chiamate asincrone
- eventi di chiamata asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1729108cae5b73ec96be208709c1360e9401ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396635"
---
# <a name="using-events-with-asynchronous-calls"></a><span data-ttu-id="7089f-107">Uso di eventi con chiamate asincrone</span><span class="sxs-lookup"><span data-stu-id="7089f-107">Using Events with Asynchronous Calls</span></span>

<span data-ttu-id="7089f-108">Spesso, quando si usano metodi che vengono chiamati in modo asincrono, è opportuno arrestare l'ulteriore elaborazione dell'applicazione fino al completamento dell'elaborazione da parte del metodo.</span><span class="sxs-lookup"><span data-stu-id="7089f-108">Frequently, when using methods that are called asynchronously, you will want to halt further processing of your application until after the method completes processing.</span></span> <span data-ttu-id="7089f-109">È possibile implementare tutte le tecniche desiderate per gestire questa situazione.</span><span class="sxs-lookup"><span data-stu-id="7089f-109">You can implement any technique you like to handle this situation.</span></span> <span data-ttu-id="7089f-110">In questa sezione viene descritto l'utilizzo di un evento per attendere le chiamate asincrone nel thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="7089f-110">This section describes using an event to wait for asynchronous calls in the calling thread.</span></span> <span data-ttu-id="7089f-111">Questa tecnica viene spesso usata con Windows Media Format SDK ed è illustrata in alcune applicazioni di esempio.</span><span class="sxs-lookup"><span data-stu-id="7089f-111">This technique is frequently used with the Windows Media Format SDK, and is demonstrated in some of the sample applications.</span></span>

<span data-ttu-id="7089f-112">Nell'elenco seguente viene riepilogato l'utilizzo degli eventi per attendere le chiamate asincrone.</span><span class="sxs-lookup"><span data-stu-id="7089f-112">The following list summarizes the use of events to wait for asynchronous calls.</span></span>

1.  <span data-ttu-id="7089f-113">Creare un evento da usare con l'applicazione chiamando la funzione **CreateEvent** di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7089f-113">Create an event for use with your application by calling the **CreateEvent** function of the Platform SDK.</span></span>
2.  <span data-ttu-id="7089f-114">Quando si implementano i callback appropriati per l'applicazione, intercettare i messaggi per i quali è necessario attendere.</span><span class="sxs-lookup"><span data-stu-id="7089f-114">When implementing the appropriate callbacks for your application, trap the messages for which you need to wait.</span></span> <span data-ttu-id="7089f-115">Nella logica di gestione dei messaggi per i messaggi desiderati, segnalare l'evento chiamando la funzione **seevent** di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7089f-115">In the message handling logic for the desired messages, signal the event by calling the **SetEvent** function of the Platform SDK.</span></span>
3.  <span data-ttu-id="7089f-116">Dopo aver eseguito le chiamate agli eventi asincroni nell'applicazione, attendere che l'evento segnali chiamando la funzione **WaitForSingleObject** di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7089f-116">After calls to asynchronous events are made in your application, wait for the event to signal by calling the **WaitForSingleObject** function of the Platform SDK.</span></span> <span data-ttu-id="7089f-117">Se si progetta un'applicazione Windows, è necessario creare un ciclo per verificare la presenza di messaggi di Windows e includere una chiamata a **WaitForSingleObject** nel ciclo con un breve periodo di attesa.</span><span class="sxs-lookup"><span data-stu-id="7089f-117">If you are designing a Windows application, you should create a loop to check for Windows messages and include a call to **WaitForSingleObject** in the loop with a short wait time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7089f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7089f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7089f-119">**Utilizzo dei metodi di callback**</span><span class="sxs-lookup"><span data-stu-id="7089f-119">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




