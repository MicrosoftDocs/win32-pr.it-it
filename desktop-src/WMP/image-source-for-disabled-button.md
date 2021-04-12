---
title: Origine immagine per il pulsante disabilitato
description: Origine immagine per il pulsante disabilitato
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396034"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="ed769-108">Origine immagine per il pulsante disabilitato</span><span class="sxs-lookup"><span data-stu-id="ed769-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="ed769-109">È necessario definire l'origine dell'immagine che si desidera visualizzare quando un pulsante è disabilitato o presenta uno stato che corrisponde a disattivato.</span><span class="sxs-lookup"><span data-stu-id="ed769-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="ed769-110">L'immagine deriva dal file definito come disabilitato nella sezione bitmap.</span><span class="sxs-lookup"><span data-stu-id="ed769-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="ed769-111">È necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio.</span><span class="sxs-lookup"><span data-stu-id="ed769-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="ed769-112">È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si desidera utilizzare nel file bitmap.</span><span class="sxs-lookup"><span data-stu-id="ed769-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="ed769-113">Il percorso in cui l'immagine verrà visualizzata deriva dalle coordinate definite per il pulsante rispetto all'immagine di sfondo, ma la posizione da cui deriva è definita dai due numeri che seguono "disabled @" ed è relativo alla bitmap disabilitata da cui si sta leggendo l'immagine.</span><span class="sxs-lookup"><span data-stu-id="ed769-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="ed769-114">Ad esempio, per usare un'immagine della bitmap disabilitata presente nel file disabilitato in un percorso superiore e sinistro di 50, 60 pixel, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="ed769-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="ed769-115">È necessario definire una bitmap disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ed769-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="ed769-116">Se non si desidera visualizzare un'immagine diversa, è possibile definire la bitmap di sfondo come bitmap disabilitata con un offset di 0, 0:</span><span class="sxs-lookup"><span data-stu-id="ed769-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="ed769-117">Nell'esempio precedente 50, 60 è la posizione del pulsante che si sta utilizzando nel file disabilitato (in questo caso, la stessa posizione del pulsante nella bitmap di sfondo).</span><span class="sxs-lookup"><span data-stu-id="ed769-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="ed769-118">È tuttavia consigliabile visualizzare un'immagine disabilitata per tutti i pulsanti per fornire agli utenti un'indicazione visiva, perché molti pulsanti non saranno utilizzabili in determinate condizioni, ad esempio una playlist vuota.</span><span class="sxs-lookup"><span data-stu-id="ed769-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="ed769-119">Se gli utenti sanno che un pulsante è disabilitato, non continuerà a fare clic su di esso o ritenere che l'interfaccia non funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="ed769-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed769-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed769-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed769-121">**Pulsanti**</span><span class="sxs-lookup"><span data-stu-id="ed769-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




