---
title: Descrizione (Windows Media Player SDK)
description: Descrizione
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Mobile Skins, sezione Descrizione
- interfacce, sezione Descrizione
- riferimento per le interfacce, sezione Descrizione
- Sezione Descrizione in Skins
- file di definizione dell'interfaccia, sezione Descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400134"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="1d130-108">Descrizione (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="1d130-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="1d130-109">Quando si crea un'interfaccia per Windows Media Player 9 Series per Windows Mobile 2003 o versione successiva, è necessario includere una sezione Descrizione.</span><span class="sxs-lookup"><span data-stu-id="1d130-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="1d130-110">La sezione Descrizione consente di specificare la larghezza e l'altezza dello schermo, la risoluzione dello schermo e l'orientamento di visualizzazione per cui è stata progettata l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1d130-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="1d130-111">La sezione Description deve essere visualizzata nel file di definizione dell'interfaccia prima di qualsiasi altra sezione e subito dopo la dichiarazione di versione iniziale.</span><span class="sxs-lookup"><span data-stu-id="1d130-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="1d130-112">La sezione Descrizione del file di definizione dell'interfaccia deve iniziare con la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="1d130-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="1d130-113">È quindi necessario aggiungere informazioni sulle dimensioni dell'interfaccia e la risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1d130-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="1d130-114">Nell'esempio seguente viene illustrato come specificare le dimensioni:</span><span class="sxs-lookup"><span data-stu-id="1d130-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="1d130-115">In questo modo si specifica che l'interfaccia è stata progettata per essere visualizzata 240 pixel di larghezza, 320 pixel di altezza e con la risoluzione dello schermo 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="1d130-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="1d130-116">Si noti che questo implica un orientamento in modalità verticale.</span><span class="sxs-lookup"><span data-stu-id="1d130-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="1d130-117">Facoltativamente, è possibile specificare la modalità di orientamento per la quale è stata progettata l'interfaccia nella sezione Descrizione.</span><span class="sxs-lookup"><span data-stu-id="1d130-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="1d130-118">Nell'esempio seguente viene illustrato come specificare l'orientamento:</span><span class="sxs-lookup"><span data-stu-id="1d130-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="1d130-119">Nella tabella seguente sono elencati i valori che è possibile utilizzare per l'orientamento.</span><span class="sxs-lookup"><span data-stu-id="1d130-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="1d130-120">Orientamento</span><span class="sxs-lookup"><span data-stu-id="1d130-120">Orientation</span></span> | <span data-ttu-id="1d130-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d130-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d130-122">Orizzontale</span><span class="sxs-lookup"><span data-stu-id="1d130-122">Landscape</span></span>   | <span data-ttu-id="1d130-123">La larghezza dell'interfaccia è maggiore dell'altezza dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1d130-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="1d130-124">La visualizzazione è orientata in modo orizzontale.</span><span class="sxs-lookup"><span data-stu-id="1d130-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="1d130-125">Verticale</span><span class="sxs-lookup"><span data-stu-id="1d130-125">Portrait</span></span>    | <span data-ttu-id="1d130-126">L'altezza dell'interfaccia è maggiore della larghezza dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1d130-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="1d130-127">La visualizzazione è orientata in modo verticale.</span><span class="sxs-lookup"><span data-stu-id="1d130-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="1d130-128">Square</span><span class="sxs-lookup"><span data-stu-id="1d130-128">Square</span></span>      | <span data-ttu-id="1d130-129">L'altezza dell'interfaccia è uguale alla larghezza dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1d130-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="1d130-130">La visualizzazione non ha un orientamento.</span><span class="sxs-lookup"><span data-stu-id="1d130-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="1d130-131">Windows Media Player 9 Series per Windows Mobile 2003 visualizzerà solo una particolare interfaccia quando la sezione Descrizione specificata nel file di definizione dell'interfaccia personalizzata corrisponde allo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d130-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="1d130-132">È necessario prestare attenzione a specificare sempre le dimensioni, la risoluzione e l'orientamento corrette per le quali è stata creata l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1d130-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="1d130-133">Se, ad esempio, le dimensioni specificate dall'interfaccia descrivono un orientamento orizzontale, l'interfaccia non sarà disponibile quando il dispositivo è in modalità verticale, anche se si specifica verticale nella linea di orientamento.</span><span class="sxs-lookup"><span data-stu-id="1d130-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d130-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d130-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d130-135">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="1d130-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




