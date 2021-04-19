---
description: Architettura DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Architettura DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303746"
---
# <a name="dmo-architecture"></a><span data-ttu-id="e9c1a-103">Architettura DMO</span><span class="sxs-lookup"><span data-stu-id="e9c1a-103">DMO Architecture</span></span>

<span data-ttu-id="e9c1a-104">In questa sezione viene descritta l'architettura complessiva di un DMO.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="e9c1a-105">**Flussi**</span><span class="sxs-lookup"><span data-stu-id="e9c1a-105">**Streams**</span></span>

<span data-ttu-id="e9c1a-106">Un DMO è un oggetto che accetta input *m* e produce *n* output.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="e9c1a-107">Gli input e gli output sono detti *flussi*.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="e9c1a-108">Ogni DMO ha almeno un flusso.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="e9c1a-109">I flussi non sono oggetti; si fa semplicemente riferimento a DMO in base al numero di indice.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="e9c1a-110">Il numero di flussi viene corretto in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="e9c1a-111">**Tipi di supporto**</span><span class="sxs-lookup"><span data-stu-id="e9c1a-111">**Media Types**</span></span>

<span data-ttu-id="e9c1a-112">Tutti i dati vengono digitati utilizzando un *tipo di supporto*, che definisce come interpretare il contenuto dei dati.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="e9c1a-113">Ad esempio, il video RGB a 320 x 240 24 bit è un tipo; 44,1-kilohertz (kHz) audio PCM stereo a 16 bit è un altro tipo.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="e9c1a-114">I tipi di supporto vengono descritti utilizzando la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="e9c1a-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="e9c1a-115">Prima che il client possa elaborare i dati, deve impostare il tipo di supporto per ogni flusso nel DMO.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="e9c1a-116">In genere, un flusso può accettare un intervallo di tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="e9c1a-117">Alcuni DMOs supportano una più ampia gamma di tipi rispetto ad altri.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="e9c1a-118">Le interfacce DMO definiscono i metodi che consentono al client di individuare i tipi supportati.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="e9c1a-119">Ad esempio, un DMO potrebbe supportare video RGB con una profondità qualsiasi, mentre un altro potrebbe supportare solo RGB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="e9c1a-120">Inoltre, un DMO potrebbe essere limitato a determinate combinazioni di input e output.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="e9c1a-121">Se, ad esempio, il tipo di input è video a 16 bit, il flusso di output potrebbe richiedere la stessa profondità del bit.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="e9c1a-122">Il client può enumerare i tipi preferiti di ogni flusso e quindi testare combinazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="e9c1a-123">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="e9c1a-123">**Buffers**</span></span>

<span data-ttu-id="e9c1a-124">Nel modello DMO predefinito, il client alloca buffer di input e buffer di output distinti.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="e9c1a-125">Riempie i buffer di input con i dati e li recapita a DMO e DMO scrive nuovi dati nei buffer di output.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="e9c1a-126">Facoltativamente, un DMO può supportare l'elaborazione "sul posto".</span><span class="sxs-lookup"><span data-stu-id="e9c1a-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="e9c1a-127">Con l'elaborazione sul posto, DMO scrive l'output direttamente nel buffer di input, sui dati originali.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="e9c1a-128">L'elaborazione sul posto elimina la necessità di buffer distinti.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="e9c1a-129">D'altra parte, modifica i dati originali, che potrebbero non essere accettabili per alcune applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="e9c1a-130">Il modello di buffering predefinito (non sul posto) è supportato tramite l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="e9c1a-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="e9c1a-131">Tutti DMOs devono implementare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="e9c1a-132">Se un DMO supporta l'elaborazione sul posto, espone anche l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="e9c1a-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="e9c1a-133">Il client è responsabile dell'allocazione di tutti i buffer, sia di input che di output.</span><span class="sxs-lookup"><span data-stu-id="e9c1a-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9c1a-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9c1a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9c1a-135">Informazioni su DMOs</span><span class="sxs-lookup"><span data-stu-id="e9c1a-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



