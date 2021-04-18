---
description: Uniscribe fornisce le API per il supporto della tipografia e per supportare la visualizzazione e la modifica del testo internazionale, incluse le complesse regole degli script Medio Oriente e asiatici.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Uso di Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319468"
---
# <a name="using-uniscribe"></a><span data-ttu-id="2b17b-103">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="2b17b-103">Using Uniscribe</span></span>

<span data-ttu-id="2b17b-104">Uniscribe fornisce le API per il supporto della tipografia e per supportare la visualizzazione e la modifica del testo internazionale, incluse le complesse regole degli script Medio Oriente e asiatici.</span><span class="sxs-lookup"><span data-stu-id="2b17b-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="2b17b-105">Uniscribe fornisce routine di basso livello per la gestione di testo completamente formattato e una semplice API ScriptString impostata per il testo non formattato.</span><span class="sxs-lookup"><span data-stu-id="2b17b-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="2b17b-106">Con Uniscribe, le applicazioni devono solo gestire un archivio di backup di codici carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b17b-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="2b17b-107">Per tenere traccia dell'ordine dei caratteri, le applicazioni di layout del testo non devono gestire altri buffer o tabelle di mapping.</span><span class="sxs-lookup"><span data-stu-id="2b17b-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="2b17b-108">Ogni applicazione deve solo archiviare e gestire l'ordine in cui i caratteri vengono immessi dall'utente, ovvero lo stesso ordine logico definito da Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b17b-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="2b17b-109">L'archivio di backup non viene mai modificato in seguito a operazioni di layout.</span><span class="sxs-lookup"><span data-stu-id="2b17b-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="2b17b-110">Uniscribe mantiene un indice dai cluster riordinati ai limiti dei caratteri originali passati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b17b-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="2b17b-111">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b17b-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="2b17b-112">**Shaping**</span><span class="sxs-lookup"><span data-stu-id="2b17b-112">**Shaping**</span></span>

-   [<span data-ttu-id="2b17b-113">Determinare se uno script richiede la definizione del glifo</span><span class="sxs-lookup"><span data-stu-id="2b17b-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="2b17b-114">Uso di shaping Engine</span><span class="sxs-lookup"><span data-stu-id="2b17b-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="2b17b-115">**Altre elaborazioni**</span><span class="sxs-lookup"><span data-stu-id="2b17b-115">**Other Processing**</span></span>

-   [<span data-ttu-id="2b17b-116">Memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="2b17b-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="2b17b-117">Visualizzazione di testo con Uniscribe</span><span class="sxs-lookup"><span data-stu-id="2b17b-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="2b17b-118">Elaborazione di script complessi</span><span class="sxs-lookup"><span data-stu-id="2b17b-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="2b17b-119">Uso del fallback dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="2b17b-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="2b17b-120">Uso delle funzioni ScriptString</span><span class="sxs-lookup"><span data-stu-id="2b17b-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="2b17b-121">**Cursore**</span><span class="sxs-lookup"><span data-stu-id="2b17b-121">**Caret**</span></span>

-   [<span data-ttu-id="2b17b-122">Visualizzazione del cursore nelle stringhe bidirezionali</span><span class="sxs-lookup"><span data-stu-id="2b17b-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="2b17b-123">Gestione della selezione host e hit testing del cursore</span><span class="sxs-lookup"><span data-stu-id="2b17b-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="2b17b-124">Conversione dell'offset X del mouse nella posizione del punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="2b17b-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="2b17b-125">**Parole e cluster di caratteri**</span><span class="sxs-lookup"><span data-stu-id="2b17b-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="2b17b-126">Uso di cluster di caratteri</span><span class="sxs-lookup"><span data-stu-id="2b17b-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="2b17b-127">Uso di punti di interruzioni di Word</span><span class="sxs-lookup"><span data-stu-id="2b17b-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="2b17b-128">Utilizzo delle relazioni tra le posizioni del punto di inserimento, i punti di giustificazione e i cluster</span><span class="sxs-lookup"><span data-stu-id="2b17b-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



