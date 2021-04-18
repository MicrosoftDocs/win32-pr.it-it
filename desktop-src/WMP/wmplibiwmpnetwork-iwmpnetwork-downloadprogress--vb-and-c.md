---
title: Proprietà downloadProgress di IWMPNetwork
description: La proprietà downloadProgress ottiene la percentuale di download completata.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Finestra delle proprietà di downloadProgress Media Player
- Proprietà di downloadProgress Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324525"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="9c641-106">IWMPNetwork::d proprietà ownloadProgress</span><span class="sxs-lookup"><span data-stu-id="9c641-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="9c641-107">La proprietà **downloadProgress** ottiene la percentuale di download completata.</span><span class="sxs-lookup"><span data-stu-id="9c641-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c641-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c641-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9c641-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9c641-109">Property value</span></span>

<span data-ttu-id="9c641-110">**System. Int32** che rappresenta lo stato di avanzamento del download espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="9c641-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c641-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c641-111">Remarks</span></span>

<span data-ttu-id="9c641-112">Quando il controllo Windows Media Player è connesso a un file multimediale digitale che può essere riprodotto e scaricato nello stesso momento, la proprietà **downloadProgress** ottiene la percentuale del file totale che è stato scaricato.</span><span class="sxs-lookup"><span data-stu-id="9c641-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="9c641-113">Questa funzionalità è attualmente supportata solo per i file multimediali digitali scaricati da server Web.</span><span class="sxs-lookup"><span data-stu-id="9c641-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="9c641-114">È possibile scaricare e riprodurre simultaneamente un file di uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c641-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="9c641-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="9c641-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="9c641-116">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="9c641-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="9c641-117">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="9c641-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="9c641-118">MP3</span><span class="sxs-lookup"><span data-stu-id="9c641-118">MP3</span></span>
-   <span data-ttu-id="9c641-119">MPEG</span><span class="sxs-lookup"><span data-stu-id="9c641-119">MPEG</span></span>
-   <span data-ttu-id="9c641-120">WAV</span><span class="sxs-lookup"><span data-stu-id="9c641-120">WAV</span></span>

<span data-ttu-id="9c641-121">Inoltre, alcuni file AVI possono essere scaricati e riprodotti simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="9c641-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="9c641-122">Usare **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** per determinare quando il buffering viene avviato o arrestato.</span><span class="sxs-lookup"><span data-stu-id="9c641-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="9c641-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c641-123">Examples</span></span>

<span data-ttu-id="9c641-124">Nell'esempio di codice seguente viene usato **downloadProgress** per visualizzare la percentuale di download completato.</span><span class="sxs-lookup"><span data-stu-id="9c641-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="9c641-125">Le informazioni vengono visualizzate in un'etichetta, in risposta all'evento di **buffering** .</span><span class="sxs-lookup"><span data-stu-id="9c641-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="9c641-126">Nell'esempio viene utilizzato un timer con un intervallo di 1 secondo per aggiornare la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9c641-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="9c641-127">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="9c641-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9c641-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c641-128">Requirements</span></span>



| <span data-ttu-id="9c641-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c641-129">Requirement</span></span> | <span data-ttu-id="9c641-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9c641-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c641-131">Versione</span><span class="sxs-lookup"><span data-stu-id="9c641-131">Version</span></span><br/>   | <span data-ttu-id="9c641-132">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9c641-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9c641-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9c641-133">Namespace</span></span><br/> | <span data-ttu-id="9c641-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9c641-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9c641-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="9c641-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9c641-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9c641-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c641-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c641-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c641-138">**Evento AxWindowsMediaPlayer. buffering (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9c641-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="9c641-139">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9c641-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





