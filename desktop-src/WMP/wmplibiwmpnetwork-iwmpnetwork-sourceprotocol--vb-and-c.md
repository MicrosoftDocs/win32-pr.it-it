---
title: Proprietà sourceProtocol di IWMPNetwork
description: La proprietà sourceProtocol ottiene il protocollo di origine utilizzato per la ricezione dei dati.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- Finestra delle proprietà di sourceProtocol Media Player
- Proprietà di sourceProtocol Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà sourceProtocol
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333105"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="580ac-106">Proprietà IWMPNetwork:: sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="580ac-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="580ac-107">La proprietà **sourceProtocol** ottiene il protocollo di origine utilizzato per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="580ac-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="580ac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="580ac-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="580ac-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="580ac-109">Property value</span></span>

<span data-ttu-id="580ac-110">**System. String** che rappresenta il nome del protocollo di origine.</span><span class="sxs-lookup"><span data-stu-id="580ac-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="580ac-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="580ac-111">Remarks</span></span>

<span data-ttu-id="580ac-112">Questa proprietà ottiene una stringa di lunghezza zero ("") quando si riproduce un CD o un DVD.</span><span class="sxs-lookup"><span data-stu-id="580ac-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="580ac-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="580ac-113">Examples</span></span>

<span data-ttu-id="580ac-114">Nell'esempio di codice riportato di seguito viene utilizzato **sourceProtocol** per visualizzare il protocollo di origine utilizzato per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="580ac-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="580ac-115">Le informazioni vengono visualizzate in un'etichetta, in risposta all'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="580ac-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="580ac-116">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="580ac-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="580ac-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="580ac-117">Requirements</span></span>



| <span data-ttu-id="580ac-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="580ac-118">Requirement</span></span> | <span data-ttu-id="580ac-119">Valore</span><span class="sxs-lookup"><span data-stu-id="580ac-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="580ac-120">Versione</span><span class="sxs-lookup"><span data-stu-id="580ac-120">Version</span></span><br/>   | <span data-ttu-id="580ac-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="580ac-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="580ac-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="580ac-122">Namespace</span></span><br/> | <span data-ttu-id="580ac-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="580ac-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="580ac-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="580ac-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="580ac-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="580ac-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580ac-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="580ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580ac-127">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="580ac-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





