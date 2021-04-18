---
description: Errori Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Errori Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304649"
---
# <a name="client-side-errors"></a><span data-ttu-id="a099f-103">Errori Client-Side</span><span class="sxs-lookup"><span data-stu-id="a099f-103">Client-Side Errors</span></span>

<span data-ttu-id="a099f-104">Gli errori sul lato client vengono gestiti in modo analogo agli errori sul lato server.</span><span class="sxs-lookup"><span data-stu-id="a099f-104">Client-side failures are handled in a way that is similar to server-side failures.</span></span> <span data-ttu-id="a099f-105">[Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) può spostare un messaggio nella coda di destinazione se, ad esempio, il messaggio non può essere spostato da client a server.</span><span class="sxs-lookup"><span data-stu-id="a099f-105">[Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) can move a message to its destination queue if, for example, the message cannot be moved from client to server.</span></span> <span data-ttu-id="a099f-106">In questo caso, il messaggio viene spostato nella coda dei messaggi non recapitabili sul lato client.</span><span class="sxs-lookup"><span data-stu-id="a099f-106">In this case, the message is moved to the client-side dead letter queue.</span></span>

<span data-ttu-id="a099f-107">Il servizio componenti in coda COM+ monitora la coda dei messaggi non recapitabili.</span><span class="sxs-lookup"><span data-stu-id="a099f-107">The COM+ queued components service monitors the dead letter queue.</span></span> <span data-ttu-id="a099f-108">Se i messaggi sono stati spostati, il servizio componenti in coda crea un'istanza della classe Exception e chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per richiedere [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span><span class="sxs-lookup"><span data-stu-id="a099f-108">If messages have been moved, the queued components service creates an instance of the exception class and calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to request [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol).</span></span> <span data-ttu-id="a099f-109">Se l'operazione ha esito positivo, il monitoraggio della coda dei messaggi non recapitabili richiama [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span><span class="sxs-lookup"><span data-stu-id="a099f-109">If this is successful, the dead letter queue monitor invokes [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).</span></span>

<span data-ttu-id="a099f-110">L'oggetto può intraprendere alcune azioni per invertire l'effetto di una transazione precedente.</span><span class="sxs-lookup"><span data-stu-id="a099f-110">The object can take some action to reverse the effect of a prior transaction.</span></span> <span data-ttu-id="a099f-111">Se viene eseguito il commit della riproduzione, il messaggio viene rimosso dalla coda dei messaggi non recapitabili di XACT.</span><span class="sxs-lookup"><span data-stu-id="a099f-111">If the playback commits, the message is removed from the Xact dead letter queue.</span></span> <span data-ttu-id="a099f-112">Se la riproduzione ha esito negativo o il CLSID e l'interfaccia necessari non sono disponibili, il messaggio rimane nella coda dei messaggi non recapitabili XACT.</span><span class="sxs-lookup"><span data-stu-id="a099f-112">If the playback fails or the required CLSID and interface are not available, the message remains on the Xact dead letter queue.</span></span>

<span data-ttu-id="a099f-113">Se è necessario intervenire nel processo descritto in precedenza o se è necessario spostare un messaggio non elaborabile dalla coda di riposo finale, usare l'utilità di spostamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="a099f-113">If you need to intervene in the process described above or if you need to move a poison message out of its final resting queue, use the message mover utility.</span></span> <span data-ttu-id="a099f-114">Per ulteriori informazioni sull'utilità Message Mover, vedere [gestione degli errori](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="a099f-114">For more information on the message mover utility, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a099f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a099f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a099f-116">Errori persistenti Client-Side</span><span class="sxs-lookup"><span data-stu-id="a099f-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)
</dt> <dt>

[<span data-ttu-id="a099f-117">Errori sul lato server</span><span class="sxs-lookup"><span data-stu-id="a099f-117">Server-Side Errors</span></span>](server-side-errors.md)
</dt> </dl>

 

 
