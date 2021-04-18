---
title: PLAYLIST. setCheckedState
description: Il metodo setCheckedState specifica che l'elemento indicizzato nella playlist è selezionato.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST. setCheckedState Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324459"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="fe98b-104">PLAYLIST. setCheckedState</span><span class="sxs-lookup"><span data-stu-id="fe98b-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="fe98b-105">Il metodo **setCheckedState** specifica che l'elemento indicizzato nella playlist è selezionato.</span><span class="sxs-lookup"><span data-stu-id="fe98b-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="fe98b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe98b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe98b-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="fe98b-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="fe98b-108">**Numero** (**Long**) che indica l'indice dell'elemento della playlist da verificare.</span><span class="sxs-lookup"><span data-stu-id="fe98b-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe98b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe98b-109">Return Value</span></span>

<span data-ttu-id="fe98b-110">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="fe98b-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe98b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe98b-111">Remarks</span></span>

<span data-ttu-id="fe98b-112">È possibile impostare tutti gli elementi sullo stato selezionato specificando 1 nel parametro *Item* .</span><span class="sxs-lookup"><span data-stu-id="fe98b-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="fe98b-113">Questo metodo è stato sostituito da **setCheckedState2**, che supporta le playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="fe98b-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe98b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe98b-114">Requirements</span></span>



| <span data-ttu-id="fe98b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe98b-115">Requirement</span></span> | <span data-ttu-id="fe98b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fe98b-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fe98b-117">Versione</span><span class="sxs-lookup"><span data-stu-id="fe98b-117">Version</span></span><br/> | <span data-ttu-id="fe98b-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="fe98b-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe98b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe98b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe98b-120">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="fe98b-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="fe98b-121">**PLAYLIST. setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="fe98b-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





