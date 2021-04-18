---
title: Attributo AlbumIDAlbumArtist
description: L'attributo AlbumIDAlbumArtist è un identificatore univoco per l'album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Attributo AlbumIDAlbumArtist Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331418"
---
# <a name="albumidalbumartist-attribute"></a><span data-ttu-id="41669-104">Attributo AlbumIDAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="41669-104">AlbumIDAlbumArtist Attribute</span></span>

<span data-ttu-id="41669-105">L'attributo **AlbumIDAlbumArtist** è un identificatore univoco per l'album.</span><span class="sxs-lookup"><span data-stu-id="41669-105">The **AlbumIDAlbumArtist** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="41669-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="41669-106">Applies To</span></span>

-   [<span data-ttu-id="41669-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="41669-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="41669-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="41669-108">Remarks</span></span>

<span data-ttu-id="41669-109">Questo attributo viene archiviato solo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="41669-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="41669-110">L'identificatore univoco è una combinazione del titolo dell'album e del nome dell'artista dell'album.</span><span class="sxs-lookup"><span data-stu-id="41669-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="41669-111">In questo attributo, il nome dell'artista dell'album viene visualizzato per primo.</span><span class="sxs-lookup"><span data-stu-id="41669-111">In this attribute, the album artist name comes first.</span></span> <span data-ttu-id="41669-112">Quando si usa il metodo [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) per ottenere un oggetto **StringCollection** usando questo attributo, i valori vengono ordinati in base al nome dell'artista dell'album.</span><span class="sxs-lookup"><span data-stu-id="41669-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album artist name.</span></span>

<span data-ttu-id="41669-113">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="41669-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="41669-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41669-114">Requirements</span></span>



| <span data-ttu-id="41669-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="41669-115">Requirement</span></span> | <span data-ttu-id="41669-116">Valore</span><span class="sxs-lookup"><span data-stu-id="41669-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="41669-117">Versione</span><span class="sxs-lookup"><span data-stu-id="41669-117">Version</span></span><br/> | <span data-ttu-id="41669-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="41669-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41669-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41669-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41669-120">**Attributo AlbumID**</span><span class="sxs-lookup"><span data-stu-id="41669-120">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="41669-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="41669-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





