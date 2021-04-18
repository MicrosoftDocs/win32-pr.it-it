---
title: SEEKSLIDER
description: Si tratta di un dispositivo di scorrimento predefinito con i seguenti valori predefiniti. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- Media Player Windows SEEKSLIDER
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325829"
---
# <a name="seekslider"></a><span data-ttu-id="0409f-105">SEEKSLIDER</span><span class="sxs-lookup"><span data-stu-id="0409f-105">SEEKSLIDER</span></span>

<span data-ttu-id="0409f-106">Si tratta di un **dispositivo di scorrimento** predefinito con i seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0409f-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="0409f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="0409f-107">Remarks</span></span>

<span data-ttu-id="0409f-108">Viene creato un controllo **dispositivo di scorrimento** che cerca il file multimediale in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="0409f-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="0409f-109">Le descrizioni comandi sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="0409f-109">The ToolTips are localized.</span></span> <span data-ttu-id="0409f-110">Per eseguire l'override di tutte le proprietà di questo **dispositivo di scorrimento** , è possibile specificarle in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="0409f-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="0409f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0409f-111">Requirements</span></span>



| <span data-ttu-id="0409f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0409f-112">Requirement</span></span> | <span data-ttu-id="0409f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0409f-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="0409f-114">Versione</span><span class="sxs-lookup"><span data-stu-id="0409f-114">Version</span></span><br/> | <span data-ttu-id="0409f-115">Windows Media Player 7,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0409f-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0409f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0409f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0409f-117">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="0409f-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





