---
title: PLAYLIST. itemMedia
description: L'attributo itemMedia recupera l'oggetto multimediale corrispondente all'indice specificato nell'elemento PLAYLIST.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST. itemMedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327622"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="ae65c-104">PLAYLIST. itemMedia</span><span class="sxs-lookup"><span data-stu-id="ae65c-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="ae65c-105">L'attributo **itemMedia** recupera l'oggetto **multimediale** corrispondente all'indice specificato nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="ae65c-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="ae65c-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ae65c-106">Possible Values</span></span>

<span data-ttu-id="ae65c-107">Questo attributo è un oggetto **multimediale** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ae65c-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae65c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae65c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae65c-109"><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="ae65c-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="ae65c-110">**Numero**(**Long**) che contiene l'indice di un elemento della playlist.</span><span class="sxs-lookup"><span data-stu-id="ae65c-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae65c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae65c-111">Remarks</span></span>

<span data-ttu-id="ae65c-112">La proprietà **itemMedia** restituirà oggetti multimediali espansi nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="ae65c-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="ae65c-113">Se, ad esempio, è presente una playlist che contiene tre clip multimediali non espanse nell'elemento **playlist** , **itemMedia**(0) restituirà la playlist come oggetto multimediale.</span><span class="sxs-lookup"><span data-stu-id="ae65c-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="ae65c-114">Se la playlist è espansa, **itemMedia**(0) restituirà il primo clip multimediale nella playlist.</span><span class="sxs-lookup"><span data-stu-id="ae65c-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae65c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae65c-115">Requirements</span></span>



| <span data-ttu-id="ae65c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae65c-116">Requirement</span></span> | <span data-ttu-id="ae65c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ae65c-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ae65c-118">Versione</span><span class="sxs-lookup"><span data-stu-id="ae65c-118">Version</span></span><br/> | <span data-ttu-id="ae65c-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ae65c-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae65c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae65c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae65c-121">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="ae65c-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ae65c-122">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="ae65c-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





