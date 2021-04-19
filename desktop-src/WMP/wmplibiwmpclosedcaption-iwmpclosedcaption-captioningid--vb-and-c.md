---
title: Proprietà captioningId di IWMPClosedCaption
description: La proprietà IWMPClosedCaption Ottiene o imposta il nome dell'elemento HTML che visualizza la didascalia.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Finestra delle proprietà di captioningId Media Player
- Proprietà di captioningId Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329284"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="685d6-106">Proprietà IWMPClosedCaption:: captioningId</span><span class="sxs-lookup"><span data-stu-id="685d6-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="685d6-107">La proprietà **IWMPClosedCaption** Ottiene o imposta il nome dell'elemento HTML che visualizza la didascalia.</span><span class="sxs-lookup"><span data-stu-id="685d6-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="685d6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="685d6-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="685d6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="685d6-109">Property value</span></span>

<span data-ttu-id="685d6-110">**System. String** che rappresenta l'ID dell'elemento HTML.</span><span class="sxs-lookup"><span data-stu-id="685d6-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="685d6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="685d6-111">Remarks</span></span>

<span data-ttu-id="685d6-112">Il nome dell'elemento specificato può essere qualsiasi elemento HTML nella pagina Web, purché supporti l'attributo **innerHTML** .</span><span class="sxs-lookup"><span data-stu-id="685d6-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="685d6-113">Se la pagina Web contiene più frame, il nome dell'elemento può fare riferimento solo a un elemento nello stesso frame del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="685d6-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="685d6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="685d6-114">Requirements</span></span>



| <span data-ttu-id="685d6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="685d6-115">Requirement</span></span> | <span data-ttu-id="685d6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="685d6-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685d6-117">Versione</span><span class="sxs-lookup"><span data-stu-id="685d6-117">Version</span></span><br/>   | <span data-ttu-id="685d6-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="685d6-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="685d6-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="685d6-119">Namespace</span></span><br/> | <span data-ttu-id="685d6-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="685d6-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="685d6-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="685d6-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="685d6-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="685d6-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685d6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="685d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685d6-124">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="685d6-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="685d6-125">**Interfaccia IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="685d6-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="685d6-126">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="685d6-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





