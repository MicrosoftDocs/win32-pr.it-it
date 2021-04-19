---
title: Controls. Next (metodo)
description: Il metodo successivo imposta l'elemento corrente sull'elemento successivo nella playlist.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- Metodo Next Windows Media Player
- Metodo Next Windows Media Player, classe Controls
- Controlla la classe Windows Media Player, metodo successivo
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333424"
---
# <a name="controlsnext-method"></a><span data-ttu-id="34fe2-106">Controls. Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="34fe2-106">Controls.next method</span></span>

<span data-ttu-id="34fe2-107">Il metodo **successivo** imposta l'elemento corrente sull'elemento successivo nella playlist.</span><span class="sxs-lookup"><span data-stu-id="34fe2-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fe2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34fe2-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="34fe2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="34fe2-109">Parameters</span></span>

<span data-ttu-id="34fe2-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="34fe2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34fe2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34fe2-111">Return value</span></span>

<span data-ttu-id="34fe2-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="34fe2-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34fe2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="34fe2-113">Remarks</span></span>

<span data-ttu-id="34fe2-114">Se la playlist si trova nell'ultima voce alla chiamata **successiva** , la prima voce nella playlist diventerà quella corrente.</span><span class="sxs-lookup"><span data-stu-id="34fe2-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="34fe2-115">Per le playlist lato server, questo metodo passa all'elemento successivo nella playlist sul lato server, non nella playlist del client.</span><span class="sxs-lookup"><span data-stu-id="34fe2-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="34fe2-116">Quando si riproduce un DVD, questo metodo passa al capitolo logico successivo nella sequenza di riproduzione, che potrebbe non essere il capitolo successivo nella playlist.</span><span class="sxs-lookup"><span data-stu-id="34fe2-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="34fe2-117">Quando si giocano ancora i DVD, questo metodo passa alla successiva.</span><span class="sxs-lookup"><span data-stu-id="34fe2-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="34fe2-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="34fe2-118">Examples</span></span>

<span data-ttu-id="34fe2-119">Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **Next** per passare all'elemento successivo nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="34fe2-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="34fe2-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="34fe2-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="34fe2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34fe2-121">Requirements</span></span>



| <span data-ttu-id="34fe2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="34fe2-122">Requirement</span></span> | <span data-ttu-id="34fe2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="34fe2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34fe2-124">Versione</span><span class="sxs-lookup"><span data-stu-id="34fe2-124">Version</span></span><br/> | <span data-ttu-id="34fe2-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="34fe2-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="34fe2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="34fe2-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="34fe2-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34fe2-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34fe2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34fe2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34fe2-129">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="34fe2-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="34fe2-130">**Controlli. Previous**</span><span class="sxs-lookup"><span data-stu-id="34fe2-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="34fe2-131">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="34fe2-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





