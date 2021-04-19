---
title: Proprietà bufferingCount di IWMPNetwork
description: La proprietà bufferingCount ottiene il numero di volte in cui si è verificato il buffer durante la riproduzione.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- Finestra delle proprietà di bufferingCount Media Player
- Proprietà di bufferingCount Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325698"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="efa25-106">Proprietà IWMPNetwork:: bufferingCount</span><span class="sxs-lookup"><span data-stu-id="efa25-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="efa25-107">La proprietà **bufferingCount** ottiene il numero di volte in cui si è verificato il buffer durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="efa25-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa25-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efa25-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="efa25-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="efa25-109">Property value</span></span>

<span data-ttu-id="efa25-110">**System. Int32** che rappresenta il numero di buffer.</span><span class="sxs-lookup"><span data-stu-id="efa25-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="efa25-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="efa25-111">Remarks</span></span>

<span data-ttu-id="efa25-112">Ogni volta che la riproduzione viene arrestata e riavviata, questa proprietà viene reimpostata su zero.</span><span class="sxs-lookup"><span data-stu-id="efa25-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="efa25-113">Non viene reimpostato se la riproduzione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="efa25-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="efa25-114">Il buffering si applica solo ai contenuti in streaming.</span><span class="sxs-lookup"><span data-stu-id="efa25-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="efa25-115">Questa proprietà ottiene informazioni valide solo in fase di esecuzione quando l'URL per la riproduzione viene impostato tramite la proprietà **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="efa25-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="efa25-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="efa25-116">Examples</span></span>

<span data-ttu-id="efa25-117">Nell'esempio seguente viene usato *bufferingCount* per visualizzare il numero di volte in cui si verifica il buffer durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="efa25-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="efa25-118">Le informazioni vengono visualizzate in un'etichetta in risposta all'evento di buffering.</span><span class="sxs-lookup"><span data-stu-id="efa25-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="efa25-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="efa25-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="efa25-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efa25-120">Requirements</span></span>



| <span data-ttu-id="efa25-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="efa25-121">Requirement</span></span> | <span data-ttu-id="efa25-122">Valore</span><span class="sxs-lookup"><span data-stu-id="efa25-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa25-123">Versione</span><span class="sxs-lookup"><span data-stu-id="efa25-123">Version</span></span><br/>   | <span data-ttu-id="efa25-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="efa25-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="efa25-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="efa25-125">Namespace</span></span><br/> | <span data-ttu-id="efa25-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="efa25-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="efa25-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="efa25-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="efa25-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="efa25-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efa25-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efa25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efa25-130">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="efa25-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="efa25-131">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="efa25-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





