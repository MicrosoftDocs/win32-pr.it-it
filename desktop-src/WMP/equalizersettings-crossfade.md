---
title: EQUALIZERSETTINGS. dissolvenza
description: L'attributo crossfader specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. dissolvenza Media Player Windows
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333127"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="ccfee-104">EQUALIZERSETTINGS. dissolvenza</span><span class="sxs-lookup"><span data-stu-id="ccfee-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="ccfee-105">L'attributo **crossfader** specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ccfee-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="ccfee-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ccfee-106">Possible Values</span></span>

<span data-ttu-id="ccfee-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ccfee-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="ccfee-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ccfee-108">Value</span></span> | <span data-ttu-id="ccfee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccfee-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="ccfee-110">true</span><span class="sxs-lookup"><span data-stu-id="ccfee-110">true</span></span>  | <span data-ttu-id="ccfee-111">La dissolvenza incrociata è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ccfee-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="ccfee-112">false</span><span class="sxs-lookup"><span data-stu-id="ccfee-112">false</span></span> | <span data-ttu-id="ccfee-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ccfee-113">Default.</span></span> <span data-ttu-id="ccfee-114">La dissolvenza incrociata è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ccfee-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ccfee-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccfee-115">Remarks</span></span>

<span data-ttu-id="ccfee-116">La dissolvenza incrociata è una funzionalità di elaborazione audio che riduce gradualmente il volume di un elemento multimediale vicino alla fine della riproduzione, avviando contemporaneamente la riproduzione del successivo elemento multimediale al volume minimo e aumentando gradualmente il volume al volume normale.</span><span class="sxs-lookup"><span data-stu-id="ccfee-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="ccfee-117">La sovrapposizione tra l'inizio del secondo elemento multimediale e la fine del primo elemento multimediale viene specificata dall'attributo **crossFadeWindow** .</span><span class="sxs-lookup"><span data-stu-id="ccfee-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccfee-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccfee-118">Requirements</span></span>



| <span data-ttu-id="ccfee-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccfee-119">Requirement</span></span> | <span data-ttu-id="ccfee-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ccfee-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ccfee-121">Versione</span><span class="sxs-lookup"><span data-stu-id="ccfee-121">Version</span></span><br/> | <span data-ttu-id="ccfee-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ccfee-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccfee-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccfee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccfee-124">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="ccfee-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="ccfee-125">**EQUALIZERSETTINGS.crossFadeWindow**</span><span class="sxs-lookup"><span data-stu-id="ccfee-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





