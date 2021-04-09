---
title: Hit testing tocco
description: Negli argomenti di questa sezione viene fornita una panoramica del supporto per l'hit testing di tocco in Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- interazione dell'utente
- input
- indicatore di misura
- tocco
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/07/2020
ms.locfileid: "103857969"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="2827a-107">Hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="2827a-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="2827a-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="2827a-108">Purpose</span></span>

<span data-ttu-id="2827a-109">Negli argomenti di questa sezione viene fornita una panoramica del supporto per l'hit testing di tocco in Windows.</span><span class="sxs-lookup"><span data-stu-id="2827a-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="2827a-110">L'hit testing tocco consente di identificare una destinazione di input a seconda che l'area di contenuto di un elemento dell'interfaccia utente rientri nell'area di contatto o includa il punto di contatto.</span><span class="sxs-lookup"><span data-stu-id="2827a-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="2827a-111">L'hit testing tocco usa la geometria di contatto complessa per l'intera area di tocco anziché una singola coordinata x-y interpolata.</span><span class="sxs-lookup"><span data-stu-id="2827a-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="2827a-112">L'uso dell'intera geometria dei contatti migliora notevolmente la precisione e l'accuratezza quando si identifica la destinazione più probabile dell'input tocco.</span><span class="sxs-lookup"><span data-stu-id="2827a-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2827a-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2827a-113">In this section</span></span>

| <span data-ttu-id="2827a-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="2827a-114">Topic</span></span> | <span data-ttu-id="2827a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2827a-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="2827a-116">Riferimento all'hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="2827a-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="2827a-117">Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per gli [hit test di tocco](touch-hit-testing-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2827a-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="2827a-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="2827a-118">Developer audience</span></span>

<span data-ttu-id="2827a-119">Le API di hit testing touch sono progettate per gli sviluppatori che compilano Framework dell'interfaccia utente che forniscono un'esperienza utente ottimizzata per il tocco per le applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="2827a-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2827a-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2827a-120">Related topics</span></span>

[<span data-ttu-id="2827a-121">Interazione dell'utente</span><span class="sxs-lookup"><span data-stu-id="2827a-121">User Interaction</span></span>](../user-interaction.md)
