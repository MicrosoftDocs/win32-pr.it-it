---
title: Evento PlayStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PlayStateChange si verifica quando viene modificato lo stato di riproduzione del controllo Media Player di Windows.
ms.assetid: f8823c90-2084-4771-a2fe-7081d4e49e63
keywords:
- Evento PlayStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PlayStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af97803224df89287847ee2b9ef83d8e976d91b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326229"
---
# <a name="playstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b5913-104">Evento PlayStateChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="b5913-104">PlayStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b5913-105">L'evento PlayStateChange si verifica quando viene modificato lo stato di riproduzione del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="b5913-105">The PlayStateChange event occurs when the play state of the Windows Media Player control changes.</span></span>

``` syntax
[C#]
private void player_PlayStateChange(
  object sender,
  _WMPOCXEvents_PlayStateChangeEvent e
)

[Visual Basic]
 Private Sub player_PlayStateChange(   
 sender As Object,  
 e As _WMPOCXEvents_PlayStateChangeEvent 
 ) Handles player.PlayStateChange
 
```

## <a name="event-data"></a><span data-ttu-id="b5913-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="b5913-106">Event Data</span></span>

<span data-ttu-id="b5913-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlayStateChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="b5913-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEventHandler**.</span></span> <span data-ttu-id="b5913-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlayStateChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="b5913-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="b5913-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5913-109">Property</span></span>     | <span data-ttu-id="b5913-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5913-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="b5913-111">**newState**</span><span class="sxs-lookup"><span data-stu-id="b5913-111">**newState**</span></span> | <span data-ttu-id="b5913-112">System. Int32Specifies il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="b5913-112">System.Int32Specifies the new state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5913-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5913-113">Remarks</span></span>

<span data-ttu-id="b5913-114">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="b5913-114">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="b5913-115">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="b5913-115">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="b5913-116">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="b5913-116">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="b5913-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="b5913-117">Examples</span></span>

<span data-ttu-id="b5913-118">Nell'esempio seguente viene illustrato un gestore eventi per l'evento PlayStateChange che visualizza lo stato di riproduzione corrente in un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="b5913-118">The following example demonstrates an event handler for the PlayStateChange Event that displays the current play state in a label.</span></span> <span data-ttu-id="b5913-119">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="b5913-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test the current state of the player and display a message for each state.
    switch (e.newState)
    {
        case 0:    // Undefined
            currentStateLabel.Text = "Undefined";
            break;

        case 1:    // Stopped
            currentStateLabel.Text = "Stopped";
            break;

        case 2:    // Paused
            currentStateLabel.Text = "Paused";
            break;

        case 3:    // Playing
            currentStateLabel.Text = "Playing";
            break;

        case 4:    // ScanForward
            currentStateLabel.Text = "ScanForward";
            break;

        case 5:    // ScanReverse
            currentStateLabel.Text = "ScanReverse";
            break;

        case 6:    // Buffering
            currentStateLabel.Text = "Buffering";
            break;

        case 7:    // Waiting
            currentStateLabel.Text = "Waiting";
            break;

        case 8:    // MediaEnded
            currentStateLabel.Text = "MediaEnded";
            break;

        case 9:    // Transitioning
            currentStateLabel.Text = "Transitioning";
            break;

        case 10:   // Ready
            currentStateLabel.Text = "Ready";
            break;

        case 11:   // Reconnecting
            currentStateLabel.Text = "Reconnecting";
            break;

        case 12:   // Last
            currentStateLabel.Text = "Last";
            break;

        default:
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString());
            break;
    }
}
```




```VB
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    ' Test the current state of the player, display a message for each state.
    Select Case e.newState

        Case 0 ' Undefined
            currentStateLabel.Text = "Undefined"

        Case 1 ' Stopped
            currentStateLabel.Text = "Stopped"

        Case 2 ' Paused
            currentStateLabel.Text = "Paused"

        Case 3 ' Playing
            currentStateLabel.Text = "Playing"

        Case 4 ' ScanForward
            currentStateLabel.Text = "ScanForward"

        Case 5 ' ScanReverse
            currentStateLabel.Text = "ScanReverse"

        Case 6 ' Buffering
            currentStateLabel.Text = "Buffering"

        Case 7 ' Waiting
            currentStateLabel.Text = "Waiting"

        Case 8 ' MediaEnded
            currentStateLabel.Text = "MediaEnded"

        Case 9 ' Transitioning
            currentStateLabel.Text = "Transitioning"

        Case 10 ' Ready
            currentStateLabel.Text = "Ready"

        Case 11 ' Reconnecting
            currentStateLabel.Text = "Reconnecting"

        Case 12 ' Last
            currentStateLabel.Text = "Last"

        Case Else
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString())

    End Select

End Sub
```



## <a name="requirements"></a><span data-ttu-id="b5913-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5913-120">Requirements</span></span>



| <span data-ttu-id="b5913-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5913-121">Requirement</span></span> | <span data-ttu-id="b5913-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b5913-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5913-123">Versione</span><span class="sxs-lookup"><span data-stu-id="b5913-123">Version</span></span><br/>   | <span data-ttu-id="b5913-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b5913-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b5913-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5913-125">Namespace</span></span><br/> | <span data-ttu-id="b5913-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b5913-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b5913-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="b5913-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b5913-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b5913-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5913-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5913-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5913-130">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b5913-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b5913-131">**AxWindowsMediaPlayer. riproduzione (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b5913-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> </dl>

 

 





