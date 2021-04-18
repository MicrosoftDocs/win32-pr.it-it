---
title: PLAYLIST. backgroundImage
description: L'attributo backgroundImage specifica o recupera l'immagine di sfondo.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- PLAYLIST. backgroundImage Media Player Windows
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329599"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="8eae3-104">PLAYLIST. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="8eae3-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="8eae3-105">L'attributo **BackgroundImage** specifica o recupera l'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="8eae3-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="8eae3-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8eae3-106">Possible Values</span></span>

<span data-ttu-id="8eae3-107">Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="8eae3-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="8eae3-108">e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8eae3-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eae3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eae3-109">Remarks</span></span>

<span data-ttu-id="8eae3-110">Se l'altezza e la larghezza dell'immagine sono inferiori all'altezza e alla larghezza dell'elemento della **playlist** , viene affiancata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8eae3-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="8eae3-111">I formati supportati sono BMP, JPG, GIF e PNG.</span><span class="sxs-lookup"><span data-stu-id="8eae3-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="8eae3-112">Se si specifica il valore "gradiente" per l'immagine di sfondo, lo sfondo della playlist viene visualizzato come sfumatura di colore.</span><span class="sxs-lookup"><span data-stu-id="8eae3-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="8eae3-113">Ciò significa che il colore di sfondo passa gradualmente tra i valori [playlist. BackgroundColor](playlist-backgroundcolor.md) (nella parte superiore dello sfondo) e [playlist. statusColor](playlist-statuscolor.md) .</span><span class="sxs-lookup"><span data-stu-id="8eae3-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eae3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eae3-114">Requirements</span></span>



| <span data-ttu-id="8eae3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eae3-115">Requirement</span></span> | <span data-ttu-id="8eae3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8eae3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eae3-117">Versione</span><span class="sxs-lookup"><span data-stu-id="8eae3-117">Version</span></span><br/> | <span data-ttu-id="8eae3-118">Windows Media Player versione 7,0 o successiva, Windows Media Player 10 per la funzionalità gradiente</span><span class="sxs-lookup"><span data-stu-id="8eae3-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8eae3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eae3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eae3-120">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="8eae3-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





