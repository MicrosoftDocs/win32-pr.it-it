---
title: Controls. pause (metodo)
description: Il metodo pause sospende la riproduzione dell'elemento multimediale. | Controls. pause (metodo)
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- sospendere il metodo Windows Media Player
- Metodo pause Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo pause
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331244"
---
# <a name="controlspause-method"></a><span data-ttu-id="7a145-107">Controls. pause (metodo)</span><span class="sxs-lookup"><span data-stu-id="7a145-107">Controls.pause method</span></span>

<span data-ttu-id="7a145-108">Il metodo **pause** sospende la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="7a145-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a145-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a145-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="7a145-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a145-110">Parameters</span></span>

<span data-ttu-id="7a145-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7a145-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a145-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a145-112">Return value</span></span>

<span data-ttu-id="7a145-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7a145-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a145-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a145-114">Remarks</span></span>

<span data-ttu-id="7a145-115">Quando un file viene sospeso, Windows Media Player non cede alcuna risorsa di sistema, ad esempio il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="7a145-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="7a145-116">Alcuni tipi di supporto non possono essere sospesi, ad esempio i flussi live.</span><span class="sxs-lookup"><span data-stu-id="7a145-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="7a145-117">Per determinare se un tipo di supporto specifico può essere sospeso, utilizzare i *controlli*. non **disponibile (' pause ')**.</span><span class="sxs-lookup"><span data-stu-id="7a145-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="7a145-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a145-118">Examples</span></span>

<span data-ttu-id="7a145-119">Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **pause** per sospendere la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="7a145-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="7a145-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7a145-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="7a145-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a145-121">Requirements</span></span>



| <span data-ttu-id="7a145-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a145-122">Requirement</span></span> | <span data-ttu-id="7a145-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7a145-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a145-124">Versione</span><span class="sxs-lookup"><span data-stu-id="7a145-124">Version</span></span><br/> | <span data-ttu-id="7a145-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="7a145-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7a145-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7a145-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a145-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a145-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a145-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a145-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a145-129">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="7a145-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="7a145-130">**Controls. disavailable**</span><span class="sxs-lookup"><span data-stu-id="7a145-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





