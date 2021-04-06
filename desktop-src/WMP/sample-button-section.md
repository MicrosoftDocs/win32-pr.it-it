---
title: Sezione pulsante di esempio
description: Sezione pulsante di esempio
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Windows Media Player Mobile Skins, sezione Button
- interfacce, sezione Button
- riferimento per Skin, sezione Button
- pulsanti in Skin, sezione Button
- file di definizione dell'interfaccia, sezione Button
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044957"
---
# <a name="sample-button-section"></a><span data-ttu-id="06fca-108">Sezione pulsante di esempio</span><span class="sxs-lookup"><span data-stu-id="06fca-108">Sample Button Section</span></span>

<span data-ttu-id="06fca-109">Le righe seguenti mostrano una sezione dei pulsanti tipici di un file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="06fca-109">The following lines show a typical Buttons section of a skin definition file:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



<span data-ttu-id="06fca-110">Questo codice definisce otto pulsanti usati per fornire tutte le funzioni seguenti in un'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="06fca-110">This code defines eight buttons that are used to provide all of the following functions in a skin:</span></span>

-   <span data-ttu-id="06fca-111">Riprodurre, sospendere e arrestare elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="06fca-111">Play, pause, and stop media items.</span></span>
-   <span data-ttu-id="06fca-112">Riproduzione casuale, ripetizione e spostamento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="06fca-112">Shuffle, repeat, and move through the playlist.</span></span>
-   <span data-ttu-id="06fca-113">Disattivare il volume.</span><span class="sxs-lookup"><span data-stu-id="06fca-113">Mute the volume.</span></span>

<span data-ttu-id="06fca-114">Tutti i pulsanti eccetto il pulsante di silenziamento sono pulsanti dell'area.</span><span class="sxs-lookup"><span data-stu-id="06fca-114">All the buttons except the mute button are region buttons.</span></span> <span data-ttu-id="06fca-115">Il pulsante di silenziamento ottiene le immagini inserite e disabilitate dalla bitmap con privilegi avanzati per praticità.</span><span class="sxs-lookup"><span data-stu-id="06fca-115">The mute button gets its Pushed and Disabled images from the Super bitmap for convenience.</span></span>

> [!Note]  
> <span data-ttu-id="06fca-116">I tipi di pulsanti sono deprecati nelle interfacce per Windows Media Player 10 mobile o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="06fca-116">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span> <span data-ttu-id="06fca-117">Invece di un tipo di pulsante dichiarato nel file skin, immettere "NA" per ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="06fca-117">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="06fca-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06fca-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06fca-119">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="06fca-119">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




