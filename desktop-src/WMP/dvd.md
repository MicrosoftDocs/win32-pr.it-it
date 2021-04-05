---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, migrazione di DVD
- Modello a oggetti di Windows Media Player, DVD
- modello a oggetti, DVD
- Controllo ActiveX di Windows Media Player, DVD
- Controllo ActiveX, DVD
- Controllo ActiveX Windows Media Player Mobile, DVD
- Windows Media Player Mobile, migrazione di DVD
- Guida alla migrazione, DVD
- Migrazione di DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711626"
---
# <a name="dvd"></a><span data-ttu-id="9bd8a-112">DVD</span><span class="sxs-lookup"><span data-stu-id="9bd8a-112">DVD</span></span>

<span data-ttu-id="9bd8a-113">Il controllo ActiveX Windows Media Player 6,4 contiene un oggetto **DVD** che espone un'ampia gamma di metodi e proprietà e un evento per la gestione specifica del contenuto DVD.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-113">The Windows Media Player 6.4 ActiveX control contains a **DVD** object that exposes a variety of methods and properties, and one event, for dealing specifically with DVD content.</span></span> <span data-ttu-id="9bd8a-114">Ad esempio, per determinare il numero di titoli DVD disponibili, usare **Player6**. proprietà **titlesAvailable** :</span><span class="sxs-lookup"><span data-stu-id="9bd8a-114">For instance, to determine the number of DVD titles available, you use the **Player6**.**titlesAvailable** property:</span></span>


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



<span data-ttu-id="9bd8a-115">Il modello a oggetti di Windows Media Player 7 o versione successiva implementa un approccio più integrato a DVD.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-115">The Windows Media Player 7 or later object model implements a more integrated approach to DVD.</span></span> <span data-ttu-id="9bd8a-116">Proprietà, metodi ed eventi specifici per DVD sono implementati solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-116">DVD-specific properties, methods, and events are implemented only where needed.</span></span> <span data-ttu-id="9bd8a-117">In caso contrario, la funzionalità del modello a oggetti esistente funziona con supporti DVD come previsto.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-117">Otherwise, existing object model functionality works with DVD media as you might expect.</span></span> <span data-ttu-id="9bd8a-118">Per determinare, ad esempio, il numero di titoli DVD disponibili quando si usa Windows Media Player 7 o versione successiva, è possibile recuperare un oggetto **playlist** dall'oggetto **CDROM** :</span><span class="sxs-lookup"><span data-stu-id="9bd8a-118">For example, to determine the number of DVD titles available when using Windows Media Player 7 or later, you retrieve a **Playlist** object from the **Cdrom** object:</span></span>


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



<span data-ttu-id="9bd8a-119">Nell'esempio precedente viene recuperato un oggetto **playlist** con una prima voce che rappresenta il supporto DVD nella prima unità.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-119">The preceding example retrieves a **Playlist** object with a first entry representing the DVD media in the first drive.</span></span> <span data-ttu-id="9bd8a-120">Le voci aggiuntive rappresentano i singoli titoli di DVD.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-120">Additional entries represent individual DVD titles.</span></span> <span data-ttu-id="9bd8a-121">Il numero di titoli disponibili può pertanto essere calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="9bd8a-121">Therefore, the number of titles available can be calculated as follows:</span></span>


```C++
var numTitles = dvdTitles.count - 1;

```



<span data-ttu-id="9bd8a-122">Di seguito sono riportate le principali differenze da tenere presenti durante la migrazione dalla versione 6,4:</span><span class="sxs-lookup"><span data-stu-id="9bd8a-122">Here are the main differences to keep in mind when migrating from version 6.4:</span></span>

-   <span data-ttu-id="9bd8a-123">La riproduzione di DVD è supportata solo quando si usa Windows Media Player per Windows XP o versione successiva e il sistema operativo Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-123">DVD playback is supported only when using Windows Media Player for Windows XP or later and the Windows XP operating system or later.</span></span>
-   <span data-ttu-id="9bd8a-124">Le unità DVD-ROM vengono enumerate esattamente come le unità CD-ROM usando l'oggetto **cdromcollection** .</span><span class="sxs-lookup"><span data-stu-id="9bd8a-124">DVD-ROM drives are enumerated exactly like CD-ROM drives using the **CdromCollection** object.</span></span>
-   <span data-ttu-id="9bd8a-125">Le singole unità DVD-ROM vengono gestite tramite l'oggetto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="9bd8a-125">Individual DVD-ROM drives are managed using the **Cdrom** object.</span></span>
-   <span data-ttu-id="9bd8a-126">L'oggetto **DVD** estende il modello a oggetti con i metodi e una proprietà specifica per l'utilizzo di DVD.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-126">The **DVD** object extends the object model with methods and one property specifically for working with DVD.</span></span>
-   <span data-ttu-id="9bd8a-127">Sono disponibili due nuovi eventi, **OpenPlaylistSwitch** e **DomainChange**, in particolare per l'uso di DVD.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-127">There are two new events, **OpenPlaylistSwitch** and **DomainChange**, specifically for working with DVD.</span></span>
-   <span data-ttu-id="9bd8a-128">Il contenuto del DVD è organizzato usando oggetti della **playlist** e oggetti **multimediali** .</span><span class="sxs-lookup"><span data-stu-id="9bd8a-128">DVD content is organized using **Playlist** objects and **Media** objects.</span></span>
-   <span data-ttu-id="9bd8a-129">Le lingue DVD sono gestite usando le funzionalità del linguaggio disponibili nell'oggetto **Controls** (Windows Media Player 9 Series o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="9bd8a-129">DVD languages are managed using the language functionality available from the **Controls** object (Windows Media Player 9 Series or later).</span></span>
-   <span data-ttu-id="9bd8a-130">I controlli di trasporto e le informazioni sulla posizione per il DVD funzionano come per altri tipi di supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="9bd8a-130">Transport controls and position information for DVD work the same as for other digital media types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bd8a-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9bd8a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bd8a-132">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-132">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="9bd8a-133">**Uso del controllo Media Player di Windows con Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="9bd8a-133">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




