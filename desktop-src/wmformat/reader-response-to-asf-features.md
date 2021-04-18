---
title: Risposta del lettore alle funzionalità ASF
description: Risposta del lettore alle funzionalità ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media Format SDK, risposte del lettore alle funzionalità ASF
- ASF (Advanced Systems Format), risposte del lettore alle funzionalità
- ASF (formato avanzato dei sistemi), risposte del lettore alle funzionalità
- risposte del lettore alle funzionalità ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298231"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="78f7a-107">Risposta del lettore alle funzionalità ASF</span><span class="sxs-lookup"><span data-stu-id="78f7a-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="78f7a-108">La maggior parte delle funzionalità speciali dei file ASF può essere configurata nei file per interagire con le applicazioni di riproduzione personalizzate progettate per gestirle.</span><span class="sxs-lookup"><span data-stu-id="78f7a-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="78f7a-109">Tuttavia, alcune funzionalità di includono il supporto incorporato nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="78f7a-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="78f7a-110">L'oggetto Reader selezionerà automaticamente i flussi dai set che si escludono a vicenda in base alla velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="78f7a-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="78f7a-111">Questo caso speciale è noto come velocità in bit multipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="78f7a-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="78f7a-112">Il flusso selezionato dal lettore è basato sulla velocità in bit del flusso.</span><span class="sxs-lookup"><span data-stu-id="78f7a-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="78f7a-113">Il numero del flusso e l'ordine in cui è stato aggiunto all'oggetto di esclusione reciproca sono irrilevanti per la selezione automatica.</span><span class="sxs-lookup"><span data-stu-id="78f7a-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="78f7a-114">Se un file include più di un set di flussi che si escludono a vicenda per velocità in bit, il lettore selezionerà i flussi in base al calcolo del migliore uso della larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="78f7a-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="78f7a-115">L'esclusione reciproca basata sulla lingua viene impostata usando un'impostazione di output, prima della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="78f7a-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="78f7a-116">Se si combinano sia la lingua che l'esclusione reciproca basata sulla velocità in bit, è necessario raggruppare i flussi che si escludono reciprocamente basati sulla velocità in bit per lingua e quindi rendere i gruppi che si escludono a vicenda in base alla lingua.</span><span class="sxs-lookup"><span data-stu-id="78f7a-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="78f7a-117">Il lettore controllerà innanzitutto la lingua e quindi determina la velocità in bit da usare.</span><span class="sxs-lookup"><span data-stu-id="78f7a-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="78f7a-118">La definizione delle priorità del flusso viene impostata tramite una matrice di record.</span><span class="sxs-lookup"><span data-stu-id="78f7a-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="78f7a-119">I record nella matrice sono in ordine decrescente di priorità.</span><span class="sxs-lookup"><span data-stu-id="78f7a-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="78f7a-120">L'ultimo flusso della matrice è il primo che verrà eliminato dal reader.</span><span class="sxs-lookup"><span data-stu-id="78f7a-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78f7a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78f7a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78f7a-122">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="78f7a-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="78f7a-123">**Esclusione reciproca**</span><span class="sxs-lookup"><span data-stu-id="78f7a-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="78f7a-124">**Assegnazione di priorità al flusso**</span><span class="sxs-lookup"><span data-stu-id="78f7a-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




