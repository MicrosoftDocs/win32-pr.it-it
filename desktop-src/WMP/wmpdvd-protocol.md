---
title: Protocollo WMPDVD
description: Protocollo WMPDVD
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player, protocolli
- Modello a oggetti di Windows Media Player, protocolli
- modello a oggetti, protocolli
- Controllo ActiveX di Windows Media Player, protocolli per il modello a oggetti
- Controllo ActiveX, protocolli per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, protocolli per il modello a oggetti
- Windows Media Player Mobile, protocolli per il modello a oggetti
- protocolli, modello a oggetti di Windows Media Player
- protocolli, WMPDVD
- Protocollo WMPDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329663"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="14828-113">Protocollo WMPDVD</span><span class="sxs-lookup"><span data-stu-id="14828-113">WMPDVD Protocol</span></span>

<span data-ttu-id="14828-114">Il protocollo WMPDVD consente di specificare un supporto da un DVD usando la sintassi dell'URL.</span><span class="sxs-lookup"><span data-stu-id="14828-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="14828-115">Questo è il formato generale del protocollo:</span><span class="sxs-lookup"><span data-stu-id="14828-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="14828-116">Il segmento *unità* è la lettera dell'unità DVD; non include i due punti usati in genere con gli identificatori di unità.</span><span class="sxs-lookup"><span data-stu-id="14828-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="14828-117">Questo segmento è sempre obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="14828-117">This segment is always required.</span></span>

<span data-ttu-id="14828-118">Il segmento del *titolo* è il numero del titolo da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="14828-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="14828-119">Non è necessario a meno che non si desideri avviare la riproduzione a un titolo specifico o a un capitolo specifico di un titolo specifico.</span><span class="sxs-lookup"><span data-stu-id="14828-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="14828-120">Il segmento del *capitolo* è il numero del capitolo da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="14828-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="14828-121">Non è necessario a meno che non si desideri avviare la riproduzione in un capitolo specifico di un titolo specifico.</span><span class="sxs-lookup"><span data-stu-id="14828-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="14828-122">L'argomento ContentDir e è il percorso di un VIDEO \_ TS. File IFO, che può trovarsi in una risorsa di archiviazione locale o in una condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="14828-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="14828-123">Se si include questo segmento, il segmento di *unità* viene ignorato anche se è ancora necessario.</span><span class="sxs-lookup"><span data-stu-id="14828-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="14828-124">Se si include anche il segmento *titolo* o i segmenti *titolo* e *capitolo* , sono relativi al contenuto DVD specificato nel segmento ContentDir e, non al segmento di *unità* .</span><span class="sxs-lookup"><span data-stu-id="14828-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="14828-125">Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre il DVD dall'inizio, come se si stesse avviando automaticamente.</span><span class="sxs-lookup"><span data-stu-id="14828-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="14828-126">Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre il DVD dall'inizio del titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="14828-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="14828-127">Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre il DVD dal capitolo specificato.</span><span class="sxs-lookup"><span data-stu-id="14828-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="14828-128">Nell'esempio seguente viene usato il protocollo WMPDVD per riprodurre contenuto DVD dalla risorsa di archiviazione locale.</span><span class="sxs-lookup"><span data-stu-id="14828-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="14828-129">La stringa di *percorso* termina con la cartella che contiene il video \_ TS. File IFO; non include il nome del file.</span><span class="sxs-lookup"><span data-stu-id="14828-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="14828-130">In questo esempio, il valore del segmento di *unità* non ha alcun effetto anche se è obbligatorio e la riproduzione inizia nel capitolo 4 del titolo 2.</span><span class="sxs-lookup"><span data-stu-id="14828-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="14828-131">Per l'assegnazione di una stringa WMPDVD alla proprietà **URL** è necessario Windows Media Player 9 Series o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="14828-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14828-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14828-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14828-133">**Protocolli e tipi di file supportati**</span><span class="sxs-lookup"><span data-stu-id="14828-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




