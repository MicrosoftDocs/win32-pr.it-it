---
title: Attributo AlbumID
description: L'attributo AlbumID è un identificatore univoco per l'album.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Attributo AlbumID Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333774"
---
# <a name="albumid-attribute"></a><span data-ttu-id="3a0c2-104">Attributo AlbumID</span><span class="sxs-lookup"><span data-stu-id="3a0c2-104">AlbumID Attribute</span></span>

<span data-ttu-id="3a0c2-105">L'attributo **AlbumID** è un identificatore univoco per l'album.</span><span class="sxs-lookup"><span data-stu-id="3a0c2-105">The **AlbumID** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3a0c2-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="3a0c2-106">Applies To</span></span>

-   [<span data-ttu-id="3a0c2-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="3a0c2-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3a0c2-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a0c2-108">Remarks</span></span>

<span data-ttu-id="3a0c2-109">Questo attributo viene archiviato solo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="3a0c2-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="3a0c2-110">L'identificatore univoco è una combinazione del titolo dell'album e del nome dell'artista dell'album.</span><span class="sxs-lookup"><span data-stu-id="3a0c2-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="3a0c2-111">In questo attributo, il titolo dell'album viene visualizzato per primo.</span><span class="sxs-lookup"><span data-stu-id="3a0c2-111">In this attribute, the album title comes first.</span></span> <span data-ttu-id="3a0c2-112">Quando si utilizza il metodo [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) per ottenere un oggetto **StringCollection** utilizzando questo attributo, i valori vengono ordinati in base al titolo dell'album.</span><span class="sxs-lookup"><span data-stu-id="3a0c2-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album title.</span></span>

<span data-ttu-id="3a0c2-113">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3a0c2-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a0c2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a0c2-114">Requirements</span></span>



| <span data-ttu-id="3a0c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a0c2-115">Requirement</span></span> | <span data-ttu-id="3a0c2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3a0c2-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3a0c2-117">Versione</span><span class="sxs-lookup"><span data-stu-id="3a0c2-117">Version</span></span><br/> | <span data-ttu-id="3a0c2-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3a0c2-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a0c2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a0c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0c2-120">**Attributo AlbumIDAlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="3a0c2-120">**AlbumIDAlbumArtist Attribute**</span></span>](albumidalbumartist-attribute.md)
</dt> <dt>

[<span data-ttu-id="3a0c2-121">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="3a0c2-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





