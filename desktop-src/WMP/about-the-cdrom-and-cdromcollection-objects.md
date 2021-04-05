---
title: Informazioni sugli oggetti cdrom e cdromcollection
description: Informazioni sugli oggetti cdrom e cdromcollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player, oggetto cdrom
- Modello a oggetti di Windows Media Player, oggetto cdrom
- modello a oggetti, oggetto cdrom
- Controllo ActiveX Windows Media Player, oggetto cdrom
- Controllo ActiveX, oggetto cdrom
- Controllo ActiveX Windows Media Player Mobile, oggetto cdrom
- Windows Media Player Mobile, oggetto cdrom
- Oggetto cdrom
- Windows Media Player, oggetto cdromcollection
- Modello a oggetti di Windows Media Player, oggetto cdromcollection
- modello a oggetti, oggetto cdromcollection
- Controllo ActiveX Windows Media Player, oggetto cdromcollection
- Controllo ActiveX, oggetto cdromcollection
- Controllo ActiveX Windows Media Player Mobile, oggetto cdromcollection
- Oggetto Windows Media Player Mobile, cdromcollection
- Oggetto cdromcollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711401"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="af707-119">Informazioni sugli oggetti cdrom e cdromcollection</span><span class="sxs-lookup"><span data-stu-id="af707-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="af707-120">Gli oggetti **CDROM** e **cdromcollection** governano l'interfaccia per le unità CD del computer per la lettura e la riproduzione di CDS.</span><span class="sxs-lookup"><span data-stu-id="af707-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="af707-121">È possibile accedere all'oggetto **cdromcollection** solo tramite la proprietà **cdromcollection** dell'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="af707-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="af707-122">La proprietà **cdromcollection** restituisce l'oggetto **cdromcollection** .</span><span class="sxs-lookup"><span data-stu-id="af707-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="af707-123">È possibile accedere alle proprietà dell'oggetto **cdromcollection** solo dopo averlo creato.</span><span class="sxs-lookup"><span data-stu-id="af707-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="af707-124">Ad esempio, per usare la proprietà **count** , è necessario usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="af707-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="af707-125">È possibile accedere all'oggetto **CDROM** solo tramite l'oggetto **cdromcollection** .</span><span class="sxs-lookup"><span data-stu-id="af707-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="af707-126">Ad esempio, per estrarre il CD utilizzando il metodo **eject** , è necessario innanzitutto creare l'oggetto raccolta e quindi un elemento nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="af707-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="af707-127">Per estrarre il CD, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="af707-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="af707-128">In entrambi i casi, si crea prima l'oggetto raccolta (**cdromcollection**) e quindi si recupera un oggetto specifico della raccolta.</span><span class="sxs-lookup"><span data-stu-id="af707-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="af707-129">L'oggetto è il primo elemento della raccolta, **Item**(0), che corrisponde alla prima unità CD.</span><span class="sxs-lookup"><span data-stu-id="af707-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="af707-130">Quindi, si chiama un metodo, **eject**, su tale elemento.</span><span class="sxs-lookup"><span data-stu-id="af707-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af707-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af707-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af707-132">**Oggetto cdrom**</span><span class="sxs-lookup"><span data-stu-id="af707-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="af707-133">**Oggetto cdromcollection**</span><span class="sxs-lookup"><span data-stu-id="af707-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="af707-134">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="af707-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




