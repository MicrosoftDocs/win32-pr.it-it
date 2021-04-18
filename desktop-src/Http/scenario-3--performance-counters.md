---
title: Contatori delle prestazioni dello scenario 3
description: I contatori delle prestazioni misurano quantità di informazioni o dati, in base al numero, alle dimensioni, alla durata e alla frequenza dei dati richiesti o ricevuti.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "106300682"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="707ac-103">Scenario 3: contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="707ac-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="707ac-104">I contatori delle prestazioni misurano quantità di informazioni o dati, in base al numero, alle dimensioni, alla durata e alla frequenza dei dati richiesti o ricevuti.</span><span class="sxs-lookup"><span data-stu-id="707ac-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="707ac-105">Non è previsto l'ottenimento di un elenco di dettagli da un contatore, ad esempio un elenco di messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="707ac-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="707ac-106">Usare invece i contatori delle prestazioni per ottenere le quantità, ad esempio il numero di messaggi di errore dall'avvio o la frequenza con cui vengono generati i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="707ac-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="707ac-107">Contatori delle prestazioni per HTTP.sys</span><span class="sxs-lookup"><span data-stu-id="707ac-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="707ac-108">A partire da Windows Vista e Windows Server 2008, HTTP.sys dispone dei contatori delle metriche delle prestazioni seguenti per semplificare il monitoraggio, la diagnosi e la pianificazione della capacità per i server Web: il componente API server HTTP presenta i contatori delle prestazioni seguenti che consentono il monitoraggio, la diagnosi e la pianificazione della capacità per i server Web:</span><span class="sxs-lookup"><span data-stu-id="707ac-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="707ac-109">Contatori servizio HTTP:</span><span class="sxs-lookup"><span data-stu-id="707ac-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="707ac-110">Numero di URI nella cache, aggiunti dall'avvio, eliminati dall'avvio e numero di scaricamenti della cache</span><span class="sxs-lookup"><span data-stu-id="707ac-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="707ac-111">Riscontri nella cache/secondo e mancati riscontri nella cache/secondo</span><span class="sxs-lookup"><span data-stu-id="707ac-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="707ac-112">Gruppi di URL del servizio HTTP:</span><span class="sxs-lookup"><span data-stu-id="707ac-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="707ac-113">Velocità di invio dati, velocità di ricezione dati, byte trasferiti (inviati e ricevuti)</span><span class="sxs-lookup"><span data-stu-id="707ac-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="707ac-114">Numero massimo di connessioni, velocità dei tentativi di connessione, frequenza delle richieste GET e HEAD e numero totale di richieste</span><span class="sxs-lookup"><span data-stu-id="707ac-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="707ac-115">Code di richieste del servizio HTTP:</span><span class="sxs-lookup"><span data-stu-id="707ac-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="707ac-116">Numero di richieste in coda, validità delle richieste meno recenti in coda (età dell'ultima richiesta nella coda)</span><span class="sxs-lookup"><span data-stu-id="707ac-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="707ac-117">Frequenza di arrivo delle richieste nella coda, frequenza di rifiuto, numero totale di richieste rifiutate, frequenza dei riscontri nella cache</span><span class="sxs-lookup"><span data-stu-id="707ac-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="707ac-118">**Accesso ai contatori delle prestazioni**</span><span class="sxs-lookup"><span data-stu-id="707ac-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="707ac-119">Digitare **PerfMon** al prompt dei comandi per avviare la console di diagnostica delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="707ac-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="707ac-120">Selezionare **Performance Monitor** nel controllo struttura ad albero, quindi aprire il **Aggiungi contatori** facendo clic su **+** .</span><span class="sxs-lookup"><span data-stu-id="707ac-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="707ac-121">Da **Aggiungi contatori** selezionare dai tre set di contatori delle prestazioni **: servizio http**, **code di richieste del servizio http** o gruppi di URL del **servizio http**.</span><span class="sxs-lookup"><span data-stu-id="707ac-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="707ac-122">Per visualizzare i contatori da insiemi di contatori di **richieste del servizio** http e gruppi di **URL del servizio http** , selezionare **istanza** /e, quindi fare clic su **Aggiungi** e infine su **OK**.</span><span class="sxs-lookup"><span data-stu-id="707ac-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="707ac-123">Per visualizzare i contatori del servizio HTTP, selezionare l'insieme di contatori nel riquadro a sinistra e fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="707ac-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="707ac-124">Per ogni computer esiste una sola istanza dei contatori dell'API server HTTP, poiché questi contatori rappresentano lo stato a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="707ac-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="707ac-125">Con le istanze dei contatori delle prestazioni del gruppo di URL, l'ID istanza (per il contatore delle prestazioni) corrisponderà all'ID gruppo URL.</span><span class="sxs-lookup"><span data-stu-id="707ac-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="707ac-126">Per visualizzare l'ID gruppo URL, è possibile eseguire **netsh http show servicestate**.</span><span class="sxs-lookup"><span data-stu-id="707ac-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="707ac-127">Con le istanze dei contatori delle prestazioni della coda di richieste, il nome dell'istanza corrisponde al nome della coda di richieste.</span><span class="sxs-lookup"><span data-stu-id="707ac-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="707ac-128">Il nome della coda di richieste (se esistente) può essere visualizzato dallo stesso **netsh http show servicestate**.</span><span class="sxs-lookup"><span data-stu-id="707ac-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="707ac-129">Tuttavia, alcune applicazioni server possono avere code di richiesta senza nome che non possono essere confrontate con un ID istanza del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="707ac-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




