---
title: Proprietà receivedPackets di IWMPNetwork
description: La proprietà receivedPackets ottiene il numero di pacchetti ricevuti.
ms.assetid: 2a79dc81-4c7a-45d6-bc2b-b19ff5704c3b
keywords:
- Finestra delle proprietà di receivedPackets Media Player
- Proprietà di receivedPackets Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà receivedPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.receivedPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c62b4d90039f07177e8fcdc971cb66e0044aee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333392"
---
# <a name="iwmpnetworkreceivedpackets-property"></a><span data-ttu-id="257c3-106">Proprietà IWMPNetwork:: receivedPackets</span><span class="sxs-lookup"><span data-stu-id="257c3-106">IWMPNetwork::receivedPackets property</span></span>

<span data-ttu-id="257c3-107">La proprietà **receivedPackets** ottiene il numero di pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="257c3-107">The **receivedPackets** property gets the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="257c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="257c3-108">Syntax</span></span>


```CSharp
public System.Int32 receivedPackets {get; set;}
```


```VB

Public ReadOnly Property receivedPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="257c3-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="257c3-109">Property value</span></span>

<span data-ttu-id="257c3-110">**System. Int32** che rappresenta il numero di pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="257c3-110">A **System.Int32** that is the number of packets received.</span></span>

## <a name="remarks"></a><span data-ttu-id="257c3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="257c3-111">Remarks</span></span>

<span data-ttu-id="257c3-112">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="257c3-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="257c3-113">Il valore non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="257c3-113">The value is not reset if playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="257c3-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="257c3-114">Examples</span></span>

<span data-ttu-id="257c3-115">Nell'esempio seguente viene usato **receivedPackets** per visualizzare il numero di pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="257c3-115">The following example uses **receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="257c3-116">Le informazioni vengono visualizzate in un'etichetta in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="257c3-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="257c3-117">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="257c3-117">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="257c3-118">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="257c3-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether packets may be arriving.
    switch (e.newState)
    {
        // If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
        // or Transitioning then stop the timer. 
        case 1: 
        case 2: 
        case 4: 
        case 5: 
        case 7: 
        case 8: 
        case 9: 
            timer.Stop();
            break;

        // If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        default:
            timer.Interval = 1000;
            timer.Start();
            break;
    }
}

private void UpdateReceivedPackets(object sender, EventArgs e)
{
    receivedPacketsLabel.Text = ("Packets received: " + player.network.receivedPackets.ToString());
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

Public Sub UpdateReceivedPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receivedPacketsLabel.Text = (&quot;Packets received: &quot; + player.network.receivedPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="257c3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="257c3-119">Requirements</span></span>



| <span data-ttu-id="257c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="257c3-120">Requirement</span></span> | <span data-ttu-id="257c3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="257c3-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="257c3-122">Versione</span><span class="sxs-lookup"><span data-stu-id="257c3-122">Version</span></span><br/>   | <span data-ttu-id="257c3-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="257c3-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="257c3-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="257c3-124">Namespace</span></span><br/> | <span data-ttu-id="257c3-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="257c3-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="257c3-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="257c3-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="257c3-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="257c3-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="257c3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="257c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257c3-129">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="257c3-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





