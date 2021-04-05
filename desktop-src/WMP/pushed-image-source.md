---
title: Origine immagine push
description: Origine immagine push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711554"
---
# <a name="pushed-image-source"></a><span data-ttu-id="64e55-108">Origine immagine push</span><span class="sxs-lookup"><span data-stu-id="64e55-108">Pushed Image Source</span></span>

<span data-ttu-id="64e55-109">È necessario definire l'origine dell'immagine che si desidera visualizzare quando l'utente preme un pulsante.</span><span class="sxs-lookup"><span data-stu-id="64e55-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="64e55-110">L'immagine deriva dal file definito come inserito nella sezione bitmap.</span><span class="sxs-lookup"><span data-stu-id="64e55-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="64e55-111">È necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="64e55-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="64e55-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate superiore e sinistra (in pixel) dell'immagine che si vuole usare all'interno del file di immagine di cui è stato eseguito il push.</span><span class="sxs-lookup"><span data-stu-id="64e55-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="64e55-113">La posizione in cui verrà visualizzata l'immagine deriva dalle coordinate definite per il pulsante rispetto all'immagine di sfondo; ma il percorso da cui deriva è definito dai due numeri che seguono "pushed @" ed è relativo all'immagine push da cui viene letta l'immagine.</span><span class="sxs-lookup"><span data-stu-id="64e55-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="64e55-114">Ad esempio, per usare un'immagine dall'immagine push presente nel file di cui è stato eseguito il push, il cui percorso superiore sinistro è 50, 60 usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="64e55-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="64e55-115">Se non si desidera visualizzare un'immagine diversa, è possibile definire la bitmap di sfondo come bitmap sottoposta a push.</span><span class="sxs-lookup"><span data-stu-id="64e55-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="64e55-116">A tale scopo, specificare il file di sfondo come file di cui è stato eseguito il push e specificare l'offset nell'angolo superiore sinistro del pulsante:</span><span class="sxs-lookup"><span data-stu-id="64e55-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="64e55-117">In tal caso, nessuno dei pulsanti può visualizzare un'immagine inserita.</span><span class="sxs-lookup"><span data-stu-id="64e55-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="64e55-118">Si consiglia di visualizzare un'immagine push per tutti i pulsanti per fornire all'utente un'indicazione visiva, perché non è sempre chiaro se un tocco produce un risultato, soprattutto quando la musica viene riprodotta o se il suono di tocco è disattivato.</span><span class="sxs-lookup"><span data-stu-id="64e55-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64e55-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64e55-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64e55-120">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="64e55-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




