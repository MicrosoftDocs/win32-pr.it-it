---
title: Progettazione dell'interfaccia
description: Progettazione dell'interfaccia
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Interfacce utente di Windows Media Player Mobile, interfacce utente
- interfacce, interfacce utente
- creazione di interfacce, interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116889"
---
# <a name="designing-the-interface"></a><span data-ttu-id="099c0-106">Progettazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="099c0-106">Designing the Interface</span></span>

<span data-ttu-id="099c0-107">Una volta scelte le funzioni, è possibile progettare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="099c0-107">Once the functions have been chosen, the interface can be designed.</span></span> <span data-ttu-id="099c0-108">È stata scelta una semplice interfaccia per corrispondere alla funzionalità.</span><span class="sxs-lookup"><span data-stu-id="099c0-108">A simple interface was chosen to match the functionality.</span></span> <span data-ttu-id="099c0-109">I simboli per i controlli sono stati scelti dai controlli VCR standard.</span><span class="sxs-lookup"><span data-stu-id="099c0-109">Symbols for the controls were chosen from standard VCR controls.</span></span>

<span data-ttu-id="099c0-110">L'immagine seguente mostra l'aspetto dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="099c0-110">The following image shows what the interface will look like.</span></span>

![interfaccia di esempio](images/ceswmful.png)

-   <span data-ttu-id="099c0-112">**Pulsante come playpause o PlayPauseStop.**</span><span class="sxs-lookup"><span data-stu-id="099c0-112">**PlayPause or PlayPauseStop button.**</span></span> <span data-ttu-id="099c0-113">L'utente sta toccando più questo, quindi è possibile considerare un pulsante più grande.</span><span class="sxs-lookup"><span data-stu-id="099c0-113">The user will be tapping this the most, so you might consider a larger button.</span></span> <span data-ttu-id="099c0-114">L'angolo superiore destro costituisce una buona posizione che l'utente può trovare rapidamente.</span><span class="sxs-lookup"><span data-stu-id="099c0-114">The upper-right corner makes a good location that the user can find quickly.</span></span> <span data-ttu-id="099c0-115">Viene usata una freccia a tinta unita per indicare la riproduzione e due barre verticali (non mostrate qui) per indicare la pausa.</span><span class="sxs-lookup"><span data-stu-id="099c0-115">A solid arrow is used to indicate play and two vertical bars (not shown here) will be used to indicate pause.</span></span>
    > [!Note]  
    > <span data-ttu-id="099c0-116">Il pulsante PlayPauseStop può essere usato solo quando si crea un'interfaccia per Windows Media Player 10 mobile o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="099c0-116">The PlayPauseStop button can only be used when creating a skin for Windows Media Player 10 Mobile or later.</span></span>

     

-   <span data-ttu-id="099c0-117">**Pulsante Arresta.**</span><span class="sxs-lookup"><span data-stu-id="099c0-117">**Stop button.**</span></span> <span data-ttu-id="099c0-118">Per facilitarne l'individuazione, è posizionata nell'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="099c0-118">To make this easy to find, it is placed at the upper-left corner.</span></span> <span data-ttu-id="099c0-119">Un quadrato viene usato per indicare l'arresto.</span><span class="sxs-lookup"><span data-stu-id="099c0-119">A square is used to indicate stop.</span></span> <span data-ttu-id="099c0-120">Se si sta creando un'interfaccia per Windows Media Player 10 mobile o versione successiva, il pulsante PlayPauseStop fornisce già questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="099c0-120">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop button already provides this functionality.</span></span>
-   <span data-ttu-id="099c0-121">**Pulsanti avanti e indietro.**</span><span class="sxs-lookup"><span data-stu-id="099c0-121">**Next and Prev buttons.**</span></span> <span data-ttu-id="099c0-122">Poiché questi non verranno usati con la stessa frequenza, verranno posizionati a sinistra.</span><span class="sxs-lookup"><span data-stu-id="099c0-122">Since these will not be used as often, they are placed on the left.</span></span> <span data-ttu-id="099c0-123">Il successivo è sopra il pulsante indietro, perché è più probabile che si desideri procedere in una playlist.</span><span class="sxs-lookup"><span data-stu-id="099c0-123">The Next is above the Prev button because people will more likely want to move forward in a playlist.</span></span> <span data-ttu-id="099c0-124">I simboli a doppia freccia vengono usati perché sono simili in funzione a un controllo di avanzamento rapido.</span><span class="sxs-lookup"><span data-stu-id="099c0-124">The double-arrow symbols are used because they are similar in function to a fast-forward control.</span></span>
-   <span data-ttu-id="099c0-125">**TrackBar del volume.**</span><span class="sxs-lookup"><span data-stu-id="099c0-125">**Volume trackbar.**</span></span> <span data-ttu-id="099c0-126">Questa posizione viene posizionata nella parte inferiore della schermata ed è una linea semplice con un pulsante Thumb.</span><span class="sxs-lookup"><span data-stu-id="099c0-126">This is placed at the bottom of the screen and is a simple line with a thumb button on top of it.</span></span>
-   <span data-ttu-id="099c0-127">**Casella di testo Marquee.**</span><span class="sxs-lookup"><span data-stu-id="099c0-127">**Marquee text box.**</span></span> <span data-ttu-id="099c0-128">Si trova sotto il pulsante come playpause o PlayPauseStop in modo che sia facile da vedere.</span><span class="sxs-lookup"><span data-stu-id="099c0-128">This is placed under the PlayPause or PlayPauseStop button so that it is easy to see.</span></span>

<span data-ttu-id="099c0-129">Si consiglia di disegnare questo primo e sperimentare la posizione di ogni elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="099c0-129">You may want to sketch this first and experiment with the placement of each user interface element.</span></span> <span data-ttu-id="099c0-130">Il progetto illustrato qui è stato scelto per semplicità e semplicità d'uso.</span><span class="sxs-lookup"><span data-stu-id="099c0-130">The design shown here was chosen for simplicity and ease of use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="099c0-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="099c0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="099c0-132">**Guida all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="099c0-132">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




