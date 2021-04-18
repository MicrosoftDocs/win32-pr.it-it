---
title: TrackBar
description: TrackBar
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Mobile Skins, trackbars
- interfacce, TrackBar
- riferimento per Skin, trackbars
- trackbars in Skin, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298649"
---
# <a name="trackbars"></a><span data-ttu-id="95124-107">TrackBar</span><span class="sxs-lookup"><span data-stu-id="95124-107">Trackbars</span></span>

<span data-ttu-id="95124-108">Un TrackBar Visualizza un'immagine che cambia in piccoli incrementi.</span><span class="sxs-lookup"><span data-stu-id="95124-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="95124-109">Gli TrackBar vengono utilizzati per i controlli volume e la posizione di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="95124-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="95124-110">È possibile utilizzare gli oggetti TrackBar per visualizzare informazioni sull'elemento multimediale corrente o per consentire all'utente di modificare le impostazioni o la posizione di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="95124-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="95124-111">Ad esempio, è possibile utilizzare un TrackBar per consentire all'utente di modificare il volume e un altro TrackBar in grado di mostrare all'utente la posizione di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="95124-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="95124-112">Gli TrackBar hanno un'immagine Thumb che definisce l'impostazione corrente del valore TrackBar.</span><span class="sxs-lookup"><span data-stu-id="95124-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="95124-113">La sezione trackbars del file di definizione Skin deve iniziare con questa riga:</span><span class="sxs-lookup"><span data-stu-id="95124-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="95124-114">È quindi necessario aggiungere una o più righe che contengono informazioni su ogni TrackBar nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="95124-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="95124-115">È possibile usare il modello seguente per la sezione trackbars del file di definizione dell'interfaccia utente:</span><span class="sxs-lookup"><span data-stu-id="95124-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="95124-116">È necessario utilizzare l'ordine seguente per le informazioni di TrackBar per ogni riga nella sezione trackbars (ogni parte della riga è obbligatoria):</span><span class="sxs-lookup"><span data-stu-id="95124-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="95124-117">Tipo TrackBar</span><span class="sxs-lookup"><span data-stu-id="95124-117">Trackbar Type</span></span>](trackbar-type.md)
2.  [<span data-ttu-id="95124-118">Posizione TrackBar</span><span class="sxs-lookup"><span data-stu-id="95124-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="95124-119">Origine immagine per TrackBar disabilitato</span><span class="sxs-lookup"><span data-stu-id="95124-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="95124-120">Origine immagine Thumb</span><span class="sxs-lookup"><span data-stu-id="95124-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="95124-121">Dimensioni Thumb</span><span class="sxs-lookup"><span data-stu-id="95124-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="95124-122">Per un esempio di codice trackbars, vedere la [sezione Sample trackbars](sample-trackbars-section.md).</span><span class="sxs-lookup"><span data-stu-id="95124-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95124-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95124-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95124-124">**Riferimento all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="95124-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




