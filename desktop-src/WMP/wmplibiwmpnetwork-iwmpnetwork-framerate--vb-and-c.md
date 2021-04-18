---
title: Proprietà frameRate IWMPNetwork
description: La proprietà frameRate ottiene la frequenza dei fotogrammi video corrente.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- proprietà frameRate Media Player di Windows
- proprietà frameRate Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà frameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325111"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="513a1-106">Proprietà IWMPNetwork:: frameRate</span><span class="sxs-lookup"><span data-stu-id="513a1-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="513a1-107">La proprietà **framerate** ottiene la frequenza dei fotogrammi video corrente.</span><span class="sxs-lookup"><span data-stu-id="513a1-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="513a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="513a1-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="513a1-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="513a1-109">Property value</span></span>

<span data-ttu-id="513a1-110">**System. Int32** che corrisponde alla frequenza dei fotogrammi corrente in frame per cento secondi.</span><span class="sxs-lookup"><span data-stu-id="513a1-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="513a1-111">Sebbene la proprietà **encodedFrameRate** misuri la frequenza dei fotogrammi codificata in frame al secondo, la proprietà **framerate** misura la frequenza dei fotogrammi corrente in frame per cento secondi.</span><span class="sxs-lookup"><span data-stu-id="513a1-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="513a1-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="513a1-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="513a1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="513a1-113">Remarks</span></span>

<span data-ttu-id="513a1-114">Il valore della frequenza dei fotogrammi corrente viene restituito in frame per cento secondi.</span><span class="sxs-lookup"><span data-stu-id="513a1-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="513a1-115">Ad esempio, il valore 2998 indica 29,98 fotogrammi al secondo (fps).</span><span class="sxs-lookup"><span data-stu-id="513a1-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="513a1-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="513a1-116">Examples</span></span>

<span data-ttu-id="513a1-117">Nell'esempio di codice seguente viene usato il **framerate** per visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato.</span><span class="sxs-lookup"><span data-stu-id="513a1-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="513a1-118">Le informazioni vengono visualizzate in un'etichetta in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="513a1-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="513a1-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="513a1-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="513a1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="513a1-120">Requirements</span></span>



| <span data-ttu-id="513a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="513a1-121">Requirement</span></span> | <span data-ttu-id="513a1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="513a1-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513a1-123">Versione</span><span class="sxs-lookup"><span data-stu-id="513a1-123">Version</span></span><br/>   | <span data-ttu-id="513a1-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="513a1-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="513a1-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="513a1-125">Namespace</span></span><br/> | <span data-ttu-id="513a1-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="513a1-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="513a1-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="513a1-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="513a1-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="513a1-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513a1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="513a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513a1-130">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="513a1-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="513a1-131">**IWMPNetwork. encodedFrameRate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="513a1-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





