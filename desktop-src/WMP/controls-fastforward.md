---
title: Controls. fastForward, metodo
description: Il metodo fastForward avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti. | Controls. fastForward, metodo
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Metodo fastForward Windows Media Player
- Metodo fastForward Windows Media Player, classe Controls
- Classe Controls Media Player Windows, metodo fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327072"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="ac94a-107">Controls. fastForward, metodo</span><span class="sxs-lookup"><span data-stu-id="ac94a-107">Controls.fastForward method</span></span>

<span data-ttu-id="ac94a-108">Il metodo **fastForward** avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti.</span><span class="sxs-lookup"><span data-stu-id="ac94a-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac94a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac94a-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="ac94a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac94a-110">Parameters</span></span>

<span data-ttu-id="ac94a-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ac94a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ac94a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac94a-112">Return value</span></span>

<span data-ttu-id="ac94a-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ac94a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac94a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac94a-114">Remarks</span></span>

<span data-ttu-id="ac94a-115">Il metodo **fastForward** riproduce il ritaglio cinque volte la velocità normale.</span><span class="sxs-lookup"><span data-stu-id="ac94a-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="ac94a-116">La chiamata di **fastForward** modifica le *Impostazioni*. proprietà **rate** su 5,0.</span><span class="sxs-lookup"><span data-stu-id="ac94a-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="ac94a-117">Se la **frequenza** viene modificata o se viene chiamato il metodo **Play** o **Stop** , Windows Media Player interromperà l'invio rapido.</span><span class="sxs-lookup"><span data-stu-id="ac94a-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="ac94a-118">Il metodo **fastForward** non funziona per le trasmissioni live e per determinati tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="ac94a-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="ac94a-119">Per determinare se è possibile eseguire l'avanzamento rapido in un clip, chiamare l'oggetto non **disponibile**("fastforward").</span><span class="sxs-lookup"><span data-stu-id="ac94a-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="ac94a-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="ac94a-120">Examples</span></span>

<span data-ttu-id="ac94a-121">Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **fastForward** per avviare la riproduzione rapida dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ac94a-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="ac94a-122">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ac94a-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="ac94a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac94a-123">Requirements</span></span>



| <span data-ttu-id="ac94a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac94a-124">Requirement</span></span> | <span data-ttu-id="ac94a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ac94a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac94a-126">Versione</span><span class="sxs-lookup"><span data-stu-id="ac94a-126">Version</span></span><br/> | <span data-ttu-id="ac94a-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ac94a-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ac94a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ac94a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac94a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac94a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac94a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac94a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac94a-131">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="ac94a-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="ac94a-132">**Controls. disavailable**</span><span class="sxs-lookup"><span data-stu-id="ac94a-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="ac94a-133">**Controls. Play**</span><span class="sxs-lookup"><span data-stu-id="ac94a-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="ac94a-134">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="ac94a-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="ac94a-135">**Settings. rate**</span><span class="sxs-lookup"><span data-stu-id="ac94a-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





