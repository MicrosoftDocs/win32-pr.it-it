---
title: Uso del modello a oggetti di Windows Media Player 7 o versione successiva
description: Uso del modello a oggetti di Windows Media Player 7 o versione successiva
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, versione 7 o successiva
- modello a oggetti, versione 7 o successiva
- Controllo ActiveX di Windows Media Player versione 7 o successiva
- Controllo ActiveX, versione 7 o successiva
- Controllo ActiveX Windows Media Player Mobile versione 7 o successiva
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione, 7 o versione successiva
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330708"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a><span data-ttu-id="d1eb1-112">Uso del modello a oggetti di Windows Media Player 7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d1eb1-112">Using the Windows Media Player 7 or Later Object Model</span></span>

<span data-ttu-id="d1eb1-113">La maggior parte delle attività che potrebbero essere state eseguite utilizzando il modello a oggetti del controllo ActiveX di Windows Media Player 6,4 richiederà un nuovo approccio.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-113">Most of the tasks you may have been performing using the Windows Media Player 6.4 ActiveX control object model will require a new approach.</span></span> <span data-ttu-id="d1eb1-114">In molti casi, i nomi delle proprietà, dei metodi e degli eventi sono stati modificati nel modello a oggetti di Windows Media Player 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-114">In many cases, the names of the properties, methods, and events have changed in the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="d1eb1-115">Ad esempio, per specificare il percorso del file nel modello a oggetti della versione 6,4, impostare la proprietà **Player6. FileName** :</span><span class="sxs-lookup"><span data-stu-id="d1eb1-115">For instance, to specify the file path in the version 6.4 object model, you set the **Player6.FileName** property:</span></span>


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="d1eb1-116">Quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, è necessario impostare la proprietà **Player. URL** :</span><span class="sxs-lookup"><span data-stu-id="d1eb1-116">When using the Windows Media Player 7 or later object model, you must set the **Player.URL** property:</span></span>


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="d1eb1-117">In alternativa, usando il modello a oggetti 10, è possibile ottenere un oggetto **multimediale** dalla libreria, quindi impostare la proprietà **Player. currentMedia** :</span><span class="sxs-lookup"><span data-stu-id="d1eb1-117">Alternatively, using the 10 object model, you can obtain a **Media** object from the library, and then set the **Player.currentMedia** property:</span></span>


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



<span data-ttu-id="d1eb1-118">Gran parte delle funzionalità del modello a oggetti di Windows Media Player 7 o versione successiva è accessibile tramite la gerarchia di oggetti.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-118">Much of the functionality in the Windows Media Player 7 or later object model is accessed through the object hierarchy.</span></span> <span data-ttu-id="d1eb1-119">Come illustrato nell'esempio precedente, è possibile ottenere un oggetto **playlist** usando il metodo **GetAll** dell'oggetto **mediacollection** , a cui si accede tramite l'oggetto **Player** radice.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-119">As the previous example showed, you can obtain a **Playlist** object by using the **getAll** method of the **mediaCollection** object, which is accessed through the root **Player** object.</span></span> <span data-ttu-id="d1eb1-120">È quindi possibile ottenere un oggetto **multimediale** particolare dall'oggetto **playlist** usando il metodo **Item** dell'oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="d1eb1-120">You can then obtain a particular **Media** object from the **Playlist** object by using the **item** method of the **Playlist** object.</span></span> <span data-ttu-id="d1eb1-121">Esistono cinque metodi aggiuntivi accessibili tramite l'oggetto **mediacollection** che restituiscono un oggetto **playlist** ; ogni metodo consente di recuperare l'oggetto in base a criteri specifici, ad esempio genere o album.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-121">There are five additional methods accessible through the **mediaCollection** object that return a **Playlist** object; each method allows you to retrieve the object based on specific criteria, like genre or album.</span></span>

<span data-ttu-id="d1eb1-122">La struttura gerarchica del modello a oggetti del controllo ActiveX Windows Media Player 7 o versioni successive offre un approccio più logico per organizzare le proprietà, i metodi e gli eventi disponibili per l'uso.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-122">The hierarchical structure of the Windows Media Player 7 or later ActiveX control object model provides a more logical approach to organizing the properties, methods, and events available for your use.</span></span> <span data-ttu-id="d1eb1-123">Tutte le funzionalità per i controlli Player sono contenute nell'oggetto **Controls** , tutte le funzionalità della connessione di rete Player sono contenute nell'oggetto di **rete** e così via.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-123">All the functionality for the Player controls is contained in the **Controls** object, all the functionality for the Player network connection is contained in the **Network** object, and so forth.</span></span> <span data-ttu-id="d1eb1-124">Ad esempio, per avviare la riproduzione del contenuto utilizzando il modello a oggetti della versione 6,4, utilizzare il metodo **Player6. Play** :</span><span class="sxs-lookup"><span data-stu-id="d1eb1-124">For example, to start content playing using the version 6.4 object model, you use the **Player6.Play** method:</span></span>


