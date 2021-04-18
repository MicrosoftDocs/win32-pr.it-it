---
description: Concetti relativi ai componenti in coda COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Concetti relativi ai componenti in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304637"
---
# <a name="com-queued-components-concepts"></a><span data-ttu-id="89425-103">Concetti relativi ai componenti in coda COM+</span><span class="sxs-lookup"><span data-stu-id="89425-103">COM+ Queued Components Concepts</span></span>

<span data-ttu-id="89425-104">In base ai servizi di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , il servizio componenti in coda com+ fornisce un modo semplice per richiamare ed eseguire i componenti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="89425-104">Based on [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) services, the COM+ queued components service provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="89425-105">L'elaborazione può verificarsi senza considerare la disponibilità o l'accessibilità del mittente o del destinatario.</span><span class="sxs-lookup"><span data-stu-id="89425-105">Processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

<span data-ttu-id="89425-106">In termini COM, una *coda* è un'area di archiviazione che consente di salvare i messaggi per un successivo recupero.</span><span class="sxs-lookup"><span data-stu-id="89425-106">In COM terms, a *queue* is a storage area that saves messages for later retrieval.</span></span> <span data-ttu-id="89425-107">L'accodamento fornisce un meccanismo per la comunicazione senza connessione.</span><span class="sxs-lookup"><span data-stu-id="89425-107">Queuing provides a mechanism for connectionless communication.</span></span> <span data-ttu-id="89425-108">Ovvero il mittente e il destinatario non sono connessi direttamente e comunicano solo tramite le code.</span><span class="sxs-lookup"><span data-stu-id="89425-108">That is, the sender and receiver are not connected directly and communicate only through queues.</span></span> <span data-ttu-id="89425-109">L'accodamento consente di mantenere le informazioni finché il ricevitore non è pronto per ottenerlo.</span><span class="sxs-lookup"><span data-stu-id="89425-109">Queuing provides a way to hold the information until the receiver is ready to obtain it.</span></span> <span data-ttu-id="89425-110">Il mittente e il destinatario comunicano indirettamente in modo che ciascuno possa funzionare in modo indipendente, non interessato dall'altro.</span><span class="sxs-lookup"><span data-stu-id="89425-110">The sender and receiver are indirectly communicating so that each can operate independently, unaffected by the other.</span></span>

<span data-ttu-id="89425-111">In passato, una conoscenza approfondita del marshalling era necessaria per accodare, inviare e ricevere messaggi asincroni.</span><span class="sxs-lookup"><span data-stu-id="89425-111">In the past, an in-depth knowledge of marshaling was necessary to queue, send, and receive asynchronous messages.</span></span> <span data-ttu-id="89425-112">Ora, usando le chiamate ai metodi facilmente comprensibili e usate dagli sviluppatori di componenti, il servizio componenti accodati COM+ esegue automaticamente il marshalling dei dati sotto forma di messaggio di Accodamento messaggi.</span><span class="sxs-lookup"><span data-stu-id="89425-112">Now, using method calls that are easily understood and used by component developers, the COM+ queued components service automatically marshals data in the form of a Message Queuing message.</span></span> <span data-ttu-id="89425-113">Poiché il servizio componenti in coda offre supporto incorporato per le transazioni, uno stato incoerente non può compromettere i dati se si verifica un errore del server.</span><span class="sxs-lookup"><span data-stu-id="89425-113">And because the queued components service offers built-in support for transactions, an inconsistent state cannot compromise data if a server failure occurs.</span></span>

<span data-ttu-id="89425-114">Negli argomenti seguenti di questa sezione sono contenute informazioni di base sulla progettazione e la scrittura di componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="89425-114">The following topics in this section contain background information about designing and writing queued components.</span></span>



| <span data-ttu-id="89425-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="89425-115">Topic</span></span>                                                                           | <span data-ttu-id="89425-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89425-116">Description</span></span>                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89425-117">Vantaggi dell'elaborazione in coda</span><span class="sxs-lookup"><span data-stu-id="89425-117">Benefits of Queued Processing</span></span>](benefits-of-queued-processing.md)<br/>   | <span data-ttu-id="89425-118">Vengono descritti i vantaggi della programmazione con i componenti in coda COM+.</span><span class="sxs-lookup"><span data-stu-id="89425-118">Describes the benefits of programming with COM+ queued components.</span></span><br/>                                         |
| [<span data-ttu-id="89425-119">Architettura dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="89425-119">Queued Components Architecture</span></span>](queued-components-architecture.md)<br/> | <span data-ttu-id="89425-120">Descrive l'architettura del servizio COM+ Queued Components.</span><span class="sxs-lookup"><span data-stu-id="89425-120">Describes the architecture of the COM+ queued components service.</span></span><br/>                                          |
| [<span data-ttu-id="89425-121">Accodamento messaggi transazionale</span><span class="sxs-lookup"><span data-stu-id="89425-121">Transactional Message Queuing</span></span>](transactional-message-queuing.md)<br/>   | <span data-ttu-id="89425-122">Viene descritto il modo in cui le transazioni vengono gestite dal servizio componenti in coda COM+.</span><span class="sxs-lookup"><span data-stu-id="89425-122">Describes how transactions are handled by the COM+ queued components service.</span></span><br/>                              |
| [<span data-ttu-id="89425-123">Sicurezza dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="89425-123">Queued Components Security</span></span>](queued-components-security.md)<br/>         | <span data-ttu-id="89425-124">Descrive le opzioni dei criteri per l'autenticazione dei messaggi client e le relative implicazioni.</span><span class="sxs-lookup"><span data-stu-id="89425-124">Describes the policy options for authentication of client messages and their implications.</span></span><br/>                 |
| [<span data-ttu-id="89425-125">Sviluppo di componenti in coda</span><span class="sxs-lookup"><span data-stu-id="89425-125">Developing Queued Components</span></span>](developing-queued-components.md)<br/>     | <span data-ttu-id="89425-126">Descrive le considerazioni di programmazione per la scrittura di componenti accodabili.</span><span class="sxs-lookup"><span data-stu-id="89425-126">Describes programming considerations when writing queuable components.</span></span><br/>                                     |
| [<span data-ttu-id="89425-127">Errori dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="89425-127">Queued Components Errors</span></span>](queued-components-errors.md)<br/>             | <span data-ttu-id="89425-128">Vengono descritti i tipi di errori più comuni che possono verificarsi quando si utilizza il servizio componenti in coda COM+.</span><span class="sxs-lookup"><span data-stu-id="89425-128">Describes the most common types of errors you may encounter when using the COM+ queued components service.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="89425-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89425-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89425-130">Attività dei componenti in coda COM+</span><span class="sxs-lookup"><span data-stu-id="89425-130">COM+ Queued Components Tasks</span></span>](com--queued-components-tasks.md)
</dt> </dl>

 

 




