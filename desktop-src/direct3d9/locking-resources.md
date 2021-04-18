---
description: Il blocco di una risorsa significa concedere l'accesso alla CPU alla relativa archiviazione.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Blocco di risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304072"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="eb84c-103">Blocco di risorse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="eb84c-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="eb84c-104">Il blocco di una risorsa significa concedere l'accesso alla CPU alla relativa archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eb84c-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="eb84c-105">Per le risorse sono definite le seguenti opzioni di blocco:</span><span class="sxs-lookup"><span data-stu-id="eb84c-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="eb84c-106">Eliminazione di D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="eb84c-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="eb84c-107">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="eb84c-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="eb84c-108">Nosovrascrive D3DLOCK \_</span><span class="sxs-lookup"><span data-stu-id="eb84c-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="eb84c-109">\_NOSYSLOCK D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="eb84c-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="eb84c-110">D3DLOCK \_ nessun \_ \_ aggiornamento Dirty</span><span class="sxs-lookup"><span data-stu-id="eb84c-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="eb84c-111">Per informazioni dettagliate sui flag di blocco e sulla relativa correlazione con risorse specifiche, vedere le pagine di riferimento sui singoli metodi di blocco delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eb84c-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="eb84c-112">Gli sviluppatori di applicazioni devono tenere presente che i \_ flag D3DLOCK scarta, D3DLOCK \_ ReadOnly e D3DLOCK overwrite \_ sono solo hint.</span><span class="sxs-lookup"><span data-stu-id="eb84c-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="eb84c-113">Il tempo di esecuzione non verifica che le applicazioni stiano seguendo la funzionalità specificata da questi flag.</span><span class="sxs-lookup"><span data-stu-id="eb84c-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="eb84c-114">Un'applicazione che specifica D3DLOCK \_ ReadOnly ma quindi scrive nella risorsa dovrebbe prevedere risultati non definiti.</span><span class="sxs-lookup"><span data-stu-id="eb84c-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="eb84c-115">In generale, non è garantito il funzionamento dei flag di blocco, inclusi i flag di utilizzo del blocco, nelle versioni successive e può comportare una riduzione significativa delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="eb84c-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="eb84c-116">Un'operazione di blocco è seguita da un'operazione di sblocco.</span><span class="sxs-lookup"><span data-stu-id="eb84c-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="eb84c-117">Ad esempio, dopo aver bloccato una trama, l'applicazione cede in seguito l'accesso diretto alle trame bloccate, sbloccando tali trame.</span><span class="sxs-lookup"><span data-stu-id="eb84c-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="eb84c-118">Oltre alla concessione dell'accesso al processore, qualsiasi altra operazione che interessa tale risorsa viene serializzata per la durata di un blocco.</span><span class="sxs-lookup"><span data-stu-id="eb84c-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="eb84c-119">È consentito un solo blocco per una risorsa, anche per le aree non sovrapposte e non è possibile continuare con operazioni di accelerazione in una superficie mentre un'operazione di blocco è in attesa su tale superficie.</span><span class="sxs-lookup"><span data-stu-id="eb84c-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="eb84c-120">Ogni interfaccia di risorsa dispone di metodi per bloccare i buffer contenuti.</span><span class="sxs-lookup"><span data-stu-id="eb84c-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="eb84c-121">Ogni risorsa di trama può anche bloccare una parte secondaria di tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb84c-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="eb84c-122">le risorse 2D (superfici) consentono il blocco di sottorettangoli e le risorse del volume consentono il blocco di sottovolumi o caselle.</span><span class="sxs-lookup"><span data-stu-id="eb84c-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="eb84c-123">Ogni metodo Lock restituisce una struttura che contiene un puntatore all'archiviazione che supporta la risorsa e i valori che rappresentano le distanze tra le righe o i piani di dati, a seconda del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb84c-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="eb84c-124">Per informazioni dettagliate, vedere gli elenchi di metodi per le interfacce delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eb84c-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="eb84c-125">Il puntatore restituito punta sempre al byte superiore sinistro nelle aree secondarie bloccate.</span><span class="sxs-lookup"><span data-stu-id="eb84c-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="eb84c-126">Quando si utilizzano i buffer di indice e vertice, è possibile effettuare più chiamate di blocco; Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.</span><span class="sxs-lookup"><span data-stu-id="eb84c-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="eb84c-127">Il DXTn archivia i pixel nei blocchi 4x4 codificati e può essere bloccato solo sui limiti 4x4.</span><span class="sxs-lookup"><span data-stu-id="eb84c-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb84c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb84c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb84c-129">Risorse Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb84c-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



