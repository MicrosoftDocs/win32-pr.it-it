---
description: Sviluppo di componenti in coda
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Sviluppo di componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748042"
---
# <a name="developing-queued-components"></a><span data-ttu-id="3dec3-103">Sviluppo di componenti in coda</span><span class="sxs-lookup"><span data-stu-id="3dec3-103">Developing Queued Components</span></span>

<span data-ttu-id="3dec3-104">Il servizio COM+ Queued Components richiede che tutti i metodi dell'applicazione contengano solo \[ \] parametri in, senza valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="3dec3-104">The COM+ queued components service requires all application methods to contain only \[in\] parameters, with no return values.</span></span> <span data-ttu-id="3dec3-105">Poiché l'oggetto server non è necessariamente disponibile quando il client effettua la chiamata, i risultati del server possono essere restituiti inviando un messaggio per la creazione di un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="3dec3-105">Because the server object is not necessarily available when the client makes the call, server results can be returned by sending a message that creates another object.</span></span> <span data-ttu-id="3dec3-106">In questo modo, la comunicazione bidirezionale non si verifica in ogni caso, ma solo quando è necessaria, da una serie di messaggi unidirezionali tra oggetti.</span><span class="sxs-lookup"><span data-stu-id="3dec3-106">In this way, two-way communication occurs not in every case but only when it is required, by a series of one-way messages between objects.</span></span>

<span data-ttu-id="3dec3-107">Per utilizzare il servizio componenti accodati COM+, è necessario che il servizio [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) sia già installato.</span><span class="sxs-lookup"><span data-stu-id="3dec3-107">To use the COM+ queued components service, you must have the [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) service already installed.</span></span> <span data-ttu-id="3dec3-108">Accodamento messaggi non viene installato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3dec3-108">Message Queuing is not installed automatically.</span></span> <span data-ttu-id="3dec3-109">È necessario selezionare Accodamento messaggi durante l'installazione del sistema operativo oppure utilizzando installazione **applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="3dec3-109">Message Queuing must be selected during the operating system setup or by using **Add/Remove programs**.</span></span> <span data-ttu-id="3dec3-110">Un certificato interno di Accodamento messaggi viene creato automaticamente all'accesso.</span><span class="sxs-lookup"><span data-stu-id="3dec3-110">An internal Message Queuing certificate is created automatically at logon.</span></span>

<span data-ttu-id="3dec3-111">Gli argomenti descritti nella tabella seguente forniscono considerazioni aggiuntive per situazioni più specializzate.</span><span class="sxs-lookup"><span data-stu-id="3dec3-111">The topics described in the following table provide additional considerations for more specialized situations.</span></span>



| <span data-ttu-id="3dec3-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="3dec3-112">Topic</span></span>                                                                                           | <span data-ttu-id="3dec3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dec3-113">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dec3-114">[Passaggio di oggetti come parametro](passing-objects-as-parameters.md)s</span><span class="sxs-lookup"><span data-stu-id="3dec3-114">[Passing Objects as Parameter](passing-objects-as-parameters.md)s</span></span><br/>                   | <span data-ttu-id="3dec3-115">Viene descritto come passare gli oggetti \[ come \] parametri nei componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="3dec3-115">Describes how to pass objects as \[in\] parameters to queued components.</span></span><br/>                    |
| [<span data-ttu-id="3dec3-116">Limitazioni di sicurezza in modalità gruppo di lavoro</span><span class="sxs-lookup"><span data-stu-id="3dec3-116">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)<br/> | <span data-ttu-id="3dec3-117">Vengono descritte le limitazioni relative all'utilizzo dell'autenticazione di Accodamento messaggi in modalità gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3dec3-117">Describes limitations on the use of Message Queuing authentication in workgroup mode.</span></span><br/>       |
| [<span data-ttu-id="3dec3-118">Considerazioni sul threading</span><span class="sxs-lookup"><span data-stu-id="3dec3-118">Threading Considerations</span></span>](threading-considerations.md)<br/>                             | <span data-ttu-id="3dec3-119">Vengono descritti i problemi specifici relativi al passaggio di puntatori dell'interfaccia del registratore tra thread.</span><span class="sxs-lookup"><span data-stu-id="3dec3-119">Describes specific concerns related to passing recorder interface pointers between threads.</span></span><br/> |
| [<span data-ttu-id="3dec3-120">Ricezione di una risposta</span><span class="sxs-lookup"><span data-stu-id="3dec3-120">Receiving a Response</span></span>](receiving-a-response.md)<br/>                                     | <span data-ttu-id="3dec3-121">Viene descritto come creare una risposta a una chiamata a un componente in coda.</span><span class="sxs-lookup"><span data-stu-id="3dec3-121">Describes how to construct a response to a queued component call.</span></span><br/>                           |



 

 

 




