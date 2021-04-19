---
title: Evento Player. PlayStateChange
description: L'evento PlayStateChange si verifica quando viene apportata una modifica alla proprietà riproduzione.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Media Player di Windows Event PlayStateChange
- Windows Event PlayStateChange Media Player, classe Player
- Classe Player Windows Media Player, evento PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326001"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="45b43-106">Evento Player. PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="45b43-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="45b43-107">L'evento **PlayStateChange** si verifica quando viene apportata una modifica alla proprietà **riproduzione** .</span><span class="sxs-lookup"><span data-stu-id="45b43-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b43-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45b43-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="45b43-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="45b43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b43-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="45b43-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="45b43-111">Numero (**Long**) che specifica il nuovo **riproduzione**.</span><span class="sxs-lookup"><span data-stu-id="45b43-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="45b43-112">Per una tabella dei valori possibili, vedere [riproduzione](player-playstate.md) .</span><span class="sxs-lookup"><span data-stu-id="45b43-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b43-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45b43-113">Return value</span></span>

<span data-ttu-id="45b43-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="45b43-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b43-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="45b43-115">Remarks</span></span>

<span data-ttu-id="45b43-116">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="45b43-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="45b43-117">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="45b43-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="45b43-118">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="45b43-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="45b43-119">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="45b43-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="45b43-120">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="45b43-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="45b43-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="45b43-121">Examples</span></span>

<span data-ttu-id="45b43-122">Nell'esempio seguente viene illustrato un gestore eventi per il *lettore*. evento **playStateChange** .</span><span class="sxs-lookup"><span data-stu-id="45b43-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="45b43-123">Un elemento di testo HTML, denominato "testo", Visualizza il nuovo stato di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="45b43-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="45b43-124">L'oggetto Player è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="45b43-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="45b43-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45b43-125">Requirements</span></span>



| <span data-ttu-id="45b43-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b43-126">Requirement</span></span> | <span data-ttu-id="45b43-127">Valore</span><span class="sxs-lookup"><span data-stu-id="45b43-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45b43-128">Versione</span><span class="sxs-lookup"><span data-stu-id="45b43-128">Version</span></span><br/> | <span data-ttu-id="45b43-129">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="45b43-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="45b43-130">DLL</span><span class="sxs-lookup"><span data-stu-id="45b43-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="45b43-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b43-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b43-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45b43-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b43-133">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="45b43-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="45b43-134">**Player. riproduzione**</span><span class="sxs-lookup"><span data-stu-id="45b43-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





