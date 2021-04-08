---
title: Indicatori
description: Indicatori
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marcatori
- Advanced Systems Format (ASF), marcatori
- ASF (formato avanzato dei sistemi), marcatori
- marcatori, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856893"
---
# <a name="markers"></a><span data-ttu-id="2ffe4-107">Indicatori</span><span class="sxs-lookup"><span data-stu-id="2ffe4-107">Markers</span></span>

<span data-ttu-id="2ffe4-108">I marcatori sono posizioni denominate nella sequenza temporale di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-108">Markers are named places on the timeline of an ASF file.</span></span> <span data-ttu-id="2ffe4-109">Ogni marcatore ha un nome e un'ora di presentazione assegnata.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-109">Each marker has a name and a presentation time that you assign.</span></span> <span data-ttu-id="2ffe4-110">È possibile specificare tutti i marcatori necessari per un file.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-110">You can specify as many markers as you need for a file.</span></span>

<span data-ttu-id="2ffe4-111">I marcatori sono utili per suddividere i file ASF di grandi dimensioni in parti logiche.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-111">Markers are useful for breaking up large ASF files in to logical pieces.</span></span> <span data-ttu-id="2ffe4-112">Un'applicazione che utilizza l'oggetto Reader per riprodurre file ASF può fornire all'utente la possibilità di passare dal marcatore al marcatore, semplificando la navigazione dei supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-112">An application that uses the reader object to play ASF files can provide the user with the option to skip from marker to marker, simplifying navigation of digital media.</span></span> <span data-ttu-id="2ffe4-113">Se, ad esempio, si crea un file ASF da una presentazione, è possibile inserire i marcatori nella sequenza temporale per ogni argomento principale descritto.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-113">For example, if you are making an ASF file out of a presentation, you can put markers in the timeline for each major topic that is discussed.</span></span> <span data-ttu-id="2ffe4-114">Al momento della riproduzione, anziché ottenere una sequenza temporale molto estesa e dover indovinare la posizione in cui eseguire la ricerca, un utente può semplicemente selezionare un argomento da un elenco e passare direttamente alla parte pertinente del file.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-114">On playback, instead of getting one long timeline and having to guess at the location to seek to, a user can simply pick a topic from a list and go right to the pertinent portion of the file.</span></span>

<span data-ttu-id="2ffe4-115">I marcatori vengono modificati dall'oggetto dell'editor di metadati.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-115">Markers are manipulated by the metadata editor object.</span></span> <span data-ttu-id="2ffe4-116">È possibile aggiungere, rimuovere e visualizzare i marcatori in un file in qualsiasi momento dopo la scrittura del file.</span><span class="sxs-lookup"><span data-stu-id="2ffe4-116">You can add, remove, and view the markers in a file at any time after the file has been written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ffe4-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ffe4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ffe4-118">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="2ffe4-118">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="2ffe4-119">**Per cercare i marcatori**</span><span class="sxs-lookup"><span data-stu-id="2ffe4-119">**To Seek to Markers**</span></span>](to-seek-to-markers.md)
</dt> <dt>

[<span data-ttu-id="2ffe4-120">**Uso dei marcatori**</span><span class="sxs-lookup"><span data-stu-id="2ffe4-120">**Using Markers**</span></span>](using-markers.md)
</dt> </dl>

 

 




