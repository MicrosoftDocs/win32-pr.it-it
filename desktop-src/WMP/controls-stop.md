---
title: Metodo Controls. Stop
description: Il metodo Stop interrompe la riproduzione dell'elemento multimediale. | Metodo Controls. Stop
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- arresta il metodo Windows Media Player
- Metodo Stop Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo Stop
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327388"
---
# <a name="controlsstop-method"></a><span data-ttu-id="56943-107">Metodo Controls. Stop</span><span class="sxs-lookup"><span data-stu-id="56943-107">Controls.stop method</span></span>

<span data-ttu-id="56943-108">Il metodo **Stop** interrompe la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="56943-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="56943-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56943-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="56943-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="56943-110">Parameters</span></span>

<span data-ttu-id="56943-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="56943-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56943-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56943-112">Return value</span></span>

<span data-ttu-id="56943-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="56943-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56943-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="56943-114">Remarks</span></span>

<span data-ttu-id="56943-115">Questo metodo fa in modo che Windows Media Player rilasciare tutte le risorse di sistema utilizzate, ad esempio il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="56943-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="56943-116">L'elemento multimediale corrente, tuttavia, non viene rilasciato.</span><span class="sxs-lookup"><span data-stu-id="56943-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="56943-117">Quando il lettore viene arrestato, la traccia viene ricaricata fino all'inizio.</span><span class="sxs-lookup"><span data-stu-id="56943-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="56943-118">La chiamata di **Play** inizierà la riproduzione della clip dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="56943-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="56943-119">Per arrestare un'operazione di riproduzione senza modificare la posizione corrente, usare il metodo **pause** .</span><span class="sxs-lookup"><span data-stu-id="56943-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="56943-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="56943-120">Examples</span></span>

<span data-ttu-id="56943-121">Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **Stop** per arrestare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="56943-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="56943-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="56943-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="56943-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56943-123">Requirements</span></span>



| <span data-ttu-id="56943-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="56943-124">Requirement</span></span> | <span data-ttu-id="56943-125">Valore</span><span class="sxs-lookup"><span data-stu-id="56943-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56943-126">Versione</span><span class="sxs-lookup"><span data-stu-id="56943-126">Version</span></span><br/> | <span data-ttu-id="56943-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="56943-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="56943-128">DLL</span><span class="sxs-lookup"><span data-stu-id="56943-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="56943-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56943-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56943-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56943-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56943-131">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="56943-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="56943-132">**Controlli. Next**</span><span class="sxs-lookup"><span data-stu-id="56943-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="56943-133">**Controls. pause**</span><span class="sxs-lookup"><span data-stu-id="56943-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="56943-134">**Controlli. Previous**</span><span class="sxs-lookup"><span data-stu-id="56943-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





