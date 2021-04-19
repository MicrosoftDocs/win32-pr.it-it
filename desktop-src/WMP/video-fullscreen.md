---
title: VIDEO. fullScreen
description: L'attributo fullScreen Specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO. Windows fullScreen Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330104"
---
# <a name="videofullscreen"></a><span data-ttu-id="cf4f1-104">VIDEO. fullScreen</span><span class="sxs-lookup"><span data-stu-id="cf4f1-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="cf4f1-105">L'attributo **FullScreen** specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="cf4f1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="cf4f1-106">Possible Values</span></span>

<span data-ttu-id="cf4f1-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="cf4f1-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cf4f1-108">Value</span></span> | <span data-ttu-id="cf4f1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf4f1-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="cf4f1-110">true</span><span class="sxs-lookup"><span data-stu-id="cf4f1-110">true</span></span>  | <span data-ttu-id="cf4f1-111">Il video viene visualizzato in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="cf4f1-112">false</span><span class="sxs-lookup"><span data-stu-id="cf4f1-112">false</span></span> | <span data-ttu-id="cf4f1-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-113">Default.</span></span> <span data-ttu-id="cf4f1-114">Il video non viene visualizzato in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cf4f1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf4f1-115">Remarks</span></span>

<span data-ttu-id="cf4f1-116">Questa proprietà può essere specificata solo in fase di esecuzione, dopo il caricamento di un file.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="cf4f1-117">Deve pertanto essere impostato in un gestore eventi di script.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="cf4f1-118">Il pulsante escape viene usato per tornare alla visualizzazione normale.</span><span class="sxs-lookup"><span data-stu-id="cf4f1-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4f1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf4f1-119">Requirements</span></span>



| <span data-ttu-id="cf4f1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf4f1-120">Requirement</span></span> | <span data-ttu-id="cf4f1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cf4f1-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cf4f1-122">Versione</span><span class="sxs-lookup"><span data-stu-id="cf4f1-122">Version</span></span><br/> | <span data-ttu-id="cf4f1-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="cf4f1-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf4f1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf4f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4f1-125">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="cf4f1-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="cf4f1-126">**VIDEO. maintainAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="cf4f1-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="cf4f1-127">**VIDEO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="cf4f1-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="cf4f1-128">**VIDEO. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="cf4f1-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





