---
title: Novità (controlli Windows)
description: In questo argomento vengono descritte le differenze di supporto per gli stili di visualizzazione e di visualizzazione tra Windows 8 e le versioni precedenti di Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474819"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="6b789-103">Novità (controlli Windows)</span><span class="sxs-lookup"><span data-stu-id="6b789-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="6b789-104">In questo argomento vengono descritte le differenze di supporto per gli stili di visualizzazione e di visualizzazione tra Windows 8 e le versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="6b789-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="6b789-105">Tramite Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b789-105">Through Windows 7</span></span>

<span data-ttu-id="6b789-106">Grazie a Windows 7, gli stili di visualizzazione sono attivati per impostazione predefinita, ma l'utente può disattivarli selezionando il tema classico di Windows o disattivando il servizio temi.</span><span class="sxs-lookup"><span data-stu-id="6b789-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="6b789-107">Quando gli stili di visualizzazione sono spenti, tutte le interfacce utente ottengono l'aspetto classico e la maggior parte delle API degli stili di visualizzazione non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="6b789-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="6b789-108">La modalità di visualizzazione degli stili di visualizzazione è stata mantenuta attraverso Windows 7 per supportare i diversi temi a contrasto elevato, oltre al tema Windows classico.</span><span class="sxs-lookup"><span data-stu-id="6b789-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="6b789-109">Se si desidera supportare sia gli stili visivi che i temi a contrasto elevato nella stessa applicazione, in genere è necessario mantenere due percorsi di codice distinti per il rendering dei controlli.</span><span class="sxs-lookup"><span data-stu-id="6b789-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="6b789-110">Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="6b789-110">Windows 8 and Later</span></span>

<span data-ttu-id="6b789-111">In Windows 8 gli stili visivi non possono essere disattivati tramite la pagina **personalizzazione** delle **impostazioni del PC** oppure disattivando il servizio temi.</span><span class="sxs-lookup"><span data-stu-id="6b789-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="6b789-112">La modalità classica di Windows non esiste più e la modalità a contrasto elevato è stata modificata per funzionare con gli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6b789-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="6b789-113">A causa di queste modifiche, le applicazioni destinate solo a Windows 8 non necessitano più di due percorsi di codice distinti per supportare gli stili visivi e i temi a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="6b789-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="6b789-114">Gli stili di visualizzazione in Windows 8 includono il supporto per la compatibilità con le versioni precedenti di Windows classico.</span><span class="sxs-lookup"><span data-stu-id="6b789-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="6b789-115">Qualsiasi codice di rendering dell'interfaccia utente che funziona nelle versioni precedenti continuerà a funzionare in Windows 8 senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="6b789-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="6b789-116">In Windows 8, se si desidera che l'applicazione supporti i temi a contrasto elevato basati sugli stili di visualizzazione, è necessario includere il GUID di Windows 8 nella sezione compatibilità del manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6b789-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="6b789-117">In caso contrario, il sistema presuppone che l'applicazione sia progettata per una versione precedente ed esegua il rendering dell'area client simulando i temi classici a contrasto elevato di Windows.</span><span class="sxs-lookup"><span data-stu-id="6b789-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="6b789-118">Per ulteriori informazioni, vedere [supporto di contrasto elevato temi](supporting-high-contrast-themes.md).</span><span class="sxs-lookup"><span data-stu-id="6b789-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="6b789-119">Come nelle versioni precedenti, Windows 8 supporta sia la versione 5 che la versione 6 dei controlli comuni, con la versione 5 predefinita.</span><span class="sxs-lookup"><span data-stu-id="6b789-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="6b789-120">Poiché solo la versione 6 supporta gli stili di visualizzazione, è necessario specificare la versione 6 nel manifesto dell'applicazione se si desidera applicare gli stili di visualizzazione ai controlli comuni nell'area client dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6b789-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="6b789-121">Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6b789-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b789-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b789-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b789-123">Abilitazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="6b789-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="6b789-124">Supporto di Contrasto elevato temi</span><span class="sxs-lookup"><span data-stu-id="6b789-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="6b789-125">Stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="6b789-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="6b789-126">Panoramica degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="6b789-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




