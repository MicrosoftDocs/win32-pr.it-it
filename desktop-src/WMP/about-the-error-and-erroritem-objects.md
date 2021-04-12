---
title: Informazioni sugli oggetti Error e ErrorItem
description: Informazioni sugli oggetti Error e ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, oggetto Error
- Modello a oggetti di Windows Media Player, oggetto Error
- modello a oggetti, oggetto Error
- Controllo ActiveX Windows Media Player, oggetto Error
- Controllo ActiveX, oggetto Error
- Controllo ActiveX Windows Media Player Mobile, oggetto Error
- Windows Media Player Mobile, oggetto Error
- Oggetto errore
- Windows Media Player, oggetto ErrorItem
- Modello a oggetti di Windows Media Player, oggetto ErrorItem
- modello a oggetti, oggetto ErrorItem
- Controllo ActiveX Windows Media Player, oggetto ErrorItem
- Controllo ActiveX, oggetto ErrorItem
- Controllo ActiveX Windows Media Player Mobile, oggetto ErrorItem
- Windows Media Player Mobile, oggetto ErrorItem
- Oggetto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330439"
---
# <a name="about-the-error-and-erroritem-objects"></a><span data-ttu-id="e4c39-119">Informazioni sugli oggetti Error e ErrorItem</span><span class="sxs-lookup"><span data-stu-id="e4c39-119">About the Error and ErrorItem Objects</span></span>

<span data-ttu-id="e4c39-120">Gli oggetti **Error** e **ErrorItem** regolano le funzionalità di gestione degli errori di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e4c39-120">The **Error** and **ErrorItem** objects govern the error-handling capabilities of Windows Media Player.</span></span> <span data-ttu-id="e4c39-121">L'oggetto **Error** viene ottenuto dall'oggetto **Player** tramite la proprietà **Error** .</span><span class="sxs-lookup"><span data-stu-id="e4c39-121">The **Error** object is obtained from the **Player** object through the **error** property.</span></span> <span data-ttu-id="e4c39-122">È possibile ottenere un codice specifico dall'oggetto **Error** usando la proprietà **Item** dell'oggetto **Error** per creare l'oggetto **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="e4c39-122">You can get a specific code from the **Error** object by using the **item** property of the **Error** object to create the **ErrorItem** object.</span></span> <span data-ttu-id="e4c39-123">Per ottenere, ad esempio, il codice di errore del primo elemento Error, digitare:</span><span class="sxs-lookup"><span data-stu-id="e4c39-123">For example, to get the error code of the first error item, type:</span></span>


```C++
myerrorcode = player.error.item(0).errorCode;

```



<span data-ttu-id="e4c39-124">È anche possibile richiamare la guida Web con l'oggetto **Error** usando il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e4c39-124">You can also invoke Web Help with the **Error** object by using the following code:</span></span>


```C++
player.error.webHelp();

```



## <a name="related-topics"></a><span data-ttu-id="e4c39-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4c39-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4c39-126">**Oggetto Error**</span><span class="sxs-lookup"><span data-stu-id="e4c39-126">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="e4c39-127">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="e4c39-127">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="e4c39-128">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="e4c39-128">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




