---
title: EFFECTs. fullScreen
description: L'attributo fullScreen Specifica o recupera un valore che indica se la visualizzazione corrente è visualizzata a schermo intero. Questo attributo può essere impostato solo in fase di esecuzione.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFETTI. Windows fullScreen Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332558"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="1c7d8-105">EFFECTs. fullScreen</span><span class="sxs-lookup"><span data-stu-id="1c7d8-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="1c7d8-106">L'attributo **FullScreen** specifica o recupera un valore che indica se la visualizzazione corrente è visualizzata a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="1c7d8-107">Questo attributo può essere impostato solo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="1c7d8-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1c7d8-108">Possible Values</span></span>

<span data-ttu-id="1c7d8-109">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1c7d8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1c7d8-110">Value</span></span> | <span data-ttu-id="1c7d8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c7d8-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="1c7d8-112">true</span><span class="sxs-lookup"><span data-stu-id="1c7d8-112">true</span></span>  | <span data-ttu-id="1c7d8-113">La visualizzazione viene visualizzata a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="1c7d8-114">false</span><span class="sxs-lookup"><span data-stu-id="1c7d8-114">false</span></span> | <span data-ttu-id="1c7d8-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-115">Default.</span></span> <span data-ttu-id="1c7d8-116">La visualizzazione non viene visualizzata a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1c7d8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c7d8-117">Remarks</span></span>

<span data-ttu-id="1c7d8-118">Una visualizzazione può essere inserita in modalità schermo intero solo quando il supporto viene riprodotto o sospeso.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="1c7d8-119">Se il *lettore*. **currentMedia** è un video, deve essere presente un plug-in video.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="1c7d8-120">Se è audio, deve essere presente un plug-in di visualizzazione che supporta la visualizzazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="1c7d8-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7d8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c7d8-121">Requirements</span></span>



| <span data-ttu-id="1c7d8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c7d8-122">Requirement</span></span> | <span data-ttu-id="1c7d8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1c7d8-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1c7d8-124">Versione</span><span class="sxs-lookup"><span data-stu-id="1c7d8-124">Version</span></span><br/> | <span data-ttu-id="1c7d8-125">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="1c7d8-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c7d8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c7d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c7d8-127">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="1c7d8-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





