---
title: Attributo WM/AlbumCoverURL
description: L'attributo WM/AlbumCoverURL è l'URL (Uniform Resource Locator) per l'immagine dell'album o un'anteprima.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Media Player Windows per gli attributi WM/AlbumCoverURL
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327038"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="259f3-104">Attributo WM/AlbumCoverURL</span><span class="sxs-lookup"><span data-stu-id="259f3-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="259f3-105">L'attributo **WM/AlbumCoverURL** è l'URL (Uniform Resource Locator) per l'immagine dell'album o un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="259f3-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="259f3-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="259f3-106">Applies To</span></span>

-   [<span data-ttu-id="259f3-107">**Elementi audio**</span><span class="sxs-lookup"><span data-stu-id="259f3-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="259f3-108">**Elementi foto**</span><span class="sxs-lookup"><span data-stu-id="259f3-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="259f3-109">**Elementi video**</span><span class="sxs-lookup"><span data-stu-id="259f3-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="259f3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="259f3-110">Remarks</span></span>

<span data-ttu-id="259f3-111">Per un elemento audio, questo attributo è l'URL dell'immagine dell'album.</span><span class="sxs-lookup"><span data-stu-id="259f3-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="259f3-112">Per un elemento Photo o video, questo attributo è l'URL di un'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="259f3-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="259f3-113">Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="259f3-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="259f3-114">È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica.</span><span class="sxs-lookup"><span data-stu-id="259f3-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="259f3-115">Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="259f3-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="259f3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="259f3-116">Requirements</span></span>



| <span data-ttu-id="259f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="259f3-117">Requirement</span></span> | <span data-ttu-id="259f3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="259f3-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="259f3-119">Versione</span><span class="sxs-lookup"><span data-stu-id="259f3-119">Version</span></span><br/> | <span data-ttu-id="259f3-120">Windows Media Player 12 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="259f3-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="259f3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="259f3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259f3-122">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="259f3-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





