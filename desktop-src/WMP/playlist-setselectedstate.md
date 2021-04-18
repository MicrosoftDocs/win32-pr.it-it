---
title: PLAYLIST. setSelectedState
description: Il metodo setSelectedState specifica che l'elemento indicizzato nella playlist è selezionato.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- PLAYLIST. setSelectedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333838"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="62364-104">PLAYLIST. setSelectedState</span><span class="sxs-lookup"><span data-stu-id="62364-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="62364-105">Il metodo **setSelectedState** specifica che l'elemento indicizzato nella playlist è selezionato.</span><span class="sxs-lookup"><span data-stu-id="62364-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="62364-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62364-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62364-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="62364-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="62364-108">**Numero** (**Long**) che indica l'indice di un elemento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="62364-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62364-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62364-109">Return Value</span></span>

<span data-ttu-id="62364-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="62364-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62364-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="62364-111">Remarks</span></span>

<span data-ttu-id="62364-112">È possibile impostare tutti gli elementi sullo stato selezionato specificando 1 nel parametro *Item* .</span><span class="sxs-lookup"><span data-stu-id="62364-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="62364-113">Questo metodo è stato sostituito da **setSelectedState2**, che supporta le playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="62364-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="62364-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62364-114">Requirements</span></span>



| <span data-ttu-id="62364-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="62364-115">Requirement</span></span> | <span data-ttu-id="62364-116">Valore</span><span class="sxs-lookup"><span data-stu-id="62364-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="62364-117">Versione</span><span class="sxs-lookup"><span data-stu-id="62364-117">Version</span></span><br/> | <span data-ttu-id="62364-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="62364-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62364-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62364-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62364-120">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="62364-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="62364-121">**PLAYLIST. setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="62364-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





