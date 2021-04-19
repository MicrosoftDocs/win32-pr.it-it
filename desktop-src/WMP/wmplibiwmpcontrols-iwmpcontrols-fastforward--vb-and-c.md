---
title: Metodo IWMPControls fastForward
description: Il metodo fastForward avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti. | Metodo IWMPControls fastForward
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- Metodo fastForward Windows Media Player
- Metodo fastForward Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332486"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="a14ca-107">Metodo IWMPControls:: fastForward</span><span class="sxs-lookup"><span data-stu-id="a14ca-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="a14ca-108">Il metodo **fastForward** avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti.</span><span class="sxs-lookup"><span data-stu-id="a14ca-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="a14ca-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a14ca-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="a14ca-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a14ca-110">Parameters</span></span>

<span data-ttu-id="a14ca-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a14ca-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a14ca-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a14ca-112">Return value</span></span>

<span data-ttu-id="a14ca-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a14ca-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a14ca-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a14ca-114">Remarks</span></span>

<span data-ttu-id="a14ca-115">Il metodo **fastForward** riproduce il clip in cinque volte la velocità normale.</span><span class="sxs-lookup"><span data-stu-id="a14ca-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="a14ca-116">La chiamata di **fastForward** equivale a specificare 5,0 per la frequenza impostando la proprietà **IWMPSettings. rate** .</span><span class="sxs-lookup"><span data-stu-id="a14ca-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="a14ca-117">Se la frequenza viene modificata in seguito o se viene chiamato **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player interromperà l'invio rapido.</span><span class="sxs-lookup"><span data-stu-id="a14ca-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="a14ca-118">Il metodo **fastForward** non funziona per le trasmissioni live e per determinati tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="a14ca-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="a14ca-119">Per determinare se è possibile eseguire rapidamente l'avanzamento in un clip, passare il valore **System. String** "fastforward" alla proprietà **IWMPControls.** IsValid (il metodo **IWMPControls. \_ Get** in C#).</span><span class="sxs-lookup"><span data-stu-id="a14ca-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="a14ca-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="a14ca-120">Examples</span></span>

<span data-ttu-id="a14ca-121">Nell'esempio seguente viene usato **fastForward** per eseguire rapidamente l'avanzamento dell'elemento multimediale corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="a14ca-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="a14ca-122">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="a14ca-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a14ca-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a14ca-123">Requirements</span></span>



| <span data-ttu-id="a14ca-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a14ca-124">Requirement</span></span> | <span data-ttu-id="a14ca-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a14ca-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14ca-126">Versione</span><span class="sxs-lookup"><span data-stu-id="a14ca-126">Version</span></span><br/>   | <span data-ttu-id="a14ca-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a14ca-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a14ca-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a14ca-128">Namespace</span></span><br/> | <span data-ttu-id="a14ca-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a14ca-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a14ca-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="a14ca-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a14ca-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a14ca-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a14ca-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a14ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14ca-133">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a14ca-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a14ca-134">**IWMPControls. disavailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a14ca-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a14ca-135">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a14ca-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a14ca-136">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a14ca-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a14ca-137">**IWMPSettings. rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a14ca-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





