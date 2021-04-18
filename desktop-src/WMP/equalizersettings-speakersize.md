---
title: EQUALIZERSETTINGS.speakerSize
description: L'attributo speakerSize specifica o Recupera il numero di indice della dimensione del relatore corrente.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- Media Player Windows EQUALIZERSETTINGS. speakerSize
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327303"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="1c72d-104">EQUALIZERSETTINGS.speakerSize</span><span class="sxs-lookup"><span data-stu-id="1c72d-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="1c72d-105">L'attributo **speakerSize** specifica o Recupera il numero di indice della dimensione del relatore corrente.</span><span class="sxs-lookup"><span data-stu-id="1c72d-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="1c72d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1c72d-106">Possible Values</span></span>

<span data-ttu-id="1c72d-107">Questo attributo è un **numero** di lettura/scrittura (Long) contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c72d-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="1c72d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1c72d-108">Value</span></span> | <span data-ttu-id="1c72d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c72d-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="1c72d-110">0</span><span class="sxs-lookup"><span data-stu-id="1c72d-110">0</span></span>     | <span data-ttu-id="1c72d-111">Gli altoparlanti correnti sono cuffie.</span><span class="sxs-lookup"><span data-stu-id="1c72d-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="1c72d-112">1</span><span class="sxs-lookup"><span data-stu-id="1c72d-112">1</span></span>     | <span data-ttu-id="1c72d-113">Gli altoparlanti correnti hanno dimensioni normali.</span><span class="sxs-lookup"><span data-stu-id="1c72d-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="1c72d-114">2</span><span class="sxs-lookup"><span data-stu-id="1c72d-114">2</span></span>     | <span data-ttu-id="1c72d-115">Gli altoparlanti correnti sono di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1c72d-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="1c72d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c72d-116">Remarks</span></span>

<span data-ttu-id="1c72d-117">Il nome descrittivo della dimensione del relatore può essere recuperato usando l'attributo **currentSpeakerName** .</span><span class="sxs-lookup"><span data-stu-id="1c72d-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="1c72d-118">Questo attributo viene ignorato se **enhancedAudio** è impostato su false.</span><span class="sxs-lookup"><span data-stu-id="1c72d-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c72d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c72d-119">Requirements</span></span>



| <span data-ttu-id="1c72d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c72d-120">Requirement</span></span> | <span data-ttu-id="1c72d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1c72d-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1c72d-122">Versione</span><span class="sxs-lookup"><span data-stu-id="1c72d-122">Version</span></span><br/> | <span data-ttu-id="1c72d-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1c72d-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c72d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c72d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c72d-125">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="1c72d-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="1c72d-126">**EQUALIZERSETTINGS.currentSpeakerName**</span><span class="sxs-lookup"><span data-stu-id="1c72d-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="1c72d-127">**EQUALIZERSETTINGS.enhancedAudio**</span><span class="sxs-lookup"><span data-stu-id="1c72d-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





