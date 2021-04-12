---
title: Testo scorrevole
description: Testo scorrevole
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skin, about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396447"
---
# <a name="marquee"></a><span data-ttu-id="6d550-107">Testo scorrevole</span><span class="sxs-lookup"><span data-stu-id="6d550-107">Marquee</span></span>

<span data-ttu-id="6d550-108">Un Marquee è una casella di visualizzazione di testo a scorrimento che visualizza informazioni da una o più caselle di visualizzazione di testo.</span><span class="sxs-lookup"><span data-stu-id="6d550-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="6d550-109">Non è necessario aggiungere un Marquee, ma può essere molto utile quando si dispone di informazioni dettagliate che si desidera visualizzare all'utente in uno spazio limitato.</span><span class="sxs-lookup"><span data-stu-id="6d550-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="6d550-110">Il testo nella casella di selezione verrà spostato solo se vengono soddisfatte entrambe le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d550-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="6d550-111">Il testo visualizzato nella casella di selezione è maggiore della larghezza della casella di visualizzazione Marquee.</span><span class="sxs-lookup"><span data-stu-id="6d550-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="6d550-112">L'elemento multimediale viene arrestato o sospeso.</span><span class="sxs-lookup"><span data-stu-id="6d550-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="6d550-113">La sezione Marquee del file di definizione dell'interfaccia deve iniziare con questa riga:</span><span class="sxs-lookup"><span data-stu-id="6d550-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="6d550-114">Per mantenere la compatibilità con le versioni di Windows Media Player Mobile precedenti a Windows Media Player 10 Mobile, l'utilizzo di "Marquis" in un file di definizione dell'interfaccia personalizzata è ancora considerato valido.</span><span class="sxs-lookup"><span data-stu-id="6d550-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="6d550-115">È quindi necessario aggiungere una o più righe contenenti informazioni su ciascuna casella di visualizzazione Marquee nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6d550-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="6d550-116">È possibile usare il modello seguente per la sezione Marquee del file di definizione dell'interfaccia utente:</span><span class="sxs-lookup"><span data-stu-id="6d550-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="6d550-117">È necessario utilizzare l'ordine seguente per informazioni in ogni riga della sezione Marquee (è necessaria ogni parte della riga):</span><span class="sxs-lookup"><span data-stu-id="6d550-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="6d550-118">Posizione Marquee</span><span class="sxs-lookup"><span data-stu-id="6d550-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="6d550-119">Carattere Marquee</span><span class="sxs-lookup"><span data-stu-id="6d550-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="6d550-120">Colore Marquee</span><span class="sxs-lookup"><span data-stu-id="6d550-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="6d550-121">Combinazioni di testo</span><span class="sxs-lookup"><span data-stu-id="6d550-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="6d550-122">Per un esempio di codice Marquee, vedere la [sezione Sample Marquee](sample-marquee-section.md).</span><span class="sxs-lookup"><span data-stu-id="6d550-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d550-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d550-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d550-124">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="6d550-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




