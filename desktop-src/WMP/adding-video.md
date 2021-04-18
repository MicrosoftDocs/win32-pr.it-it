---
title: Aggiunta di video
description: Aggiunta di video
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- creazione di interfacce, video
- Windows Media Player Skins, video
- interfacce, video
- video in interfacce, aggiunta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298221"
---
# <a name="adding-video"></a><span data-ttu-id="40d47-107">Aggiunta di video</span><span class="sxs-lookup"><span data-stu-id="40d47-107">Adding Video</span></span>

<span data-ttu-id="40d47-108">È possibile aggiungere un video al file semplicemente usando l'elemento **video** e definendo la posizione in cui si vuole inserire la finestra video.</span><span class="sxs-lookup"><span data-stu-id="40d47-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="40d47-109">Usare lo stesso codice riportato nella sezione scelta dei file; è sufficiente aggiungere l'elemento **video** con gli attributi top, Left, Width e Height.</span><span class="sxs-lookup"><span data-stu-id="40d47-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="40d47-110">Quando si riproduce un video, questo verrà visualizzato nella finestra.</span><span class="sxs-lookup"><span data-stu-id="40d47-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="40d47-111">L'immagine per l'esempio video è stata modificata per creare un'interfaccia leggermente più ampia.</span><span class="sxs-lookup"><span data-stu-id="40d47-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="40d47-112">Poiché i livelli sono stati usati in Photoshop, i pulsanti sono stati spostati in modo semplice e un nuovo set è stato creato molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="40d47-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="40d47-113">Solo l'immagine di sfondo è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="40d47-113">Only the background image was changed.</span></span> <span data-ttu-id="40d47-114">Un riempimento è stato usato in un livello vuoto ed è stato aggiunto un effetto smussato e rilievo.</span><span class="sxs-lookup"><span data-stu-id="40d47-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="40d47-115">Nella sezione di esempio dell'SDK è possibile visualizzare una simile interfaccia video funzionante.</span><span class="sxs-lookup"><span data-stu-id="40d47-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40d47-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40d47-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40d47-117">**Guida alla creazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="40d47-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




