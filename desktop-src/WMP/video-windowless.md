---
title: VIDEO. senza finestra
description: L'attributo senza finestra specifica o recupera un valore che indica se il controllo video sarà finestra o senza finestra; ovvero se l'intero rettangolo del controllo sarà sempre visibile o possa essere ritagliato.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO. finestre senza finestra Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328289"
---
# <a name="videowindowless"></a><span data-ttu-id="68c89-104">VIDEO. senza finestra</span><span class="sxs-lookup"><span data-stu-id="68c89-104">VIDEO.windowless</span></span>

<span data-ttu-id="68c89-105">L'attributo senza **finestra** specifica o recupera un valore che indica se il controllo video sarà finestra o senza finestra; ovvero se l'intero rettangolo del controllo sarà sempre visibile o possa essere ritagliato.</span><span class="sxs-lookup"><span data-stu-id="68c89-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="68c89-106">Può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="68c89-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="68c89-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="68c89-107">Possible Values</span></span>

<span data-ttu-id="68c89-108">Questo attributo è un **valore booleano** specificato in fase di progettazione e di sola lettura in seguito.</span><span class="sxs-lookup"><span data-stu-id="68c89-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="68c89-109">Valore</span><span class="sxs-lookup"><span data-stu-id="68c89-109">Value</span></span> | <span data-ttu-id="68c89-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68c89-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="68c89-111">true</span><span class="sxs-lookup"><span data-stu-id="68c89-111">true</span></span>  | <span data-ttu-id="68c89-112">Il controllo video sarà privo di finestra.</span><span class="sxs-lookup"><span data-stu-id="68c89-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="68c89-113">false</span><span class="sxs-lookup"><span data-stu-id="68c89-113">false</span></span> | <span data-ttu-id="68c89-114">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="68c89-114">Default.</span></span> <span data-ttu-id="68c89-115">Il controllo video sarà a finestre.</span><span class="sxs-lookup"><span data-stu-id="68c89-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="68c89-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="68c89-116">Remarks</span></span>

<span data-ttu-id="68c89-117">Se si desidera una finestra video non rettangolare o si desidera coprire qualsiasi parte della finestra video con un'immagine, questo attributo deve essere impostato su true.</span><span class="sxs-lookup"><span data-stu-id="68c89-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="68c89-118">In questo modo si sacrificano alcune prestazioni per eseguire il troncamento necessario.</span><span class="sxs-lookup"><span data-stu-id="68c89-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="68c89-119">La riproduzione video è ottimizzata per la riproduzione non ritagliata.</span><span class="sxs-lookup"><span data-stu-id="68c89-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="68c89-120">In questo caso, l'attributo senza **finestra** è impostato su false e l'intero rettangolo video viene sempre visualizzato.</span><span class="sxs-lookup"><span data-stu-id="68c89-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="68c89-121">Qualsiasi immagine che copre la finestra video viene ignorata e la finestra del video ha l'ordine z di livello più alto.</span><span class="sxs-lookup"><span data-stu-id="68c89-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c89-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68c89-122">Requirements</span></span>



| <span data-ttu-id="68c89-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c89-123">Requirement</span></span> | <span data-ttu-id="68c89-124">Valore</span><span class="sxs-lookup"><span data-stu-id="68c89-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="68c89-125">Versione</span><span class="sxs-lookup"><span data-stu-id="68c89-125">Version</span></span><br/> | <span data-ttu-id="68c89-126">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="68c89-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68c89-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68c89-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c89-128">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="68c89-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





