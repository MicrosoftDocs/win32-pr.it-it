---
description: La classe CMsgThread fornisce supporto per un thread di lavoro al quale è possibile inviare le richieste in modo asincrono anziché essere inviate direttamente.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Classe CMsg
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304124"
---
# <a name="cmsg-class"></a><span data-ttu-id="dc2b3-103">Classe CMsg</span><span class="sxs-lookup"><span data-stu-id="dc2b3-103">CMsg class</span></span>

<span data-ttu-id="dc2b3-104">La classe [**CMsgThread**](cmsgthread.md) fornisce supporto per un thread di lavoro al quale è possibile inviare le richieste in modo asincrono anziché essere inviate direttamente.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="dc2b3-105">La classe [**CAMThread**](camthread.md) fornisce un thread di lavoro a cui è possibile inviare singole richieste.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="dc2b3-106">Solo un client può effettuare una richiesta alla volta e il client si blocca fino a quando il thread di lavoro non ha completato la richiesta.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="dc2b3-107">Al contrario, la classe **CMsgThread** fornisce un thread di lavoro a cui è possibile inviare un numero qualsiasi di richieste.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="dc2b3-108">Le richieste (sotto forma di `CMsg` oggetto) vengono accodate ed eseguite in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="dc2b3-109">Non viene ricevuto alcun valore restituito o di risposta.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-109">No reply or return value is received.</span></span>



| <span data-ttu-id="dc2b3-110">Membri dei dati</span><span class="sxs-lookup"><span data-stu-id="dc2b3-110">Data Members</span></span>              | <span data-ttu-id="dc2b3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc2b3-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2b3-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="dc2b3-112">dwFlags</span></span>                   | <span data-ttu-id="dc2b3-113">Parametro del flag per il codice della richiesta.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="dc2b3-114">lpParam</span><span class="sxs-lookup"><span data-stu-id="dc2b3-114">lpParam</span></span>                   | <span data-ttu-id="dc2b3-115">Dati richiesti dal thread di lavoro come parametri o valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="dc2b3-116">Questi dati non devono essere basati su stack, in quanto verrà fatto riferimento a un po' di tempo dopo il completamento dell'operazione di Accodamento.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="dc2b3-117">pEvent</span><span class="sxs-lookup"><span data-stu-id="dc2b3-117">pEvent</span></span>                    | <span data-ttu-id="dc2b3-118">Oggetto evento che un thread di lavoro può segnalare per indicare il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="dc2b3-119">uMsg</span><span class="sxs-lookup"><span data-stu-id="dc2b3-119">uMsg</span></span>                      | <span data-ttu-id="dc2b3-120">Codice di richiesta definito dal client della classe thread e riconosciuto dalla funzione thread di lavoro sottoposta a override.</span><span class="sxs-lookup"><span data-stu-id="dc2b3-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="dc2b3-121">Funzioni di membro</span><span class="sxs-lookup"><span data-stu-id="dc2b3-121">Member Functions</span></span>          | <span data-ttu-id="dc2b3-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc2b3-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="dc2b3-123">**CMsg**</span><span class="sxs-lookup"><span data-stu-id="dc2b3-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="dc2b3-124">Costruisce un oggetto [**CMsg**](cmsg-cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2b3-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



