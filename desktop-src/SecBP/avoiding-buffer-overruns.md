---
description: Viene fornita una breve introduzione ad alcuni tipi di situazioni di sovraccarico del buffer e vengono offerte alcune idee e risorse che consentono di evitare la creazione di nuovi rischi e attenuare quelli esistenti.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Evitare i sovraccarichi del buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315422"
---
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="04550-103">Evitare i sovraccarichi del buffer</span><span class="sxs-lookup"><span data-stu-id="04550-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="04550-104">Un sovraccarico del buffer è una delle fonti più comuni di rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="04550-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="04550-105">Un sovraccarico del buffer è essenzialmente causato dal trattamento degli input esterni deselezionati come dati attendibili.</span><span class="sxs-lookup"><span data-stu-id="04550-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="04550-106">L'atto di copiare questi dati, usando operazioni come [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** o **wcscpy**, può creare risultati imprevisti che consentono il danneggiamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="04550-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="04550-107">Nei casi migliori, l'applicazione verrà interrotta con un dump di base, un errore di segmentazione o una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="04550-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="04550-108">Nel peggiore dei casi, un utente malintenzionato può sfruttare il sovraccarico del buffer introducendo ed eseguendo altro codice dannoso nel processo.</span><span class="sxs-lookup"><span data-stu-id="04550-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="04550-109">La copia di dati di input deselezionati in un buffer basato su stack è la ragione più comune di errori sfruttabili.</span><span class="sxs-lookup"><span data-stu-id="04550-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="04550-110">I sovraccarichi del buffer possono essere eseguiti in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="04550-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="04550-111">Nell'elenco seguente viene fornita una breve introduzione ad alcuni tipi di situazioni di sovraccarico del buffer e vengono offerte alcune idee e risorse che consentono di evitare la creazione di nuovi rischi e attenuare quelli esistenti:</span><span class="sxs-lookup"><span data-stu-id="04550-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="04550-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Sovraccarichi del buffer statici</span><span class="sxs-lookup"><span data-stu-id="04550-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="04550-113">Un sovraccarico del buffer statico si verifica quando un buffer, dichiarato nello stack, viene scritto con un numero di dati superiore a quello allocato.</span><span class="sxs-lookup"><span data-stu-id="04550-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="04550-114">Le versioni meno evidenti di questo errore si verificano quando i dati di input utente non verificati vengono copiati direttamente in una variabile statica, causando un potenziale danneggiamento dello stack.</span><span class="sxs-lookup"><span data-stu-id="04550-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="04550-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Sovraccarichi heap</span><span class="sxs-lookup"><span data-stu-id="04550-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="04550-116">I sovraccarichi dell'heap, come i sovraccarichi del buffer statico, possono causare danneggiamenti della memoria e dello stack.</span><span class="sxs-lookup"><span data-stu-id="04550-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="04550-117">Poiché i sovraccarichi dell'heap si verificano nella memoria heap anziché nello stack, alcuni utenti li considerano meno in grado di causare gravi problemi; Tuttavia, i sovraccarichi dell'heap richiedono una reale attenzione alla programmazione e sono in grado di consentire i rischi di sistema come sovraccarichi del buffer statico.</span><span class="sxs-lookup"><span data-stu-id="04550-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="04550-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Errori di indicizzazione della matrice</span><span class="sxs-lookup"><span data-stu-id="04550-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="04550-119">Gli errori di indicizzazione della matrice sono inoltre un'origine di sovraccarichi di memoria.</span><span class="sxs-lookup"><span data-stu-id="04550-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="04550-120">Il controllo accurato dei limiti e la gestione degli indici contribuiranno a impedire questo tipo di sovraccarico di memoria.</span><span class="sxs-lookup"><span data-stu-id="04550-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="04550-121">La prevenzione dei sovraccarichi del buffer riguarda principalmente la scrittura di codice valido.</span><span class="sxs-lookup"><span data-stu-id="04550-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="04550-122">Convalidare sempre tutti gli input e non eseguire correttamente l'operazione quando necessario.</span><span class="sxs-lookup"><span data-stu-id="04550-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="04550-123">Per ulteriori informazioni sulla scrittura di codice protetto, vedere le risorse seguenti:</span><span class="sxs-lookup"><span data-stu-id="04550-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="04550-124">Maguire, Steve \[ 1993 \] , *scrittura di codice solido*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="04550-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="04550-125">Howard, Michael e LeBlanc, David \[ 2003 \] , *scrittura di codice sicuro*, 2D ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="04550-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="04550-126">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi.</span><span class="sxs-lookup"><span data-stu-id="04550-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="04550-127">Una gestione sicura delle stringhe è un problema di lunga durata che continua a essere risolto, seguendo le buone procedure di programmazione e spesso usando e adeguando i sistemi esistenti con funzioni sicure di gestione delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="04550-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="04550-128">Un esempio di tale set di funzioni per la shell di Windows inizia con [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span><span class="sxs-lookup"><span data-stu-id="04550-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 
