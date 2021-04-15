---
description: Segmenti busta
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmenti busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521634"
---
# <a name="envelope-segments"></a><span data-ttu-id="bb90b-103">Segmenti busta</span><span class="sxs-lookup"><span data-stu-id="bb90b-103">Envelope Segments</span></span>

<span data-ttu-id="bb90b-104">Una curva di parametro è costituita da uno o più segmenti di busta, definiti mediante la struttura del [**\_ \_ segmento della busta MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) .</span><span class="sxs-lookup"><span data-stu-id="bb90b-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="bb90b-105">Questa struttura contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb90b-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="bb90b-106">Ora di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="bb90b-106">The start and end times.</span></span>
-   <span data-ttu-id="bb90b-107">Valori di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="bb90b-107">The starting and ending values.</span></span>
-   <span data-ttu-id="bb90b-108">Tipo di curva (lineare, quadrato e così via).</span><span class="sxs-lookup"><span data-stu-id="bb90b-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="bb90b-109">Flag facoltativi, descritti a breve.</span><span class="sxs-lookup"><span data-stu-id="bb90b-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="bb90b-110">Il client aggiunge segmenti di busta a un parametro chiamando il metodo [**IMediaParams:: AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) e passando una matrice di strutture **del \_ \_ segmento della busta MP** .</span><span class="sxs-lookup"><span data-stu-id="bb90b-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="bb90b-111">Il client deve ordinare i segmenti in ordine di tempo crescente prima di chiamare il metodo.</span><span class="sxs-lookup"><span data-stu-id="bb90b-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="bb90b-112">Quando DMO elabora i dati, è possibile immaginare il parametro in viaggio su ogni segmento della busta, ad esempio un'auto che conduce a una serie di colline.</span><span class="sxs-lookup"><span data-stu-id="bb90b-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="bb90b-113">Il metodo [**IMediaParams:: Getparat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) restituisce il valore più recente.</span><span class="sxs-lookup"><span data-stu-id="bb90b-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="bb90b-114">Due segmenti adiacenti possono avere un gap tra di essi.</span><span class="sxs-lookup"><span data-stu-id="bb90b-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="bb90b-115">Durante i gap, il parametro mantiene il valore precedente, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="bb90b-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="bb90b-116">Prima del primo segmento, il valore è il valore neutro.</span><span class="sxs-lookup"><span data-stu-id="bb90b-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="bb90b-117">Tra i segmenti, il valore è il valore finale del segmento precedente.</span><span class="sxs-lookup"><span data-stu-id="bb90b-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="bb90b-118">Dopo l'ultimo segmento, il valore rimane in corrispondenza del valore finale di tale segmento.</span><span class="sxs-lookup"><span data-stu-id="bb90b-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="bb90b-119">Se il client Scarica DMO, il valore viene ripristinato sul valore neutro.</span><span class="sxs-lookup"><span data-stu-id="bb90b-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="bb90b-120">È possibile modificare un segmento impostando uno dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb90b-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="bb90b-121">ENVLP di MPF \_ \_ Avvia \_ CURRENTVAL.</span><span class="sxs-lookup"><span data-stu-id="bb90b-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="bb90b-122">DMO usa il valore più recente del parametro come valore iniziale per il segmento.</span><span class="sxs-lookup"><span data-stu-id="bb90b-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="bb90b-123">Potrebbe trattarsi del valore neutro o del valore finale del segmento precedente.</span><span class="sxs-lookup"><span data-stu-id="bb90b-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="bb90b-124">DMO ignora il membro **valStart** della struttura del **segmento della \_ busta \_ MP** .</span><span class="sxs-lookup"><span data-stu-id="bb90b-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="bb90b-125">ENVLP di MPF \_ \_ Avvia \_ NEUTRALVAL.</span><span class="sxs-lookup"><span data-stu-id="bb90b-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="bb90b-126">DMO usa il valore neutro del parametro come valore iniziale per il segmento.</span><span class="sxs-lookup"><span data-stu-id="bb90b-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="bb90b-127">Ignora **valStart**.</span><span class="sxs-lookup"><span data-stu-id="bb90b-127">It ignores **valStart**.</span></span>

<span data-ttu-id="bb90b-128">È possibile considerare questi flag come il punto iniziale del segmento e spostarli verso l'alto o verso il basso, mentre il valore finale rimane fisso.</span><span class="sxs-lookup"><span data-stu-id="bb90b-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="bb90b-129">Il segmento si estenderà di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="bb90b-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb90b-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb90b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb90b-131">Parametri dei supporti</span><span class="sxs-lookup"><span data-stu-id="bb90b-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



