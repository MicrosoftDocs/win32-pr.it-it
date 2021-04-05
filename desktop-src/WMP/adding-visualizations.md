---
title: Aggiunta di visualizzazioni
description: Aggiunta di visualizzazioni
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- creazione di interfacce, visualizzazioni
- Interfacce di Media Player Windows, visualizzazioni
- interfacce, visualizzazioni
- Visualizzazioni, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710786"
---
# <a name="adding-visualizations"></a><span data-ttu-id="90012-107">Aggiunta di visualizzazioni</span><span class="sxs-lookup"><span data-stu-id="90012-107">Adding Visualizations</span></span>

<span data-ttu-id="90012-108">È possibile aggiungere una finestra di visualizzazione nello stesso modo in cui è stata aggiunta una finestra video.</span><span class="sxs-lookup"><span data-stu-id="90012-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="90012-109">È possibile utilizzare la stessa interfaccia, ma viene utilizzato un elemento **Effects** .</span><span class="sxs-lookup"><span data-stu-id="90012-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="90012-110">Prima di tutto è necessario aggiungere l'elemento **Effects** e assegnargli un ID e una dimensione:</span><span class="sxs-lookup"><span data-stu-id="90012-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="90012-111">È quindi possibile assegnare i due pulsanti a una stringa di codice di visualizzazione precedente e successiva:</span><span class="sxs-lookup"><span data-stu-id="90012-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="90012-112">I livelli e le bitmap sono gli stessi usati nell'esempio video, ad eccezione del fatto che la freccia di riproduzione è stata copiata e capovolta orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="90012-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="90012-113">Infine, è stato aggiunto un semplice elemento **Player** con l'attributo **URL** per scegliere un brano da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="90012-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="90012-114">Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia di visualizzazione di lavoro simile.</span><span class="sxs-lookup"><span data-stu-id="90012-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90012-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90012-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90012-116">**Guida alla creazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="90012-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




