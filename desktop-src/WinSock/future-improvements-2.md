---
description: Miglioramenti futuri per il codice dell'applicazione Winsock di esempio.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Miglioramenti futuri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306972"
---
# <a name="future-improvements"></a><span data-ttu-id="e0aea-103">Miglioramenti futuri</span><span class="sxs-lookup"><span data-stu-id="e0aea-103">Future Improvements</span></span>

<span data-ttu-id="e0aea-104">È possibile apportare diversi miglioramenti a questa applicazione, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="e0aea-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="e0aea-105">Un'unica connessione persistente può essere creata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e0aea-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="e0aea-106">È necessario aggiungere la gestione degli errori appropriata.</span><span class="sxs-lookup"><span data-stu-id="e0aea-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="e0aea-107">In questo modo si riduce il sovraccarico associato all'avvio della connessione e a teardown.</span><span class="sxs-lookup"><span data-stu-id="e0aea-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="e0aea-108">Il codice di risposta sul server può essere ottimizzato per consolidare le risposte, riducendo il numero di pacchetti inviati dal server.</span><span class="sxs-lookup"><span data-stu-id="e0aea-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="e0aea-109">È possibile che siano stati apportati miglioramenti al protocollo.</span><span class="sxs-lookup"><span data-stu-id="e0aea-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="e0aea-110">È possibile, ad esempio, utilizzare una maschera di aggiornamento per indicare le celle da aggiornare e solo i dati della cella inviati.</span><span class="sxs-lookup"><span data-stu-id="e0aea-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="e0aea-111">Gli aggiornamenti possono essere sovrapposti usando thread diversi, in modo che la rete non sia inattiva mentre è in esecuzione la funzione **ComputeNext** .</span><span class="sxs-lookup"><span data-stu-id="e0aea-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0aea-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0aea-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0aea-113">Miglioramento di un'applicazione lenta</span><span class="sxs-lookup"><span data-stu-id="e0aea-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="e0aea-114">Versione di base: applicazione con prestazioni molto scarsa</span><span class="sxs-lookup"><span data-stu-id="e0aea-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="e0aea-115">Revisione 1: pulizia dell'ovvia</span><span class="sxs-lookup"><span data-stu-id="e0aea-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="e0aea-116">Revisione 2: riprogettazione per un minor numero di connessioni</span><span class="sxs-lookup"><span data-stu-id="e0aea-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="e0aea-117">Revisione 3: invio blocco compresso</span><span class="sxs-lookup"><span data-stu-id="e0aea-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



