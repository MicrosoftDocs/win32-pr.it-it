---
title: Proprietà durata IWMPMedia
description: La proprietà Duration ottiene la durata in secondi dell'elemento multimediale corrente.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Proprietà durata Media Player di Windows
- Proprietà Duration Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà Duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332409"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="cac46-106">IWMPMedia::d proprietà uration</span><span class="sxs-lookup"><span data-stu-id="cac46-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="cac46-107">La proprietà **Duration** ottiene la durata in secondi dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="cac46-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="cac46-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cac46-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac46-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cac46-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="cac46-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cac46-110">Property value</span></span>

<span data-ttu-id="cac46-111">**System. Double** che rappresenta la durata in secondi.</span><span class="sxs-lookup"><span data-stu-id="cac46-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac46-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cac46-112">Remarks</span></span>

<span data-ttu-id="cac46-113">Se questa proprietà viene utilizzata con un elemento multimediale diverso da quello specificato in AxWindowsMediaPlayer. currentMedia, potrebbe non contenere un valore valido.</span><span class="sxs-lookup"><span data-stu-id="cac46-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="cac46-114">Per recuperare la durata per i file che non si trovano nella libreria dell'utente, è necessario attendere che Windows Media Player Apra il file; ovvero, il **OpenState** corrente deve essere uguale a **MediaOpen**.</span><span class="sxs-lookup"><span data-stu-id="cac46-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="cac46-115">Per verificarlo, è possibile gestire **AxWindowsMediaPlayer. \_ Evento \_ OpenStateChange WMPOCXEvents** o verificando periodicamente il valore di **AxWindowsMediaPlayer. openState**.</span><span class="sxs-lookup"><span data-stu-id="cac46-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="cac46-116">Per le playlist, la durata di ogni elemento multimediale può essere recuperata quando viene aperto il singolo elemento multimediale, anziché quando viene aperta la playlist.</span><span class="sxs-lookup"><span data-stu-id="cac46-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="cac46-117">Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="cac46-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="cac46-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cac46-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cac46-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="cac46-119">Examples</span></span>

<span data-ttu-id="cac46-120">Nell'esempio seguente viene usato **Duration** per visualizzare l'ora rimanente dell'elemento multimediale corrente in un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="cac46-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="cac46-121">Un timer aggiorna il testo nell'etichetta ogni secondo.</span><span class="sxs-lookup"><span data-stu-id="cac46-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="cac46-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cac46-122">Requirements</span></span>



| <span data-ttu-id="cac46-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac46-123">Requirement</span></span> | <span data-ttu-id="cac46-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cac46-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac46-125">Versione</span><span class="sxs-lookup"><span data-stu-id="cac46-125">Version</span></span><br/>   | <span data-ttu-id="cac46-126">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cac46-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cac46-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cac46-127">Namespace</span></span><br/> | <span data-ttu-id="cac46-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cac46-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cac46-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="cac46-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cac46-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cac46-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac46-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cac46-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac46-132">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cac46-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cac46-133">**AxWindowsMediaPlayer. openState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cac46-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cac46-134">**Evento AxWindowsMediaPlayer. OpenStateChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cac46-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="cac46-135">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cac46-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cac46-136">**IWMPMedia. durationString (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cac46-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





