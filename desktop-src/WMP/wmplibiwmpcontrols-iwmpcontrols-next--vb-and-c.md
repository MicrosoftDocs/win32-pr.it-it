---
title: Metodo Next di IWMPControls
description: Il metodo successivo imposta l'elemento successivo nella playlist come elemento corrente.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- Metodo Next Windows Media Player
- Metodo Next Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo Next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332476"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="58b30-106">IWMPControls:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="58b30-106">IWMPControls::next method</span></span>

<span data-ttu-id="58b30-107">Il metodo **successivo** imposta l'elemento successivo nella playlist come elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="58b30-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b30-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58b30-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="58b30-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="58b30-109">Parameters</span></span>

<span data-ttu-id="58b30-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="58b30-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58b30-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58b30-111">Return value</span></span>

<span data-ttu-id="58b30-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="58b30-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b30-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="58b30-113">Remarks</span></span>

<span data-ttu-id="58b30-114">Se la playlist si trova nell'ultima voce alla chiamata **successiva** , la prima voce nella playlist diventerà quella corrente.</span><span class="sxs-lookup"><span data-stu-id="58b30-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="58b30-115">Per le playlist lato server, questo metodo passa all'elemento successivo nella playlist sul lato server, non nella playlist del client.</span><span class="sxs-lookup"><span data-stu-id="58b30-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="58b30-116">Quando si riproduce un DVD, questo metodo passa al capitolo logico successivo nella sequenza di riproduzione, che potrebbe non essere il capitolo successivo nella playlist.</span><span class="sxs-lookup"><span data-stu-id="58b30-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="58b30-117">Quando si riproducono immagini ancora DVD, questo metodo passa all'immagine successiva.</span><span class="sxs-lookup"><span data-stu-id="58b30-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="58b30-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="58b30-118">Examples</span></span>

<span data-ttu-id="58b30-119">L'esempio seguente usa **Next** per passare all'elemento successivo nella playlist corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="58b30-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="58b30-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="58b30-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="58b30-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58b30-121">Requirements</span></span>



| <span data-ttu-id="58b30-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="58b30-122">Requirement</span></span> | <span data-ttu-id="58b30-123">Valore</span><span class="sxs-lookup"><span data-stu-id="58b30-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b30-124">Versione</span><span class="sxs-lookup"><span data-stu-id="58b30-124">Version</span></span><br/>   | <span data-ttu-id="58b30-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="58b30-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="58b30-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="58b30-126">Namespace</span></span><br/> | <span data-ttu-id="58b30-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="58b30-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="58b30-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="58b30-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="58b30-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="58b30-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58b30-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58b30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b30-131">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="58b30-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58b30-132">**IWMPControls. Previous (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="58b30-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58b30-133">**IWMPControls. Stop (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="58b30-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





