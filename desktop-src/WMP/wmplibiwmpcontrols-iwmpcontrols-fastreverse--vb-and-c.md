---
title: Metodo IWMPControls fastReverse
description: Il metodo fastReverse avvia la riproduzione rapida dell'elemento multimediale nella direzione inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- Metodo fastReverse Windows Media Player
- Metodo fastReverse Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332483"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="1ec18-106">Metodo IWMPControls:: fastReverse</span><span class="sxs-lookup"><span data-stu-id="1ec18-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="1ec18-107">Il metodo **fastReverse** avvia la riproduzione rapida dell'elemento multimediale nella direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="1ec18-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec18-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ec18-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="1ec18-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ec18-109">Parameters</span></span>

<span data-ttu-id="1ec18-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1ec18-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ec18-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ec18-111">Return value</span></span>

<span data-ttu-id="1ec18-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1ec18-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec18-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ec18-113">Remarks</span></span>

<span data-ttu-id="1ec18-114">Il metodo **fastReverse** analizza il clip in senso inverso cinque volte la velocità normale, visualizzando solo i fotogrammi chiave se si tratta di un file video.</span><span class="sxs-lookup"><span data-stu-id="1ec18-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="1ec18-115">La chiamata di **fastReverse** equivale a specificare-5,0 per la frequenza impostando la proprietà **IWMPSettings. rate** .</span><span class="sxs-lookup"><span data-stu-id="1ec18-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="1ec18-116">Se la frequenza viene modificata in seguito o se viene chiamato **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player interromperà velocemente.</span><span class="sxs-lookup"><span data-stu-id="1ec18-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="1ec18-117">Se l'elemento fa parte di una playlist, **fastReverse** si interrompe all'inizio della traccia corrente. Ad esempio, se Track 3 si trova in **fastReverse**, quando si raggiunge l'inizio di Track 3, Windows Media Player non passerà a Track 2.</span><span class="sxs-lookup"><span data-stu-id="1ec18-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="1ec18-118">Il numero di Play non viene incrementato quando si chiama **fastReverse**.</span><span class="sxs-lookup"><span data-stu-id="1ec18-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="1ec18-119">Se si chiama **IWMPControls. fastForward** mentre **fastReverse** è in esecuzione, **fastReverse** verrà arrestato e **IWMPControls. fastForward** inizierà.</span><span class="sxs-lookup"><span data-stu-id="1ec18-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="1ec18-120">Questo metodo non funziona per trasmissioni live e determinati tipi di supporti digitali.</span><span class="sxs-lookup"><span data-stu-id="1ec18-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="1ec18-121">Per determinare se è possibile utilizzare l'inversione veloce in un clip, passare il valore **System. String** "FastReverse" alla proprietà **IWMPControls.** IsValid (il metodo **IWMPControls. \_ Get** in C#).</span><span class="sxs-lookup"><span data-stu-id="1ec18-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="1ec18-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="1ec18-122">Examples</span></span>

<span data-ttu-id="1ec18-123">Nell'esempio seguente viene usato **fastReverse** per invertire l'elemento multimediale corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="1ec18-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="1ec18-124">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="1ec18-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1ec18-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ec18-125">Requirements</span></span>



| <span data-ttu-id="1ec18-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec18-126">Requirement</span></span> | <span data-ttu-id="1ec18-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1ec18-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec18-128">Versione</span><span class="sxs-lookup"><span data-stu-id="1ec18-128">Version</span></span><br/>   | <span data-ttu-id="1ec18-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1ec18-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1ec18-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ec18-130">Namespace</span></span><br/> | <span data-ttu-id="1ec18-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1ec18-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1ec18-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="1ec18-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1ec18-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec18-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec18-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ec18-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec18-135">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1ec18-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1ec18-136">**IWMPControls. fastForward (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1ec18-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1ec18-137">**IWMPControls. disavailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1ec18-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1ec18-138">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1ec18-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1ec18-139">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1ec18-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1ec18-140">**IWMPSettings. rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1ec18-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





