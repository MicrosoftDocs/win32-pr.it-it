---
title: Pulsanti (Windows Media Player SDK)
description: Pulsanti
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Interfacce di Windows Media Player Mobile, panoramica sui pulsanti
- interfacce, panoramica sui pulsanti
- riferimento per le interfacce, i pulsanti
- pulsanti in Skin, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118863"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="52ecb-107">Pulsanti (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="52ecb-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="52ecb-108">È possibile usare uno o più pulsanti nell'interfaccia personalizzata e ogni pulsante deve essere definito nel file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="52ecb-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="52ecb-109">Se non si definisce un pulsante in questa sezione, l'interfaccia non sarà in grado di utilizzarla.</span><span class="sxs-lookup"><span data-stu-id="52ecb-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="52ecb-110">La sezione Buttons del file di definizione Skin inizia con questa riga:</span><span class="sxs-lookup"><span data-stu-id="52ecb-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="52ecb-111">È quindi necessario aggiungere una o più righe contenenti informazioni su ognuno dei pulsanti dell'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="52ecb-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="52ecb-112">Una linea tipica potrebbe essere:</span><span class="sxs-lookup"><span data-stu-id="52ecb-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="52ecb-113">Si noti che questo codice deve essere digitato come una riga che inizia con "come playpause" e termina con "pushed @ 160, 98".</span><span class="sxs-lookup"><span data-stu-id="52ecb-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="52ecb-114">È possibile usare il modello seguente per la sezione Button del file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="52ecb-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="52ecb-115">Si noti anche che questi devono essere tipizzati come righe singole, il primo a partire da "// <Function> " e termina con " &lt; push 2 Image src &gt; ".</span><span class="sxs-lookup"><span data-stu-id="52ecb-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="52ecb-116">La seconda riga inizia con "//----------" e termina con "------------------."</span><span class="sxs-lookup"><span data-stu-id="52ecb-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="52ecb-117">Le informazioni sul pulsante per ogni riga della sezione Button devono essere visualizzate nell'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="52ecb-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="52ecb-118">Sono necessarie solo le prime sei parti della riga.</span><span class="sxs-lookup"><span data-stu-id="52ecb-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="52ecb-119">Le immagini secondarie non vengono incluse a meno che non siano necessarie.</span><span class="sxs-lookup"><span data-stu-id="52ecb-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="52ecb-120">Button (funzione)</span><span class="sxs-lookup"><span data-stu-id="52ecb-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="52ecb-121">Tipo di pulsante</span><span class="sxs-lookup"><span data-stu-id="52ecb-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="52ecb-122">Posizione del pulsante</span><span class="sxs-lookup"><span data-stu-id="52ecb-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="52ecb-123">Origine immagine push</span><span class="sxs-lookup"><span data-stu-id="52ecb-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="52ecb-124">Origine immagine per il pulsante disabilitato</span><span class="sxs-lookup"><span data-stu-id="52ecb-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="52ecb-125">Colore RGB raggiunto</span><span class="sxs-lookup"><span data-stu-id="52ecb-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="52ecb-126">Origine normale dell'immagine secondaria</span><span class="sxs-lookup"><span data-stu-id="52ecb-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="52ecb-127">Origine normale dell'immagine terziaria</span><span class="sxs-lookup"><span data-stu-id="52ecb-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="52ecb-128">Origine immagine secondaria push</span><span class="sxs-lookup"><span data-stu-id="52ecb-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="52ecb-129">Origine dell'immagine terziaria push</span><span class="sxs-lookup"><span data-stu-id="52ecb-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="52ecb-130">Per un esempio di codice pulsante, vedere la [sezione pulsante di esempio](sample-button-section.md).</span><span class="sxs-lookup"><span data-stu-id="52ecb-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52ecb-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52ecb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52ecb-132">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="52ecb-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




