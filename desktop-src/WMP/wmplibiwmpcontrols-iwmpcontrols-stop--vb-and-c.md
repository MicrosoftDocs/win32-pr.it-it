---
title: Metodo Stop IWMPControls
description: Il metodo Stop interrompe la riproduzione dell'elemento multimediale. | Metodo Stop IWMPControls
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- arresta il metodo Windows Media Player
- Metodo Stop Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo Stop
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332469"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="8c1cf-107">Metodo IWMPControls:: Stop</span><span class="sxs-lookup"><span data-stu-id="8c1cf-107">IWMPControls::stop method</span></span>

<span data-ttu-id="8c1cf-108">Il metodo **Stop** interrompe la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1cf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c1cf-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="8c1cf-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c1cf-110">Parameters</span></span>

<span data-ttu-id="8c1cf-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c1cf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c1cf-112">Return value</span></span>

<span data-ttu-id="8c1cf-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c1cf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c1cf-114">Remarks</span></span>

<span data-ttu-id="8c1cf-115">Questo metodo fa in modo che Windows Media Player rilasciare tutte le risorse di sistema utilizzate, ad esempio il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="8c1cf-116">L'elemento multimediale corrente, tuttavia, non viene rilasciato.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="8c1cf-117">Quando Windows Media Player viene arrestato, la posizione di riproduzione corrente nell'elemento multimediale viene reimpostata all'inizio dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="8c1cf-118">Successivamente, la chiamata a **IWMPControls. Play** avvierà la riproduzione dall'inizio dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="8c1cf-119">Per arrestare un'operazione di riproduzione senza modificare la posizione corrente, usare il metodo **IWMPControls. pause** .</span><span class="sxs-lookup"><span data-stu-id="8c1cf-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="8c1cf-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c1cf-120">Examples</span></span>

<span data-ttu-id="8c1cf-121">Nell'esempio seguente viene usato **Stop** per arrestare l'elemento multimediale corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="8c1cf-122">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="8c1cf-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="8c1cf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c1cf-123">Requirements</span></span>



| <span data-ttu-id="8c1cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c1cf-124">Requirement</span></span> | <span data-ttu-id="8c1cf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8c1cf-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1cf-126">Versione</span><span class="sxs-lookup"><span data-stu-id="8c1cf-126">Version</span></span><br/>   | <span data-ttu-id="8c1cf-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8c1cf-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8c1cf-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c1cf-128">Namespace</span></span><br/> | <span data-ttu-id="8c1cf-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8c1cf-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8c1cf-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="8c1cf-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8c1cf-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8c1cf-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c1cf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c1cf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c1cf-133">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c1cf-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c1cf-134">**IWMPControls. Next (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c1cf-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c1cf-135">**IWMPControls. pause (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c1cf-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c1cf-136">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c1cf-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c1cf-137">**IWMPControls. Previous (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c1cf-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





