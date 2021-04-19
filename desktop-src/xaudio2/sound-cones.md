---
description: Modello che descrive la sonorità del suono orientato.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Coni audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317844"
---
# <a name="sound-cones"></a><span data-ttu-id="27d94-103">Coni audio</span><span class="sxs-lookup"><span data-stu-id="27d94-103">Sound Cones</span></span>

<span data-ttu-id="27d94-104">Modello che descrive la sonorità del suono orientato.</span><span class="sxs-lookup"><span data-stu-id="27d94-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="27d94-105">Un suono senza orientamento ha la stessa ampiezza a una distanza specificata in tutte le direzioni.</span><span class="sxs-lookup"><span data-stu-id="27d94-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="27d94-106">Un suono con orientamento è più forte nella direzione dell'orientamento.</span><span class="sxs-lookup"><span data-stu-id="27d94-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="27d94-107">Il modello che descrive la sonorità del suono orientato è detto cono acustico.</span><span class="sxs-lookup"><span data-stu-id="27d94-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="27d94-108">I coni acustici sono costituiti da un cono interno (o interno) e da un cono esterno (o esterno).</span><span class="sxs-lookup"><span data-stu-id="27d94-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="27d94-109">L'angolo del cono esterno deve essere sempre uguale o maggiore dell'angolo del cono interno.</span><span class="sxs-lookup"><span data-stu-id="27d94-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="27d94-110">In qualsiasi angolo all'interno del cono interno, il volume del suono viene impostato sul volume del cono interno.</span><span class="sxs-lookup"><span data-stu-id="27d94-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="27d94-111">In questo modo viene preso in considerazione il volume di base del buffer, la distanza dal listener, l'orientamento del listener se il listener ha un cono e così via.</span><span class="sxs-lookup"><span data-stu-id="27d94-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="27d94-112">In qualsiasi angolo esterno al cono esterno, il volume normale viene attenuato da un fattore impostato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27d94-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="27d94-113">Il livello del volume del cono esterno è espresso come scaler di ampiezza lineare: 1,0 f non rappresenta alcuna attenuazione applicata al segnale originale, 0,5 f denota un'attenuazione di 6 dB e 0,0 f risultano silenziosi.</span><span class="sxs-lookup"><span data-stu-id="27d94-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="27d94-114">È consentita anche l'amplificazione (volume > 1,0 f) e non è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="27d94-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="27d94-115">L'intervallo di volumi validi è effettivamente 0,0 f a 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="27d94-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="27d94-116">Tra i coni interni ed esterni è presente una zona di transizione dal volume interno al volume esterno.</span><span class="sxs-lookup"><span data-stu-id="27d94-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="27d94-117">Il volume si avvicina al volume esterno del cono Man mano che aumenta l'angolo.</span><span class="sxs-lookup"><span data-stu-id="27d94-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="27d94-118">I coni possono influenzare parametri diversi dal volume.</span><span class="sxs-lookup"><span data-stu-id="27d94-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="27d94-119">Anche il livello di filtro di passaggio basso e di invio del riverbero potrebbe essere influenzato, rendendo la tecnica ancora più drammatica.</span><span class="sxs-lookup"><span data-stu-id="27d94-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="27d94-120">Ad esempio, con un cono sul listener, è possibile specificare che tutti i suoni dietro il listener ottengano un bit smorzato e abbiano un contenuto leggermente più alto per il rapporto tra reverbi diretti.</span><span class="sxs-lookup"><span data-stu-id="27d94-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="27d94-121">Che forniscono più segnali che il suono è dietro l'utente.</span><span class="sxs-lookup"><span data-stu-id="27d94-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="27d94-122">Ciò migliora il realismo.</span><span class="sxs-lookup"><span data-stu-id="27d94-122">This enhances realism.</span></span>

<span data-ttu-id="27d94-123">Nella figura seguente viene illustrato il concetto di coni audio.</span><span class="sxs-lookup"><span data-stu-id="27d94-123">The following illustration shows the concept of sound cones.</span></span>

![coni audio](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="27d94-125">La progettazione corretta dei coni audio può aggiungere effetti significativi all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27d94-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="27d94-126">Ad esempio, è possibile posizionare una sorgente audio al centro di una stanza, impostando l'orientamento verso una porta aperta in un corridoio.</span><span class="sxs-lookup"><span data-stu-id="27d94-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="27d94-127">Impostare quindi l'angolo del cono interno in modo che si estenda alla larghezza della porta, rendere il cono esterno a un bit più ampio e infine impostare il volume del cono esterno su impercettibile.</span><span class="sxs-lookup"><span data-stu-id="27d94-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="27d94-128">Un listener che si muove lungo il corridoio inizierà a udire il suono solo quando è vicino alla porta.</span><span class="sxs-lookup"><span data-stu-id="27d94-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="27d94-129">Il suono sarà più forte quando il listener passa davanti alla porta aperta.</span><span class="sxs-lookup"><span data-stu-id="27d94-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27d94-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27d94-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27d94-131">Concetti audio comuni</span><span class="sxs-lookup"><span data-stu-id="27d94-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="27d94-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="27d94-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="27d94-133">**\_Cono X3DAUDIO**</span><span class="sxs-lookup"><span data-stu-id="27d94-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



