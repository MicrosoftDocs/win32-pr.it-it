---
title: Informazioni sull'oggetto DVD
description: Informazioni sull'oggetto DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player, oggetto DVD
- Modello a oggetti di Windows Media Player, oggetto DVD
- modello a oggetti, oggetto DVD
- Controllo ActiveX Windows Media Player, oggetto DVD
- Controllo ActiveX, oggetto DVD
- Controllo ActiveX Windows Media Player Mobile, oggetto DVD
- Windows Media Player Mobile, oggetto DVD
- Oggetto DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328524"
---
# <a name="about-the-dvd-object"></a><span data-ttu-id="4b16f-111">Informazioni sull'oggetto DVD</span><span class="sxs-lookup"><span data-stu-id="4b16f-111">About the DVD Object</span></span>

<span data-ttu-id="4b16f-112">L'oggetto **DVD** aggiunge funzionalità specifiche dei supporti DVD.</span><span class="sxs-lookup"><span data-stu-id="4b16f-112">The **DVD** object adds functionality specific to DVD media.</span></span> <span data-ttu-id="4b16f-113">In generale, i supporti DVD sono trattati come altri supporti digitali in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4b16f-113">In a general sense, DVD media is treated just like other digital media in Windows Media Player.</span></span> <span data-ttu-id="4b16f-114">Ad esempio, le unità DVD vengono enumerate usando l'oggetto **cdromcollection** e i titoli e i capitoli dei DVD vengono modificati usando oggetti della **playlist** e oggetti **multimediali** .</span><span class="sxs-lookup"><span data-stu-id="4b16f-114">For instance, DVD drives are enumerated using the **CdromCollection** object and DVD titles and chapters are manipulated using **Playlist** objects and **Media** objects.</span></span> <span data-ttu-id="4b16f-115">Alcune funzionalità sono tuttavia specifiche del DVD e l'oggetto **DVD** lo fornisce.</span><span class="sxs-lookup"><span data-stu-id="4b16f-115">Some functionality is DVD-specific, however, and the **DVD** object provides this.</span></span> <span data-ttu-id="4b16f-116">Ad esempio, il DVD ha un concetto denominato dominio.</span><span class="sxs-lookup"><span data-stu-id="4b16f-116">For example, DVD has a concept called domain.</span></span> <span data-ttu-id="4b16f-117">Per recuperare il dominio corrente per i supporti DVD, digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4b16f-117">To retrieve the current domain for DVD media, type the following:</span></span>


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a><span data-ttu-id="4b16f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b16f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b16f-119">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="4b16f-119">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="4b16f-120">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="4b16f-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




