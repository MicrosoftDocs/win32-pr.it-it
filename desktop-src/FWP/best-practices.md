---
title: Procedure consigliate (piattaforma filtro Windows)
description: Nell'elenco seguente sono contenute le procedure consigliate per lo sviluppo di applicazioni tramite l'API Windows Filtering Platform (WFP).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517289"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="2fef9-103">Procedure consigliate (piattaforma filtro Windows)</span><span class="sxs-lookup"><span data-stu-id="2fef9-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="2fef9-104">Nell'elenco seguente sono contenute le procedure consigliate per lo sviluppo di applicazioni tramite l'API Windows Filtering Platform (WFP).</span><span class="sxs-lookup"><span data-stu-id="2fef9-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="2fef9-105">Utilizzare sessioni dinamiche.</span><span class="sxs-lookup"><span data-stu-id="2fef9-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="2fef9-106">Molte applicazioni aggiungono oggetti Criteri di filtro all'avvio, quindi eliminano questi oggetti in fase di arresto.</span><span class="sxs-lookup"><span data-stu-id="2fef9-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="2fef9-107">Utilizzando una sessione dinamica, si garantisce che questi oggetti vengano eliminati anche in caso di arresto anomalo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2fef9-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="2fef9-108">Inoltre, la semplice chiusura dell'handle del motore alla fase di arresto è più efficiente rispetto all'esecuzione di singole chiamate per eliminare ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="2fef9-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="2fef9-109">Gestire correttamente i timeout delle transazioni o impostare la sessione **txnWaitTimeoutInMSec** su infinite per impedire i timeout.</span><span class="sxs-lookup"><span data-stu-id="2fef9-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="2fef9-110">Anche se non si utilizzano transazioni esplicite, la maggior parte delle chiamate viene comunque eseguita in una transazione implicita e pertanto può essere timeout.</span><span class="sxs-lookup"><span data-stu-id="2fef9-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="2fef9-111">Utilizzare transazioni esplicite per combinare operazioni di aggiunta o eliminazione correlate in una singola transazione.</span><span class="sxs-lookup"><span data-stu-id="2fef9-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="2fef9-112">Questa operazione è più efficiente e semplifica la pulizia dei risultati parziali nei percorsi degli errori.</span><span class="sxs-lookup"><span data-stu-id="2fef9-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="2fef9-113">Utilizzare stringhe compatibili con MUI.</span><span class="sxs-lookup"><span data-stu-id="2fef9-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="2fef9-114">Tutte le stringhe localizzabili sono archiviate in una struttura di dati comune: [**FWPM \_ Visualizza \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span><span class="sxs-lookup"><span data-stu-id="2fef9-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="2fef9-115">Le stringhe all'interno di questa struttura possono essere stringhe indirette del tipo supportato da [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="2fef9-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="2fef9-116">Prima che venga restituita una struttura **\_ \_ DATA0 per la visualizzazione FWPM** da parte delle funzioni, le stringhe indirette vengono risolte nella risorsa di stringa specificata utilizzando le impostazioni locali del chiamante.</span><span class="sxs-lookup"><span data-stu-id="2fef9-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="2fef9-117">Associare tutti gli oggetti a un provider.</span><span class="sxs-lookup"><span data-stu-id="2fef9-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="2fef9-118">Quando più provider sono installati nel sistema, ciò rende più semplice per gli strumenti di diagnostica determinare chi ha aggiunto.</span><span class="sxs-lookup"><span data-stu-id="2fef9-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="2fef9-119">Aggiungere filtri al sottolivello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2fef9-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="2fef9-120">Quando viene raggiunto un filtro di terminazione in un sottolivello, non vengono valutati altri filtri in quel sottolivello.</span><span class="sxs-lookup"><span data-stu-id="2fef9-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="2fef9-121">Pertanto, se si aggiungono i filtri allo stesso sottolivello di un altro provider, è possibile impedire che vengano richiamati i filtri di altri, ottenendo risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="2fef9-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="2fef9-122">Usare l'applicazione a livello di applicazione (ALE) anziché il filtro orientato ai pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2fef9-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="2fef9-123">Il filtro a livello di pacchetto è lento.</span><span class="sxs-lookup"><span data-stu-id="2fef9-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="2fef9-124">Filtrare gli errori ICMP e gli eventi RST prima che vengano generati.</span><span class="sxs-lookup"><span data-stu-id="2fef9-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="2fef9-125">Questa operazione è più efficiente che filtra questi eventi dopo che sono stati generati.</span><span class="sxs-lookup"><span data-stu-id="2fef9-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="2fef9-126">Eseguire l'ispezione di pacchetti a livello di dati Stream/datagramma anziché a livello di trasporto.</span><span class="sxs-lookup"><span data-stu-id="2fef9-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="2fef9-127">Questo vale per lo sviluppo di callout.</span><span class="sxs-lookup"><span data-stu-id="2fef9-127">This applies to developing callouts.</span></span> <span data-ttu-id="2fef9-128">Per ulteriori informazioni, vedere [considerazioni sulla programmazione dei driver di callout](/windows-hardware/drivers/network/callout-driver-programming-considerations) in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="2fef9-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="2fef9-129">Prendere in considerazione le implicazioni sulle prestazioni quando si usano filtri complessi.</span><span class="sxs-lookup"><span data-stu-id="2fef9-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="2fef9-130">A partire da Windows 7 e Windows Server 2008 R2, è possibile creare filtri con più condizioni che usano la stessa chiave di campo.</span><span class="sxs-lookup"><span data-stu-id="2fef9-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="2fef9-131">In questo modo è possibile creare criteri complessi con un minor numero di filtri.</span><span class="sxs-lookup"><span data-stu-id="2fef9-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="2fef9-132">Tuttavia, tali filtri complessi potrebbero comportare una riduzione delle prestazioni per la classificazione del motore di filtro WFP.</span><span class="sxs-lookup"><span data-stu-id="2fef9-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="2fef9-133">È necessario eseguire una valutazione per determinare se l'utilizzo di tali filtri causa un effetto negativo sulle prestazioni complessive della soluzione.</span><span class="sxs-lookup"><span data-stu-id="2fef9-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
