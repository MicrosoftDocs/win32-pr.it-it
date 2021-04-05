---
title: Attributi di chiamata di funzione
description: I programmi possono usare questi attributi sulle singole funzioni all'interno dell'interfaccia e influiscono solo su tale funzione.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- MIDL, attributi, chiamata di funzione IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714083"
---
# <a name="function-call-attributes"></a><span data-ttu-id="23377-104">Attributi di chiamata di funzione</span><span class="sxs-lookup"><span data-stu-id="23377-104">Function Call Attributes</span></span>

<span data-ttu-id="23377-105">I programmi possono usare questi attributi sulle singole funzioni all'interno dell'interfaccia e influiscono solo su tale funzione.</span><span class="sxs-lookup"><span data-stu-id="23377-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="23377-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="23377-106">Attribute</span></span>                        | <span data-ttu-id="23377-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="23377-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23377-108">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="23377-108">**message**</span></span>](message.md)       | <span data-ttu-id="23377-109">La chiamata di procedura remota deve essere considerata come un messaggio asincrono dal client al server.</span><span class="sxs-lookup"><span data-stu-id="23377-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="23377-110">Il client effettua la chiamata e restituisce immediatamente un risultato, mentre la chiamata effettiva viene gestita dal trasporto di Accodamento messaggi ([**ncadg \_ mq**](ncadg-mq.md)).</span><span class="sxs-lookup"><span data-stu-id="23377-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="23377-111">**Forse**</span><span class="sxs-lookup"><span data-stu-id="23377-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="23377-112">Il client che effettua questa chiamata di procedura remota non prevede alcuna risposta che indichi il recapito o il completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="23377-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="23377-113">Si differenziano dalle operazioni dei [**messaggi**](message.md) in cui non è prevista alcuna risposta, ma il recapito è garantito.</span><span class="sxs-lookup"><span data-stu-id="23377-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="23377-114">**trasmissione**</span><span class="sxs-lookup"><span data-stu-id="23377-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="23377-115">La chiamata di procedura remota deve essere inviata a tutti i server della rete.</span><span class="sxs-lookup"><span data-stu-id="23377-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="23377-116">Il client accetta il primo ritorno, le successive risposte degli altri server vengono scartate.</span><span class="sxs-lookup"><span data-stu-id="23377-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="23377-117">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="23377-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="23377-118">La chiamata non modifica lo stato e restituisce le stesse informazioni ogni volta che viene chiamato con gli stessi parametri di input.</span><span class="sxs-lookup"><span data-stu-id="23377-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="23377-119">**callback**</span><span class="sxs-lookup"><span data-stu-id="23377-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="23377-120">Definisce una funzione che risiede nell'applicazione client, che il server può chiamare per ottenere informazioni dal client.</span><span class="sxs-lookup"><span data-stu-id="23377-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="23377-121">**chiama \_ come**</span><span class="sxs-lookup"><span data-stu-id="23377-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="23377-122">Esegue il mapping di una funzione non a una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="23377-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="23377-123">**locale**</span><span class="sxs-lookup"><span data-stu-id="23377-123">**local**</span></span>](local.md)           | <span data-ttu-id="23377-124">Definisce una procedura locale per la quale MIDL non genera codice stub.</span><span class="sxs-lookup"><span data-stu-id="23377-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="23377-125">Sulle interfacce non [**oggetto**](object.md) , è anche possibile applicare l'attributo [**di \_ gestione del contesto**](context-handle.md) a una funzione per specificare le caratteristiche del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="23377-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




