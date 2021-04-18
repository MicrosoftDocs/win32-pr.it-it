---
title: Proprietà bufferingProgress di IWMPNetwork
description: La proprietà bufferingProgress ottiene la percentuale di memorizzazione nel buffer completata.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- Finestra delle proprietà di bufferingProgress Media Player
- Proprietà di bufferingProgress Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà bufferingProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329005"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="def1e-106">Proprietà IWMPNetwork:: bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="def1e-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="def1e-107">La proprietà **bufferingProgress** ottiene la percentuale di memorizzazione nel buffer completata.</span><span class="sxs-lookup"><span data-stu-id="def1e-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="def1e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="def1e-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="def1e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="def1e-109">Property value</span></span>

<span data-ttu-id="def1e-110">**System. Int32** che rappresenta lo stato di avanzamento del buffer espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="def1e-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="def1e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="def1e-111">Remarks</span></span>

<span data-ttu-id="def1e-112">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="def1e-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="def1e-113">Non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="def1e-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="def1e-114">Il buffering si applica solo ai contenuti in streaming.</span><span class="sxs-lookup"><span data-stu-id="def1e-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="def1e-115">Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato tramite la proprietà **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="def1e-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="def1e-116">Usare **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** per determinare quando il buffering viene avviato o arrestato.</span><span class="sxs-lookup"><span data-stu-id="def1e-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="def1e-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="def1e-117">Examples</span></span>

<span data-ttu-id="def1e-118">Nell'esempio seguente viene usato **bufferingProgress** per visualizzare la percentuale di memorizzazione nel buffer completata in un'etichetta, in risposta all'evento di buffering.</span><span class="sxs-lookup"><span data-stu-id="def1e-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="def1e-119">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="def1e-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="def1e-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="def1e-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="def1e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="def1e-121">Requirements</span></span>



| <span data-ttu-id="def1e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="def1e-122">Requirement</span></span> | <span data-ttu-id="def1e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="def1e-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def1e-124">Versione</span><span class="sxs-lookup"><span data-stu-id="def1e-124">Version</span></span><br/>   | <span data-ttu-id="def1e-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="def1e-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="def1e-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="def1e-126">Namespace</span></span><br/> | <span data-ttu-id="def1e-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="def1e-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="def1e-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="def1e-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="def1e-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="def1e-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def1e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="def1e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def1e-131">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="def1e-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="def1e-132">**Evento AxWindowsMediaPlayer. buffering (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="def1e-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="def1e-133">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="def1e-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





