---
description: Errori dei componenti in coda
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Errori dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305010"
---
# <a name="queued-components-errors"></a><span data-ttu-id="1ad89-103">Errori dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="1ad89-103">Queued Components Errors</span></span>

<span data-ttu-id="1ad89-104">Quando una chiamata a un componente in coda ha esito negativo, perché non è stato possibile trasmettere al server (un errore sul lato client) o perché l'esecuzione non è riuscita al momento dell'arrivo (errore sul lato server), il messaggio di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) corrispondente viene chiamato *messaggio non elaborabile*.</span><span class="sxs-lookup"><span data-stu-id="1ad89-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="1ad89-105">Il servizio componenti in coda COM+ gestisce i messaggi non elaborabili utilizzando una serie di code di tentativi.</span><span class="sxs-lookup"><span data-stu-id="1ad89-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="1ad89-106">Dopo diversi tentativi, il messaggio viene spostato in una coda di riposo finale.</span><span class="sxs-lookup"><span data-stu-id="1ad89-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="1ad89-107">I messaggi rimangono nella coda di riposo fino a quando non vengono spostati manualmente tramite l'utilità di spostamento messaggi dei componenti in coda.</span><span class="sxs-lookup"><span data-stu-id="1ad89-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="1ad89-108">Per ulteriori informazioni sull'utilizzo di Message Mover, vedere [gestione degli errori](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="1ad89-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="1ad89-109">Descrizioni dettagliate della sequenza di eventi che si verificano per diversi tipi di errori sono disponibili negli argomenti descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1ad89-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="1ad89-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="1ad89-110">Topic</span></span>                                                                             | <span data-ttu-id="1ad89-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ad89-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ad89-112">Errori sul lato server</span><span class="sxs-lookup"><span data-stu-id="1ad89-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="1ad89-113">Viene descritta in dettaglio la risposta del servizio componenti in coda COM+ a un errore sul lato server.</span><span class="sxs-lookup"><span data-stu-id="1ad89-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="1ad89-114">Errori lato client</span><span class="sxs-lookup"><span data-stu-id="1ad89-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="1ad89-115">Viene descritta in dettaglio la risposta del servizio componenti in coda COM+ a un errore sul lato client.</span><span class="sxs-lookup"><span data-stu-id="1ad89-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="1ad89-116">Errori persistenti Client-Side</span><span class="sxs-lookup"><span data-stu-id="1ad89-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="1ad89-117">Viene descritto in dettaglio la risposta del servizio componenti in coda COM+ a errori ripetuti sul lato client.</span><span class="sxs-lookup"><span data-stu-id="1ad89-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




