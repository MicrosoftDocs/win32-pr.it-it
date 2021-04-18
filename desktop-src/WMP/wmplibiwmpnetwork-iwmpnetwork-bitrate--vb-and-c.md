---
title: Proprietà bitrate IWMPNetwork
description: La proprietà bitrate ottiene la velocità in bit corrente ricevuta.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- Finestre delle proprietà bitrate Media Player
- Proprietà bitrate Media Player di Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà bitrate
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325699"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="f79d8-106">Proprietà IWMPNetwork:: bitrate</span><span class="sxs-lookup"><span data-stu-id="f79d8-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="f79d8-107">La proprietà **bitrate** ottiene la velocità in bit corrente ricevuta.</span><span class="sxs-lookup"><span data-stu-id="f79d8-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79d8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f79d8-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f79d8-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f79d8-109">Property value</span></span>

<span data-ttu-id="f79d8-110">**System. Int32** che rappresenta la velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="f79d8-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="f79d8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f79d8-111">Remarks</span></span>

<span data-ttu-id="f79d8-112">Il valore di questa proprietà è una combinazione della velocità in bit dei flussi video e audio.</span><span class="sxs-lookup"><span data-stu-id="f79d8-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="f79d8-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="f79d8-113">Examples</span></span>

<span data-ttu-id="f79d8-114">Nell'esempio seguente viene usata la **velocità in bit** per visualizzare la velocità in bit del supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="f79d8-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="f79d8-115">Le informazioni vengono visualizzate in un'etichetta in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="f79d8-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="f79d8-116">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="f79d8-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f79d8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f79d8-117">Requirements</span></span>



| <span data-ttu-id="f79d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f79d8-118">Requirement</span></span> | <span data-ttu-id="f79d8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f79d8-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79d8-120">Versione</span><span class="sxs-lookup"><span data-stu-id="f79d8-120">Version</span></span><br/>   | <span data-ttu-id="f79d8-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f79d8-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f79d8-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f79d8-122">Namespace</span></span><br/> | <span data-ttu-id="f79d8-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f79d8-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f79d8-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="f79d8-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f79d8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f79d8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f79d8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f79d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79d8-127">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f79d8-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





