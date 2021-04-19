---
title: Controls. fastReverse, metodo
description: Il metodo fastReverse avvia l'analisi rapida dell'elemento multimediale nella direzione inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Metodo fastReverse Windows Media Player
- Metodo fastReverse Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327071"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="f31d5-106">Controls. fastReverse, metodo</span><span class="sxs-lookup"><span data-stu-id="f31d5-106">Controls.fastReverse method</span></span>

<span data-ttu-id="f31d5-107">Il metodo **fastReverse** avvia l'analisi rapida dell'elemento multimediale nella direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="f31d5-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31d5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f31d5-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="f31d5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f31d5-109">Parameters</span></span>

<span data-ttu-id="f31d5-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f31d5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f31d5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f31d5-111">Return value</span></span>

<span data-ttu-id="f31d5-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f31d5-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f31d5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f31d5-113">Remarks</span></span>

<span data-ttu-id="f31d5-114">Il metodo **fastReverse** analizza il clip in senso inverso cinque volte la velocità normale, visualizzando solo i fotogrammi chiave se si tratta di un file video.</span><span class="sxs-lookup"><span data-stu-id="f31d5-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="f31d5-115">La chiamata di **fastReverse** modifica le *Impostazioni*. proprietà **rate** su 5,0.</span><span class="sxs-lookup"><span data-stu-id="f31d5-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="f31d5-116">Se la **frequenza** viene modificata in seguito o se viene chiamato il metodo **Play** o **Stop** , Windows Media Player interromperà velocemente.</span><span class="sxs-lookup"><span data-stu-id="f31d5-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="f31d5-117">Se l'elemento fa parte di una playlist, **fastReverse** si interrompe all'inizio della traccia corrente. Ad esempio, se Track 3 si trova in **fastReverse**, quando si raggiunge l'inizio di Track 3, Windows Media Player non passerà a Track 2.</span><span class="sxs-lookup"><span data-stu-id="f31d5-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="f31d5-118">Il numero di Play non viene incrementato quando si chiama **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="f31d5-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="f31d5-119">Se si chiama **fastForward** mentre **fastReverse** è attivo, **fastReverse** verrà arrestato e **fastForward** inizierà.</span><span class="sxs-lookup"><span data-stu-id="f31d5-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="f31d5-120">Questo metodo non funziona per le trasmissioni live e per determinati tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="f31d5-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="f31d5-121">Per determinare se è possibile utilizzare l'inversione veloce in un clip **, chiamare il** campo ("FastReverse").</span><span class="sxs-lookup"><span data-stu-id="f31d5-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="f31d5-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="f31d5-122">Examples</span></span>

<span data-ttu-id="f31d5-123">Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **fastReverse** per avviare la riproduzione veloce dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="f31d5-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="f31d5-124">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f31d5-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="f31d5-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f31d5-125">Requirements</span></span>



| <span data-ttu-id="f31d5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f31d5-126">Requirement</span></span> | <span data-ttu-id="f31d5-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f31d5-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f31d5-128">Versione</span><span class="sxs-lookup"><span data-stu-id="f31d5-128">Version</span></span><br/> | <span data-ttu-id="f31d5-129">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f31d5-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f31d5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f31d5-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="f31d5-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31d5-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31d5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f31d5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31d5-133">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="f31d5-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f31d5-134">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="f31d5-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="f31d5-135">**Controls. disavailable**</span><span class="sxs-lookup"><span data-stu-id="f31d5-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="f31d5-136">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="f31d5-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="f31d5-137">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="f31d5-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="f31d5-138">**Settings. rate**</span><span class="sxs-lookup"><span data-stu-id="f31d5-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





