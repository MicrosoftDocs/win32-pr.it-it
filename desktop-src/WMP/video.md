---
title: Video (Windows Media Player SDK)
description: Video
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins, video
- interfacce, video
- informazioni di riferimento per Skins, video
- video in Skin, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300808"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="6b76f-107">Video (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="6b76f-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="6b76f-108">Una visualizzazione video consente all'utente di visualizzare i file video digitali.</span><span class="sxs-lookup"><span data-stu-id="6b76f-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="6b76f-109">L'area di visualizzazione video è visibile solo quando il video viene riprodotto o sospeso.</span><span class="sxs-lookup"><span data-stu-id="6b76f-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="6b76f-110">Quando si progetta l'interfaccia, è consigliabile riservare spazio nell'immagine di sfondo per contenere la visualizzazione video.</span><span class="sxs-lookup"><span data-stu-id="6b76f-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="6b76f-111">In caso contrario, la visualizzazione video potrebbe sovrapporsi a qualsiasi immagine visibile, ad esempio il file in background, i pulsanti e gli TrackBar, che impediscono all'utente di gestire i controlli sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6b76f-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="6b76f-112">La sezione video del file di definizione Skin deve iniziare con questa riga:</span><span class="sxs-lookup"><span data-stu-id="6b76f-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="6b76f-113">È quindi necessario aggiungere una riga che specifica la posizione e le dimensioni dell'area di visualizzazione video nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6b76f-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="6b76f-114">È possibile usare il modello seguente per la sezione video del file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="6b76f-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="6b76f-115">Le sezioni seguenti forniscono ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="6b76f-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="6b76f-116">Posizione video</span><span class="sxs-lookup"><span data-stu-id="6b76f-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="6b76f-117">Origine immagine video</span><span class="sxs-lookup"><span data-stu-id="6b76f-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="6b76f-118">Dimensioni del video</span><span class="sxs-lookup"><span data-stu-id="6b76f-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="6b76f-119">Sezione video di esempio</span><span class="sxs-lookup"><span data-stu-id="6b76f-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="6b76f-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6b76f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b76f-121">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="6b76f-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




