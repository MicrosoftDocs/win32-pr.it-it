---
description: Il clip epecifica un'origine multimediale.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908669"
---
# <a name="clip-element"></a><span data-ttu-id="1bce1-103">Elemento clip</span><span class="sxs-lookup"><span data-stu-id="1bce1-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="1bce1-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1bce1-104">\[Deprecated.</span></span> <span data-ttu-id="1bce1-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1bce1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1bce1-106">`clip`L'oggetto epecifica un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="1bce1-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="1bce1-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="1bce1-107">Attributes</span></span>

<span data-ttu-id="1bce1-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), start , [**stop**](start-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md) [](stop-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="1bce1-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="1bce1-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="1bce1-109">Parent/Child Information</span></span>



| <span data-ttu-id="1bce1-110">Label</span><span class="sxs-lookup"><span data-stu-id="1bce1-110">Label</span></span> | <span data-ttu-id="1bce1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="1bce1-111">Value</span></span> |
|----------|----------------------------------|
| <span data-ttu-id="1bce1-112">Padre</span><span class="sxs-lookup"><span data-stu-id="1bce1-112">Parent</span></span>   | [<span data-ttu-id="1bce1-113">**Traccia**</span><span class="sxs-lookup"><span data-stu-id="1bce1-113">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="1bce1-114">Children</span><span class="sxs-lookup"><span data-stu-id="1bce1-114">Children</span></span> | [<span data-ttu-id="1bce1-115">**Effetto**</span><span class="sxs-lookup"><span data-stu-id="1bce1-115">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="1bce1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bce1-116">Remarks</span></span>

<span data-ttu-id="1bce1-117">**L'attributo clsid** specifica il CLSID di un filtro di origine da usare come origine.</span><span class="sxs-lookup"><span data-stu-id="1bce1-117">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="1bce1-118">Non specificare gli attributi **src** e **clsid** all'interno dello stesso `clip` elemento.</span><span class="sxs-lookup"><span data-stu-id="1bce1-118">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="1bce1-119">Specificare almeno un attributo dell'ora di inizio (**start** o **mstart**) e un attributo stop-time (**stop** o **mstop**).</span><span class="sxs-lookup"><span data-stu-id="1bce1-119">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="1bce1-120">Se uno degli attributi dell'ora di inizio non è specificato, il valore predefinito è 0 (l'inizio della sequenza temporale per **start** o l'inizio del clip per **mstart**).</span><span class="sxs-lookup"><span data-stu-id="1bce1-120">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="1bce1-121">Se uno degli attributi del tempo di arresto non è specificato, DES presuppone una velocità di riproduzione normale e calcola di conseguenza il tempo di arresto non specificato.</span><span class="sxs-lookup"><span data-stu-id="1bce1-121">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="1bce1-122">Se vengono specificati entrambi i tempi di arresto, la riproduzione è più veloce o più lenta del normale, se necessario.</span><span class="sxs-lookup"><span data-stu-id="1bce1-122">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="1bce1-123">Nell'esempio seguente la durata della sequenza temporale è di sette secondi (**stop** meno **start**).</span><span class="sxs-lookup"><span data-stu-id="1bce1-123">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="1bce1-124">Si presuppone la frequenza di riproduzione normale, quindi il tempo di arresto multimediale è 10 secondi (durata più **mstart**).</span><span class="sxs-lookup"><span data-stu-id="1bce1-124">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="1bce1-125">Nell'esempio successivo l'ora di inizio del supporto è impostata su 0, forzando la durata del supporto a 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="1bce1-125">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="1bce1-126">La durata della sequenza temporale è di cinque secondi, quindi il clip viene riprodotto al doppio della frequenza normale.</span><span class="sxs-lookup"><span data-stu-id="1bce1-126">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="1bce1-127">Se **l'attributo src** specifica un'immagine fisse, DES tenta di caricare una serie di immagini fisse per creare un'animazione.</span><span class="sxs-lookup"><span data-stu-id="1bce1-127">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="1bce1-128">Ad esempio, se **l'attributo src** è IMAGE001.BMP, DES cerca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e così via.</span><span class="sxs-lookup"><span data-stu-id="1bce1-128">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="1bce1-129">Supponendo che esistano, vengono visualizzati in ordine numerico sequenziale, alla frequenza specificata **dall'attributo framerate.**</span><span class="sxs-lookup"><span data-stu-id="1bce1-129">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="1bce1-130">Esempi</span><span class="sxs-lookup"><span data-stu-id="1bce1-130">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="1bce1-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1bce1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bce1-132">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="1bce1-132">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