```C++
WMP64.Play();

```



<span data-ttu-id="d1eb1-125">Quando si usa il modello a oggetti di Windows Media Player 7 o versione successiva, è necessario accedere al metodo **Play** usando l'oggetto **Controls** :</span><span class="sxs-lookup"><span data-stu-id="d1eb1-125">When using the Windows Media Player 7 or later object model, you must access the **Play** method by using the **Controls** object:</span></span>


```C++
WMP9.controls.play();

```



<span data-ttu-id="d1eb1-126">La profondità del modello a oggetti, tuttavia, può causare istruzioni script molto lunghe:</span><span class="sxs-lookup"><span data-stu-id="d1eb1-126">The depth of the object model, however, can lead to very long script statements:</span></span>


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



<span data-ttu-id="d1eb1-127">Le istruzioni come la precedente possono essere rese molto più semplici e più leggibili tramite l'utilizzo di singoli oggetti denominati.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-127">Statements like the preceding one can be made much simpler and more readable by working with individual named objects.</span></span> <span data-ttu-id="d1eb1-128">Nell'esempio seguente l'istruzione del codice precedente viene sostituita con la sintassi utilizzando variabili oggetto separate:</span><span class="sxs-lookup"><span data-stu-id="d1eb1-128">The following example replaces the preceding code statement with syntax using separate object variables:</span></span>


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



<span data-ttu-id="d1eb1-129">Questo stile di codifica richiede più righe di script, ma è molto più semplice da seguire, soprattutto con i commenti aggiunti.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-129">This coding style requires more lines of script, but is much easier to follow, especially with the added comments.</span></span> <span data-ttu-id="d1eb1-130">Un altro vantaggio: l'oggetto **currentPlaylist** è facile da riutilizzare perché è archiviato nella variabile pl.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-130">There is another advantage: the **currentPlaylist** object is easy to reuse because it is stored in the variable pl.</span></span>

<span data-ttu-id="d1eb1-131">Molte proprietà, metodi ed eventi nel modello a oggetti di Windows Media Player 7 o versione successiva impostano o recuperano valori diversi oppure restituiscono valori di un tipo o di un numero diverso rispetto alla funzionalità corrispondente nel modello a oggetti della versione 6,4.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-131">Many of the properties, methods, and events in the Windows Media Player 7 or later object model set or retrieve different values, or return values of a different type or number, compared to corresponding functionality in the version 6.4 object model.</span></span> <span data-ttu-id="d1eb1-132">Ad esempio, quando **Player6. openState** recupera 2, tale valore corrisponde alla costante Visual Basic **nsLoadingNSC**, vale a dire che il lettore sta caricando un file di stazione con estensione NSC.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-132">For instance, when **Player6.openState** retrieves 2, that value corresponds to the Visual Basic constant **nsLoadingNSC**, meaning the Player is loading a station file with a .nsc file name extension.</span></span> <span data-ttu-id="d1eb1-133">Tuttavia, quando **la proprietà del** modello a oggetti di Windows Media Player 7 o versione successiva restituisce 2, tale valore corrisponde allo stato PlaylistLocating, ovvero Windows Media Player sta tentando di individuare una playlist.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-133">But when the Windows Media Player 7 or later object model property **Player.openState** retrieves 2, that value corresponds to the state PlaylistLocating, meaning Windows Media Player is attempting to locate a playlist.</span></span> <span data-ttu-id="d1eb1-134">Inoltre, la proprietà **Player6. openState** può recuperare sette valori diversi, mentre la proprietà **Player. openState** di Windows Media Player 7 o versione successiva può recuperare 22 valori diversi.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-134">Additionally, the **Player6.openState** property can retrieve seven different values, while the Windows Media Player 7 or later **Player.openState** property can retrieve 22 different values.</span></span> <span data-ttu-id="d1eb1-135">Assicurarsi di fare riferimento al riferimento del modello a oggetti per la sezione scripting di Windows Media Player SDK durante la revisione del codice per l'utilizzo di una versione diversa del modello a oggetti.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-135">Be sure to refer to the Object Model Reference for Scripting section of the Windows Media Player SDK when revising code to use a different object model version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1eb1-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1eb1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1eb1-137">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="d1eb1-137">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="d1eb1-138">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="d1eb1-138">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="d1eb1-139">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="d1eb1-139">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




