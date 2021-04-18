---
description: Una coda di file è un elenco di operazioni di file elaborate in una sola volta. Le operazioni sui file nella coda possono essere operazioni di copia, ridenominazione o eliminazione. La coda file organizza le operazioni sui file in base al tipo, creando la copia, la ridenominazione e l'eliminazione delle code secondarie.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Informazioni sulle code di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306521"
---
# <a name="about-file-queues"></a><span data-ttu-id="af774-105">Informazioni sulle code di file</span><span class="sxs-lookup"><span data-stu-id="af774-105">About File Queues</span></span>

<span data-ttu-id="af774-106">Una coda di file è un elenco di operazioni di file elaborate in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="af774-106">A file queue is a list of file operations that are processed at one time.</span></span> <span data-ttu-id="af774-107">Le operazioni sui file nella coda possono essere operazioni di copia, ridenominazione o eliminazione.</span><span class="sxs-lookup"><span data-stu-id="af774-107">The file operations in the queue may be copy, rename, or delete operations.</span></span> <span data-ttu-id="af774-108">La coda file organizza le operazioni sui file in base al tipo, creando la copia, la ridenominazione e l'eliminazione delle code secondarie.</span><span class="sxs-lookup"><span data-stu-id="af774-108">The file queue organizes file operations by type, creating copy, rename, and delete subqueues.</span></span>

<span data-ttu-id="af774-109">Queste operazioni possono essere inviate alla coda in qualsiasi ordine e il processo di Accodamento non deve essere contiguo.</span><span class="sxs-lookup"><span data-stu-id="af774-109">These operations may be sent to the queue in any order, and the enqueuing process need not be contiguous.</span></span> <span data-ttu-id="af774-110">Quando viene eseguito il commit della coda, la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) esegue le operazioni sui file in ordine del tipo di operazione.</span><span class="sxs-lookup"><span data-stu-id="af774-110">When the queue is committed, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function performs file operations in order of the operation type.</span></span>

<span data-ttu-id="af774-111">In genere, tutte le operazioni sui file necessarie per un'intera installazione vengono accodate alla coda di file e quindi elaborate in un singolo batch quando viene eseguito il commit della coda.</span><span class="sxs-lookup"><span data-stu-id="af774-111">Typically, all of the file operations necessary for an entire installation are queued to the file queue, and then processed in a single batch when the queue is committed.</span></span>

<span data-ttu-id="af774-112">Un vantaggio di accodamento delle operazioni sui file rispetto all'installazione dei file sezione per sezione da un file INF è che è possibile semplificare il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="af774-112">One advantage of queuing file operations over installing files section-by-section from an INF file is that you can streamline the installation process.</span></span> <span data-ttu-id="af774-113">Anziché dover ottenere informazioni dall'utente per ogni sezione da installare, è possibile ottenere informazioni sull'installazione dall'utente per tutti i file da installare durante la compilazione della coda.</span><span class="sxs-lookup"><span data-stu-id="af774-113">Instead of having to obtain information from the user for each section to be installed, you can obtain installation information from the user for all the files to be installed while building the queue.</span></span> <span data-ttu-id="af774-114">In questo modo l'utente può proseguire con altre attività mentre le operazioni di copia che richiedono molto tempo vengono elaborate dalla funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .</span><span class="sxs-lookup"><span data-stu-id="af774-114">This frees the user to pursue other activities while the time-intensive copy operations are processed by the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function.</span></span>

<span data-ttu-id="af774-115">Un altro vantaggio delle code di file è che è possibile tenere traccia dello stato di avanzamento dell'installazione nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="af774-115">Another advantage of file queues is that you can track the progress of the installation as a whole.</span></span> <span data-ttu-id="af774-116">Quando si installa la sezione per sezione da un file INF, gli indicatori di stato, ad esempio le barre di stato, possono tenere traccia solo della sezione INF corrente.</span><span class="sxs-lookup"><span data-stu-id="af774-116">When installing section-by-section from an INF file, progress indicators such as progress bars can track only the current INF section.</span></span> <span data-ttu-id="af774-117">Quando viene installata la sezione successiva, l'indicatore di stato viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="af774-117">When the next section is installed, the progress bar starts over.</span></span> <span data-ttu-id="af774-118">Con una coda, il numero totale di file da elaborare durante l'intera installazione è noto prima del commit della coda, quindi è possibile generare un indicatore di stato per tenere traccia dell'intera installazione.</span><span class="sxs-lookup"><span data-stu-id="af774-118">With a queue, the total number of files to be processed during the entire installation is known before the queue is committed, and thus, a progress bar can be generated to track the entire installation.</span></span>

<span data-ttu-id="af774-119">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="af774-119">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="af774-120">Ordine di impegno della coda</span><span class="sxs-lookup"><span data-stu-id="af774-120">Order of Queue Commitment</span></span>](order-of-queue-commitment.md)
-   [<span data-ttu-id="af774-121">Notifiche della coda</span><span class="sxs-lookup"><span data-stu-id="af774-121">Queue Notifications</span></span>](queue-notifications.md)

 

 



