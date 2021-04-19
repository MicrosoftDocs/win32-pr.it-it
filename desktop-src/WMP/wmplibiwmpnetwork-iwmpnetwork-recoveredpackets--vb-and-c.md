---
title: Proprietà recoveredPackets di IWMPNetwork
description: La proprietà recoveredPackets ottiene il numero di pacchetti ripristinati.
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- Finestra delle proprietà di recoveredPackets Media Player
- Proprietà di recoveredPackets Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà recoveredPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe9fb8b44249be30289abb2f8922343285ca074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333539"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a><span data-ttu-id="e48b5-106">Proprietà IWMPNetwork:: recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="e48b5-106">IWMPNetwork::recoveredPackets property</span></span>

<span data-ttu-id="e48b5-107">La proprietà **recoveredPackets** ottiene il numero di pacchetti ripristinati.</span><span class="sxs-lookup"><span data-stu-id="e48b5-107">The **recoveredPackets** property gets the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48b5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e48b5-108">Syntax</span></span>


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e48b5-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e48b5-109">Property value</span></span>

<span data-ttu-id="e48b5-110">**System. Int32** che rappresenta il numero di pacchetti ripristinati.</span><span class="sxs-lookup"><span data-stu-id="e48b5-110">A **System.Int32** that is the number of recovered packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="e48b5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e48b5-111">Remarks</span></span>

<span data-ttu-id="e48b5-112">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="e48b5-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="e48b5-113">Il valore non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="e48b5-113">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="e48b5-114">Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato tramite la proprietà **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="e48b5-114">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span> <span data-ttu-id="e48b5-115">Il valore sarà zero quando si usa il protocollo HTTP, che è lossless.</span><span class="sxs-lookup"><span data-stu-id="e48b5-115">The value will be zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="e48b5-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="e48b5-116">Examples</span></span>

<span data-ttu-id="e48b5-117">Nell'esempio seguente viene usato **recoveredPackets** per visualizzare il numero di pacchetti ripristinati in un'etichetta, in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="e48b5-117">The following example uses **recoveredPackets** to display the number of recovered packets in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="e48b5-118">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e48b5-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="e48b5-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="e48b5-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e48b5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e48b5-120">Requirements</span></span>



| <span data-ttu-id="e48b5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e48b5-121">Requirement</span></span> | <span data-ttu-id="e48b5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e48b5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e48b5-123">Versione</span><span class="sxs-lookup"><span data-stu-id="e48b5-123">Version</span></span><br/>   | <span data-ttu-id="e48b5-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e48b5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e48b5-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e48b5-125">Namespace</span></span><br/> | <span data-ttu-id="e48b5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e48b5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e48b5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="e48b5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e48b5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e48b5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48b5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e48b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48b5-130">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e48b5-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e48b5-131">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e48b5-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





