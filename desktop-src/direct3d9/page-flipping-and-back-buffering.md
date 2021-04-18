---
description: Il capovolgimento della pagina è fondamentale per il software multimediale, di animazione e di gioco; è analogo al modo in cui è possibile eseguire l'animazione con una carta da tastiera.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Capovolgimento della pagina e buffering indietro (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303844"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="39a60-103">Capovolgimento della pagina e buffering indietro (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="39a60-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="39a60-104">Il capovolgimento della pagina è fondamentale per il software multimediale, di animazione e di gioco; è analogo al modo in cui è possibile eseguire l'animazione con una carta da tastiera.</span><span class="sxs-lookup"><span data-stu-id="39a60-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="39a60-105">In ogni pagina, l'artista modifica leggermente la figura, in modo che, quando si scorre rapidamente tra i fogli, il disegno appaia animato.</span><span class="sxs-lookup"><span data-stu-id="39a60-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="39a60-106">Il capovolgimento della pagina nel software è simile a questo processo.</span><span class="sxs-lookup"><span data-stu-id="39a60-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="39a60-107">Direct3D implementa la funzionalità di capovolgimento della pagina tramite una catena di scambio, che è una proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39a60-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="39a60-108">Inizialmente, viene configurata una serie di buffer Direct3D che passano sullo schermo nel modo in cui il documento dell'artista passa alla pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="39a60-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="39a60-109">Il primo buffer viene definito buffer anteriore del colore.</span><span class="sxs-lookup"><span data-stu-id="39a60-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="39a60-110">I buffer sottostanti vengono richiamati buffer.</span><span class="sxs-lookup"><span data-stu-id="39a60-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="39a60-111">L'applicazione scrive in un buffer nascosto e quindi capovolge il buffer anteriore del colore in modo che il buffer nascosto venga visualizzato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="39a60-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="39a60-112">Mentre il sistema Visualizza l'immagine, il software sta scrivendo nuovamente in un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="39a60-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="39a60-113">Il processo continua fino a quando si sta aggiungendo un'animazione, consentendo di animare le immagini in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="39a60-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="39a60-114">Direct3D semplifica la configurazione degli schemi di capovolgimento della pagina, da un semplice schema con doppio buffer (un buffer anteriore a un colore con un buffer nascosto) a schemi più sofisticati con buffer back aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="39a60-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39a60-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39a60-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a60-116">Superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="39a60-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="39a60-117">Che cos'è una catena di scambio? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="39a60-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



