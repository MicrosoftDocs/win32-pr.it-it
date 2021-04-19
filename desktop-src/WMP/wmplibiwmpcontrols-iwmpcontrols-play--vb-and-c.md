---
title: Metodo Play IWMPControls
description: Il metodo Play inizia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- Metodo di riproduzione Media Player Windows
- Metodo Play Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo Play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332472"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="c1122-106">IWMPControls::p metodo Lay</span><span class="sxs-lookup"><span data-stu-id="c1122-106">IWMPControls::play method</span></span>

<span data-ttu-id="c1122-107">Il metodo **Play** inizia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.</span><span class="sxs-lookup"><span data-stu-id="c1122-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1122-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1122-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="c1122-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1122-109">Parameters</span></span>

<span data-ttu-id="c1122-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c1122-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1122-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1122-111">Return value</span></span>

<span data-ttu-id="c1122-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c1122-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1122-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1122-113">Remarks</span></span>

<span data-ttu-id="c1122-114">Se questo metodo viene chiamato durante l'avanzamento rapido o il riavvolgimento, la frequenza di riproduzione (il valore di **IWMPSettings. rate**) viene impostata su 1,0.</span><span class="sxs-lookup"><span data-stu-id="c1122-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="c1122-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1122-115">Examples</span></span>

<span data-ttu-id="c1122-116">Nell'esempio seguente viene usato **Play** per riprodurre l'elemento multimediale corrente in risposta all'evento Click di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="c1122-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="c1122-117">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c1122-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c1122-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1122-118">Requirements</span></span>



| <span data-ttu-id="c1122-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1122-119">Requirement</span></span> | <span data-ttu-id="c1122-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c1122-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1122-121">Versione</span><span class="sxs-lookup"><span data-stu-id="c1122-121">Version</span></span><br/>   | <span data-ttu-id="c1122-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c1122-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c1122-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1122-123">Namespace</span></span><br/> | <span data-ttu-id="c1122-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c1122-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c1122-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="c1122-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c1122-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c1122-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1122-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1122-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1122-128">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c1122-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1122-129">**IWMPControls. playItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c1122-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1122-130">**IWMPSettings. rate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c1122-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





