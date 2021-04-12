---
description: La clip epecifies un'origine multimediale.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Elemento clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480996"
---
# <a name="clip-element"></a><span data-ttu-id="b8c63-103">Elemento clip</span><span class="sxs-lookup"><span data-stu-id="b8c63-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="b8c63-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b8c63-104">\[Deprecated.</span></span> <span data-ttu-id="b8c63-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8c63-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8c63-106">`clip`Epecifies un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="b8c63-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="b8c63-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="b8c63-107">Attributes</span></span>

<span data-ttu-id="b8c63-108">[**CLSID**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**Lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b8c63-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="b8c63-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="b8c63-109">Parent/Child Information</span></span>



|          |                                  |
|----------|----------------------------------|
| <span data-ttu-id="b8c63-110">Padre</span><span class="sxs-lookup"><span data-stu-id="b8c63-110">Parent</span></span>   | [<span data-ttu-id="b8c63-111">**tenere traccia**</span><span class="sxs-lookup"><span data-stu-id="b8c63-111">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="b8c63-112">Children</span><span class="sxs-lookup"><span data-stu-id="b8c63-112">Children</span></span> | [<span data-ttu-id="b8c63-113">**effetto**</span><span class="sxs-lookup"><span data-stu-id="b8c63-113">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="b8c63-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8c63-114">Remarks</span></span>

<span data-ttu-id="b8c63-115">L'attributo **CLSID** specifica il CLSID di un filtro di origine da utilizzare come origine.</span><span class="sxs-lookup"><span data-stu-id="b8c63-115">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="b8c63-116">Non specificare gli attributi **src** e **CLSID** nello stesso `clip` elemento.</span><span class="sxs-lookup"><span data-stu-id="b8c63-116">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="b8c63-117">Specificare almeno un attributo di inizio-ora (**Start** o **mstart**) e un attributo dell'ora di arresto (**Stop** o **mstop**).</span><span class="sxs-lookup"><span data-stu-id="b8c63-117">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="b8c63-118">Se uno degli attributi della fase di avvio non è specificato, il valore predefinito è 0 (l'inizio della sequenza temporale per l' **avvio** o l'inizio della clip per **mstart**).</span><span class="sxs-lookup"><span data-stu-id="b8c63-118">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="b8c63-119">Se uno degli attributi dell'ora di arresto non è specificato, DES presuppone una frequenza di riproduzione normale e calcola di conseguenza l'ora di arresto non specificata.</span><span class="sxs-lookup"><span data-stu-id="b8c63-119">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="b8c63-120">Se vengono specificate entrambe le ore di arresto, la riproduzione è più veloce o più lenta del normale, se necessario.</span><span class="sxs-lookup"><span data-stu-id="b8c63-120">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="b8c63-121">Nell'esempio seguente la durata della sequenza temporale è di sette secondi (**Stop** minus **Start**).</span><span class="sxs-lookup"><span data-stu-id="b8c63-121">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="b8c63-122">Si presuppone una frequenza di riproduzione normale, quindi il tempo di arresto del supporto predefinito è di 10 secondi (durata più **mstart**).</span><span class="sxs-lookup"><span data-stu-id="b8c63-122">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="b8c63-123">Nell'esempio seguente l'ora di inizio del supporto viene impostata su 0, forzando la durata dei supporti su 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="b8c63-123">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="b8c63-124">La durata della sequenza temporale è di cinque secondi, quindi la clip viene riprodotta al doppio della normale frequenza.</span><span class="sxs-lookup"><span data-stu-id="b8c63-124">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="b8c63-125">Se l'attributo **src** specifica un'immagine ancora, des tenta di caricare una serie di immagini ancora per creare un'animazione.</span><span class="sxs-lookup"><span data-stu-id="b8c63-125">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="b8c63-126">Se, ad esempio, l'attributo **src** è IMAGE001.BMP, DES Cerca IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP e così via.</span><span class="sxs-lookup"><span data-stu-id="b8c63-126">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="b8c63-127">Supponendo che esistano, vengono visualizzati in ordine numerico sequenziale, alla velocità specificata dall'attributo **framerate** .</span><span class="sxs-lookup"><span data-stu-id="b8c63-127">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="b8c63-128">Esempi</span><span class="sxs-lookup"><span data-stu-id="b8c63-128">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="b8c63-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b8c63-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c63-130">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="b8c63-130">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



