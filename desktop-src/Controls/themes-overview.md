---
title: Stili di visualizzazione
description: In questa sezione viene fornita una panoramica degli stili di visualizzazione e viene illustrato come configurare l'applicazione per utilizzarli.
ms.assetid: 9b135ccb-5e36-4657-b79c-689201047430
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bb1f8ff84f2c9f4d268ec8b50f8e7688519ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044553"
---
# <a name="visual-styles"></a><span data-ttu-id="56c71-103">Stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="56c71-103">Visual Styles</span></span>

## <a name="purpose"></a><span data-ttu-id="56c71-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="56c71-104">Purpose</span></span>

<span data-ttu-id="56c71-105">Gli *stili di visualizzazione* modificano l'aspetto dei controlli comuni in base al tema scelto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="56c71-105">*Visual styles* changes the appearance of common controls based on the theme chosen by the user.</span></span> <span data-ttu-id="56c71-106">Prima di Windows 8, è necessario configurare l'applicazione in modo specifico per l'utilizzo degli stili di visualizzazione. in caso contrario, i controlli comuni dell'applicazione vengono sempre sottoposti a rendering nello stile associato al tema classico di Windows, indipendentemente dal tema attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="56c71-106">Prior to Windows 8, you must specifically configure your application to use visual styles; otherwise, the application's common controls are always rendered in the style associated with the Windows Classic theme, regardless of the currently selected theme.</span></span> <span data-ttu-id="56c71-107">In Windows 8 gli stili visivi non possono essere disattivati, la modalità classica di Windows non esiste più e la modalità a contrasto elevato è stata modificata per funzionare con gli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="56c71-107">In Windows 8, visual styles can't be turned off, Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span>

<span data-ttu-id="56c71-108">In questa sezione viene fornita una panoramica degli stili di visualizzazione e viene illustrato come configurare l'applicazione per utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="56c71-108">This section provides an overview of visual styles and explains how to configure your application to use them.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="56c71-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="56c71-109">Developer audience</span></span>

<span data-ttu-id="56c71-110">Gli stili di visualizzazione sono progettati per essere utilizzati dagli sviluppatori C/C++ e dalle finestre di progettazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="56c71-110">Visual styles are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="56c71-111">In generale, gli sviluppatori necessitano di un livello moderato di informazioni sui concetti di programmazione dell'interfaccia utente, sulla programmazione dell'API Windows e su Unicode.</span><span class="sxs-lookup"><span data-stu-id="56c71-111">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="56c71-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="56c71-112">Run-time requirements</span></span>

<span data-ttu-id="56c71-113">Windows Vista e sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="56c71-113">Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="56c71-114">Gli stili di visualizzazione non sono supportati in modalità colore 256.</span><span class="sxs-lookup"><span data-stu-id="56c71-114">Visual Styles are not supported in 256-color mode.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="56c71-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="56c71-115">In this section</span></span>

-   [<span data-ttu-id="56c71-116">Novità</span><span class="sxs-lookup"><span data-stu-id="56c71-116">What's New</span></span>](what-s-new-for-windows-8.md)
-   [<span data-ttu-id="56c71-117">Panoramica degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="56c71-117">Visual Styles Overview</span></span>](visual-styles-overview.md)
-   [<span data-ttu-id="56c71-118">Abilitazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="56c71-118">Enabling Visual Styles</span></span>](cookbook-overview.md)
-   [<span data-ttu-id="56c71-119">Uso di stili di visualizzazione con controlli personalizzati e Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="56c71-119">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>](using-visual-styles.md)
-   [<span data-ttu-id="56c71-120">Supporto di Contrasto elevato temi</span><span class="sxs-lookup"><span data-stu-id="56c71-120">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
-   [<span data-ttu-id="56c71-121">Riferimenti agli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="56c71-121">Visual Styles Reference</span></span>](uxctl-ref.md)

## <a name="related-topics"></a><span data-ttu-id="56c71-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56c71-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56c71-123">Formato file tema</span><span class="sxs-lookup"><span data-stu-id="56c71-123">Theme File Format</span></span>](themesfileformat-overview.md)
</dt> <dt>

[<span data-ttu-id="56c71-124">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="56c71-124">Windows Controls</span></span>](window-controls.md)
</dt> </dl>

 

 




