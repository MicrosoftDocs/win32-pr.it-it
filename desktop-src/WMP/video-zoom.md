---
title: VIDEO. zoom
description: L'attributo zoom specifica la percentuale in base alla quale ridimensionare il video.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. Zoom Media Player Windows
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324080"
---
# <a name="videozoom"></a><span data-ttu-id="df390-104">VIDEO. zoom</span><span class="sxs-lookup"><span data-stu-id="df390-104">VIDEO.zoom</span></span>

<span data-ttu-id="df390-105">L'attributo **Zoom** specifica la percentuale in base alla quale ridimensionare il video.</span><span class="sxs-lookup"><span data-stu-id="df390-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="df390-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="df390-106">Possible Values</span></span>

<span data-ttu-id="df390-107">Questo attributo è un **numero** di lettura/scrittura (**Long**) compreso tra 1 e le dimensioni massime consentite dalla larghezza e dall'altezza del controllo video.</span><span class="sxs-lookup"><span data-stu-id="df390-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="df390-108">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="df390-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="df390-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="df390-109">Remarks</span></span>

<span data-ttu-id="df390-110">Questo attributo non può essere usato in combinazione con l'attributo **FullScreen** .</span><span class="sxs-lookup"><span data-stu-id="df390-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="df390-111">Se si specifica **Width** e **Height** e la finestra video risultante è più grande del video riprodotto, è possibile aumentare le dimensioni del video scalando fino alla dimensione massima consentita dalla finestra.</span><span class="sxs-lookup"><span data-stu-id="df390-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="df390-112">Se non si specifica **Width** e **Height** , **lo zoom** è limitato ai valori di 100 o meno.</span><span class="sxs-lookup"><span data-stu-id="df390-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="df390-113">Se la proprietà **shrinkToFit** è impostata su false, il video verrà modificato proporzionalmente allo zoom, per adattarsi allo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="df390-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="df390-114">Se **shrinkToFit** è true, il video verrà compattato per adattarsi alla dimensione più restrittiva, mantenendo le proporzioni originali.</span><span class="sxs-lookup"><span data-stu-id="df390-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="df390-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df390-115">Requirements</span></span>



| <span data-ttu-id="df390-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="df390-116">Requirement</span></span> | <span data-ttu-id="df390-117">Valore</span><span class="sxs-lookup"><span data-stu-id="df390-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="df390-118">Versione</span><span class="sxs-lookup"><span data-stu-id="df390-118">Version</span></span><br/> | <span data-ttu-id="df390-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="df390-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df390-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df390-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df390-121">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="df390-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="df390-122">**VIDEO. fullScreen**</span><span class="sxs-lookup"><span data-stu-id="df390-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="df390-123">**VIDEO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="df390-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 





