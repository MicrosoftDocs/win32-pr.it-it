---
title: Proprietà receptionQuality di IWMPNetwork
description: La proprietà receptionQuality ottiene la percentuale di pacchetti non persi negli ultimi 30 secondi.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- Finestra delle proprietà di receptionQuality Media Player
- Proprietà di receptionQuality Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà receptionQuality
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333390"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="58037-106">Proprietà IWMPNetwork:: receptionQuality</span><span class="sxs-lookup"><span data-stu-id="58037-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="58037-107">La proprietà **receptionQuality** ottiene la percentuale di pacchetti non persi negli ultimi 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="58037-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="58037-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58037-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="58037-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="58037-109">Property value</span></span>

<span data-ttu-id="58037-110">**System. Int32** che rappresenta la qualità della ricezione.</span><span class="sxs-lookup"><span data-stu-id="58037-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="58037-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="58037-111">Remarks</span></span>

<span data-ttu-id="58037-112">Il numero di pacchetti ricevuti, persi e ripristinati durante il flusso viene monitorato una volta al secondo.</span><span class="sxs-lookup"><span data-stu-id="58037-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="58037-113">La proprietà **receptionQuality** ottiene la percentuale di pacchetti non persi negli ultimi 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="58037-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="58037-114">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="58037-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="58037-115">Il valore non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="58037-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="58037-116">Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato tramite la proprietà **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="58037-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="58037-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="58037-117">Examples</span></span>

<span data-ttu-id="58037-118">Nell'esempio seguente viene usato **receptionQuality** per visualizzare la percentuale di pacchetti ricevuti in un'etichetta, in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="58037-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="58037-119">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="58037-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="58037-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="58037-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="58037-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58037-121">Requirements</span></span>



| <span data-ttu-id="58037-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="58037-122">Requirement</span></span> | <span data-ttu-id="58037-123">Valore</span><span class="sxs-lookup"><span data-stu-id="58037-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58037-124">Versione</span><span class="sxs-lookup"><span data-stu-id="58037-124">Version</span></span><br/>   | <span data-ttu-id="58037-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="58037-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="58037-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="58037-126">Namespace</span></span><br/> | <span data-ttu-id="58037-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="58037-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="58037-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="58037-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="58037-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="58037-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58037-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58037-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58037-131">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="58037-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58037-132">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="58037-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





