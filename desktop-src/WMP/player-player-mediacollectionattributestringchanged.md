---
title: Evento Player. MediaCollectionAttributeStringChanged
description: L'evento MediaCollectionAttributeStringChanged si verifica quando viene modificato un valore di attributo nella libreria. | Evento Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Media Player di Windows Event MediaCollectionAttributeStringChanged
- Windows Event MediaCollectionAttributeStringChanged Media Player, classe Player
- Classe Player Windows Media Player, evento MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326109"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="59dcf-107">Evento Player. MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="59dcf-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="59dcf-108">L'evento **MediaCollectionAttributeStringChanged** si verifica quando viene modificato un valore di attributo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="59dcf-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="59dcf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59dcf-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="59dcf-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="59dcf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59dcf-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="59dcf-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="59dcf-112">**Stringa** che specifica il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="59dcf-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="59dcf-113">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="59dcf-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="59dcf-114">*bstrOldAttribVal*</span><span class="sxs-lookup"><span data-stu-id="59dcf-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="59dcf-115">**Stringa** che specifica il valore precedente dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="59dcf-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="59dcf-116">*bstrNewAttribVal*</span><span class="sxs-lookup"><span data-stu-id="59dcf-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="59dcf-117">**Stringa** che specifica il nuovo valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="59dcf-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59dcf-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59dcf-118">Return value</span></span>

<span data-ttu-id="59dcf-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="59dcf-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59dcf-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="59dcf-120">Remarks</span></span>

<span data-ttu-id="59dcf-121">Quando un utente modifica i metadati della libreria, l'oggetto **mediacollection** viene aggiornato e questo evento viene generato per ogni attributo modificato.</span><span class="sxs-lookup"><span data-stu-id="59dcf-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="59dcf-122">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="59dcf-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="59dcf-123">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="59dcf-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="59dcf-124">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="59dcf-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="59dcf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59dcf-125">Requirements</span></span>



| <span data-ttu-id="59dcf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="59dcf-126">Requirement</span></span> | <span data-ttu-id="59dcf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="59dcf-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59dcf-128">Versione</span><span class="sxs-lookup"><span data-stu-id="59dcf-128">Version</span></span><br/> | <span data-ttu-id="59dcf-129">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="59dcf-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="59dcf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="59dcf-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="59dcf-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59dcf-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59dcf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59dcf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59dcf-133">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="59dcf-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="59dcf-134">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="59dcf-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="59dcf-135">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="59dcf-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





