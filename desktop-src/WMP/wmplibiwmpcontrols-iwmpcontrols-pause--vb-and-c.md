---
title: Metodo di sospensione IWMPControls
description: Il metodo pause sospende la riproduzione dell'elemento multimediale. | Metodo di sospensione IWMPControls
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- sospendere il metodo Windows Media Player
- sospendere il metodo Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo pause
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332474"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="f717c-107">IWMPControls::p metodo ause</span><span class="sxs-lookup"><span data-stu-id="f717c-107">IWMPControls::pause method</span></span>

<span data-ttu-id="f717c-108">Il metodo **pause** sospende la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="f717c-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f717c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f717c-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="f717c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f717c-110">Parameters</span></span>

<span data-ttu-id="f717c-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f717c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f717c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f717c-112">Return value</span></span>

<span data-ttu-id="f717c-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f717c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f717c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f717c-114">Remarks</span></span>

<span data-ttu-id="f717c-115">Quando un file viene sospeso, Windows Media Player non cede alcuna risorsa di sistema, ad esempio il dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="f717c-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="f717c-116">Per determinare se un particolare tipo di supporto può essere sospeso, passare il valore **System. String** "pause" alla proprietà **IWMPControls.** IsValid (il metodo **IWMPControls. Get \_ unavailable** in C#).</span><span class="sxs-lookup"><span data-stu-id="f717c-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="f717c-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="f717c-117">Examples</span></span>

<span data-ttu-id="f717c-118">Nell'esempio seguente viene usato **pause** per sospendere la riproduzione dell'elemento multimediale corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="f717c-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="f717c-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="f717c-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f717c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f717c-120">Requirements</span></span>



| <span data-ttu-id="f717c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f717c-121">Requirement</span></span> | <span data-ttu-id="f717c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f717c-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f717c-123">Versione</span><span class="sxs-lookup"><span data-stu-id="f717c-123">Version</span></span><br/>   | <span data-ttu-id="f717c-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f717c-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f717c-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f717c-125">Namespace</span></span><br/> | <span data-ttu-id="f717c-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f717c-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f717c-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="f717c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f717c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f717c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f717c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f717c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f717c-130">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f717c-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f717c-131">**IWMPControls. disavailable (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f717c-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





