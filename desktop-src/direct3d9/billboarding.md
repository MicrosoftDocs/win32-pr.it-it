---
description: Quando si creano scene 3D, un'applicazione può a volte ottenere vantaggi in termini di prestazioni tramite il rendering di oggetti 2D in modo da renderli apparentemente oggetti 3D. Si tratta dell'idea fondamentale dietro la tecnica di affissione.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Billboard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305309"
---
# <a name="billboarding-direct3d-9"></a><span data-ttu-id="11aa4-104">Billboard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="11aa4-104">Billboarding (Direct3D 9)</span></span>

<span data-ttu-id="11aa4-105">Quando si creano scene 3D, un'applicazione può a volte ottenere vantaggi in termini di prestazioni tramite il rendering di oggetti 2D in modo da renderli apparentemente oggetti 3D.</span><span class="sxs-lookup"><span data-stu-id="11aa4-105">When creating 3D scenes, an application can sometimes gain performance advantages by rendering 2D objects in a way that makes them appear to be 3D objects.</span></span> <span data-ttu-id="11aa4-106">Si tratta dell'idea fondamentale dietro la tecnica di affissione.</span><span class="sxs-lookup"><span data-stu-id="11aa4-106">This is the basic idea behind the technique of billboarding.</span></span>

<span data-ttu-id="11aa4-107">Un cartellone nel normale senso della parola è un segno lungo una carreggiata.</span><span class="sxs-lookup"><span data-stu-id="11aa4-107">A billboard in the normal sense of the word is a sign along a roadway.</span></span> <span data-ttu-id="11aa4-108">Le applicazioni Microsoft Direct3D possono creare ed eseguire il rendering di questo tipo di Billboard definendo un solido rettangolare e applicando una trama a essa.</span><span class="sxs-lookup"><span data-stu-id="11aa4-108">Microsoft Direct3D applications can create and render this type of billboard by defining a rectangular solid and applying a texture to it.</span></span> <span data-ttu-id="11aa4-109">Il tabellone nel senso più specializzato della grafica 3D è un'estensione di questo.</span><span class="sxs-lookup"><span data-stu-id="11aa4-109">Billboarding in the more specialized sense of 3D graphics is an extension of this.</span></span> <span data-ttu-id="11aa4-110">L'obiettivo consiste nel creare oggetti 2D che risultino 3D.</span><span class="sxs-lookup"><span data-stu-id="11aa4-110">The goal is to make 2D objects appear to be 3D.</span></span> <span data-ttu-id="11aa4-111">La tecnica consiste nell'applicare una trama che contiene l'immagine dell'oggetto a una primitiva rettangolare.</span><span class="sxs-lookup"><span data-stu-id="11aa4-111">The technique is to apply a texture that contains the object's image to a rectangular primitive.</span></span> <span data-ttu-id="11aa4-112">La primitiva viene ruotata in modo che faccia sempre fronte all'utente.</span><span class="sxs-lookup"><span data-stu-id="11aa4-112">The primitive is rotated so that it always faces the user.</span></span> <span data-ttu-id="11aa4-113">Non è importante se l'immagine dell'oggetto non è rettangolare.</span><span class="sxs-lookup"><span data-stu-id="11aa4-113">It doesn't matter if the object's image is not rectangular.</span></span> <span data-ttu-id="11aa4-114">È possibile rendere trasparente parti del cartellone, quindi le parti dell'immagine di Billboard che non si vuole visualizzare non sono visibili.</span><span class="sxs-lookup"><span data-stu-id="11aa4-114">Portions of the billboard can be made transparent, so the parts of the billboard image that you don't want seen are not visible.</span></span>

<span data-ttu-id="11aa4-115">Molti giochi impiegano il tabellone per gli sprite animati.</span><span class="sxs-lookup"><span data-stu-id="11aa4-115">Many games employ billboarding for animated sprites.</span></span> <span data-ttu-id="11aa4-116">Ad esempio, quando l'utente si muove in un labirinto 3D, può visualizzare le armi o i ricompense che possono essere prelevati.</span><span class="sxs-lookup"><span data-stu-id="11aa4-116">For instance, when the user is moving through a 3D maze, he or she may see weapons or rewards that can be picked up.</span></span> <span data-ttu-id="11aa4-117">Si tratta in genere di immagini 2D con trama su una primitiva rettangolare.</span><span class="sxs-lookup"><span data-stu-id="11aa4-117">These are typically 2D images textured on a rectangular primitive.</span></span> <span data-ttu-id="11aa4-118">Il tabellone viene spesso usato nei giochi per il rendering di immagini di alberi, cespugli e cloud.</span><span class="sxs-lookup"><span data-stu-id="11aa4-118">Billboarding is often used in games to render images of trees, bushes, and clouds.</span></span>

<span data-ttu-id="11aa4-119">Quando un'immagine viene applicata a un tabellone, la primitiva rettangolare deve prima essere ruotata in modo che l'immagine risultante faccia fronte all'utente.</span><span class="sxs-lookup"><span data-stu-id="11aa4-119">When an image is applied to a billboard, the rectangular primitive must first be rotated so that the resulting image faces the user.</span></span> <span data-ttu-id="11aa4-120">L'applicazione deve quindi tradurla in posizione.</span><span class="sxs-lookup"><span data-stu-id="11aa4-120">Your application must then translate it into position.</span></span> <span data-ttu-id="11aa4-121">L'applicazione può quindi applicare una trama alla primitiva.</span><span class="sxs-lookup"><span data-stu-id="11aa4-121">The application can then apply a texture to the primitive.</span></span>

<span data-ttu-id="11aa4-122">Il tabellone funziona meglio per gli oggetti simmetrici, in particolare gli oggetti simmetrici lungo l'asse verticale.</span><span class="sxs-lookup"><span data-stu-id="11aa4-122">Billboarding works best for symmetrical objects, especially objects that are symmetrical along the vertical axis.</span></span> <span data-ttu-id="11aa4-123">Richiede inoltre che l'altitudine del punto di vista non aumenti eccessivamente.</span><span class="sxs-lookup"><span data-stu-id="11aa4-123">It also requires that the altitude of the viewpoint doesn't increase too much.</span></span> <span data-ttu-id="11aa4-124">Se l'utente è autorizzato a visualizzare il tabellone indicato sopra, diventa immediatamente evidente che l'oggetto è 2D anziché 3D.</span><span class="sxs-lookup"><span data-stu-id="11aa4-124">If the user is allowed to view the billboarded from above, it becomes readily apparent that the object is 2D rather than 3D.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11aa4-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11aa4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11aa4-126">Esempi di Alpha</span><span class="sxs-lookup"><span data-stu-id="11aa4-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



