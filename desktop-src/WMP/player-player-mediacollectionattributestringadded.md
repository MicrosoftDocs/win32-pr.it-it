---
title: Evento Player. MediaCollectionAttributeStringAdded
description: L'evento MediaCollectionAttributeStringAdded si verifica quando un valore di attributo viene aggiunto alla libreria. | Evento Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Media Player di Windows Event MediaCollectionAttributeStringAdded
- Windows Event MediaCollectionAttributeStringAdded Media Player, classe Player
- Classe Player Windows Media Player, evento MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331852"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="0768e-107">Evento Player. MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="0768e-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="0768e-108">L'evento **MediaCollectionAttributeStringAdded** si verifica quando un valore di attributo viene aggiunto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="0768e-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="0768e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0768e-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="0768e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0768e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0768e-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="0768e-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="0768e-112">**Stringa** che specifica il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="0768e-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="0768e-113">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0768e-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="0768e-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="0768e-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0768e-115">**Stringa** che specifica il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="0768e-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0768e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0768e-116">Return value</span></span>

<span data-ttu-id="0768e-117">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0768e-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0768e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0768e-118">Remarks</span></span>

<span data-ttu-id="0768e-119">Quando un elemento multimediale viene aggiunto alla libreria, i relativi metadati vengono aggiunti all'oggetto **mediacollection** e questo evento viene generato per ogni attributo aggiunto.</span><span class="sxs-lookup"><span data-stu-id="0768e-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="0768e-120">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="0768e-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0768e-121">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="0768e-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="0768e-122">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0768e-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0768e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0768e-123">Requirements</span></span>



| <span data-ttu-id="0768e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0768e-124">Requirement</span></span> | <span data-ttu-id="0768e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0768e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0768e-126">Versione</span><span class="sxs-lookup"><span data-stu-id="0768e-126">Version</span></span><br/> | <span data-ttu-id="0768e-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="0768e-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0768e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0768e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="0768e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0768e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0768e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0768e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0768e-131">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="0768e-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="0768e-132">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="0768e-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0768e-133">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="0768e-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





