---
title: Proprietà della larghezza di banda IWMPNetwork
description: La proprietà bandWidth ottiene la larghezza di banda corrente dell'elemento multimediale.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- Proprietà della larghezza di banda di Windows Media Player
- Proprietà della larghezza di banda Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà bandWidth
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327142"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="44e31-106">Proprietà IWMPNetwork:: bandWidth</span><span class="sxs-lookup"><span data-stu-id="44e31-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="44e31-107">La proprietà **Bandwidth** ottiene la larghezza di banda corrente dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="44e31-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e31-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44e31-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="44e31-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="44e31-109">Property value</span></span>

<span data-ttu-id="44e31-110">**System. Int32** che rappresenta la larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="44e31-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="44e31-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="44e31-111">Remarks</span></span>

<span data-ttu-id="44e31-112">Il valore recuperato tramite **AxWindowsMediaPlayer. URL** sarà zero se l'URL non è impostato.</span><span class="sxs-lookup"><span data-stu-id="44e31-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="44e31-113">Questa proprietà è valida solo per i flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="44e31-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="44e31-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="44e31-114">Examples</span></span>

<span data-ttu-id="44e31-115">Nell'esempio seguente viene utilizzata la **larghezza di banda** per visualizzare la larghezza di banda media corrente.</span><span class="sxs-lookup"><span data-stu-id="44e31-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="44e31-116">Le informazioni vengono visualizzate in un'etichetta in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="44e31-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="44e31-117">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="44e31-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
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

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="44e31-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44e31-118">Requirements</span></span>



| <span data-ttu-id="44e31-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e31-119">Requirement</span></span> | <span data-ttu-id="44e31-120">Valore</span><span class="sxs-lookup"><span data-stu-id="44e31-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44e31-121">Versione</span><span class="sxs-lookup"><span data-stu-id="44e31-121">Version</span></span><br/>   | <span data-ttu-id="44e31-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="44e31-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="44e31-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="44e31-123">Namespace</span></span><br/> | <span data-ttu-id="44e31-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="44e31-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="44e31-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="44e31-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="44e31-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="44e31-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e31-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44e31-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e31-128">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="44e31-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="44e31-129">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="44e31-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





