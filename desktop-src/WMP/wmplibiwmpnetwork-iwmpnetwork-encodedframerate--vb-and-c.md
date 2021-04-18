---
title: Proprietà encodedFrameRate di IWMPNetwork
description: La proprietà encodedFrameRate ottiene la frequenza dei fotogrammi video specificata dall'autore del contenuto.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- Finestra delle proprietà di encodedFrameRate Media Player
- Proprietà di encodedFrameRate Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324524"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="444f8-106">Proprietà IWMPNetwork:: encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="444f8-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="444f8-107">La proprietà **encodedFrameRate** ottiene la frequenza dei fotogrammi video specificata dall'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="444f8-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="444f8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="444f8-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="444f8-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="444f8-109">Property value</span></span>

<span data-ttu-id="444f8-110">**System. Int32** che è la frequenza dei fotogrammi codificata in frame al secondo (fps).</span><span class="sxs-lookup"><span data-stu-id="444f8-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="444f8-111">Sebbene la proprietà **encodedFrameRate** misuri la frequenza dei fotogrammi codificata in frame al secondo, la proprietà **framerate** misura la frequenza dei fotogrammi corrente in frame per cento secondi.</span><span class="sxs-lookup"><span data-stu-id="444f8-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="444f8-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="444f8-112">Examples</span></span>

<span data-ttu-id="444f8-113">Nell'esempio di codice seguente viene usato **encodedFrameRate** per visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato.</span><span class="sxs-lookup"><span data-stu-id="444f8-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="444f8-114">Le informazioni vengono visualizzate in un'etichetta, in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="444f8-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="444f8-115">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="444f8-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="444f8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="444f8-116">Requirements</span></span>



| <span data-ttu-id="444f8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="444f8-117">Requirement</span></span> | <span data-ttu-id="444f8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="444f8-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="444f8-119">Versione</span><span class="sxs-lookup"><span data-stu-id="444f8-119">Version</span></span><br/>   | <span data-ttu-id="444f8-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="444f8-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="444f8-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="444f8-121">Namespace</span></span><br/> | <span data-ttu-id="444f8-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="444f8-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="444f8-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="444f8-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="444f8-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="444f8-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444f8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="444f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444f8-126">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="444f8-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="444f8-127">**IWMPNetwork. frameRate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="444f8-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





