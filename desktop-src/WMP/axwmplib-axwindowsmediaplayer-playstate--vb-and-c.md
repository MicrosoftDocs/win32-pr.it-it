---
title: Proprietà AxWindowsMediaPlayer. riproduzione
description: La proprietà riproduzione ottiene un valore di enumerazione che indica lo stato dell'operazione Windows Media Player.
ms.assetid: ab9f1547-5c28-4289-beaf-9262f7f59b07
keywords:
- Finestra delle proprietà di riproduzione Media Player
- Proprietà riproduzione Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà riproduzione
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d397c65c1cfd7f4adb040cc94e208a66c6c42d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332297"
---
# <a name="axwindowsmediaplayerplaystate-property"></a><span data-ttu-id="e585d-106">Proprietà AxWindowsMediaPlayer. riproduzione</span><span class="sxs-lookup"><span data-stu-id="e585d-106">AxWindowsMediaPlayer.playState property</span></span>

<span data-ttu-id="e585d-107">La proprietà riproduzione ottiene un valore di enumerazione che indica lo stato dell'operazione Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e585d-107">The playState property gets an enumeration value indicating the state of the Windows Media Player operation.</span></span>

<span data-ttu-id="e585d-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e585d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e585d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e585d-109">Syntax</span></span>


```CSharp
public WMPPlayState playState {get;}
```


```VB

Public ReadOnly Property playState As WMPPlayState
```





## <a name="property-value"></a><span data-ttu-id="e585d-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e585d-110">Property value</span></span>

<span data-ttu-id="e585d-111">Valore di enumerazione WMPLib. WMPPlayState.</span><span class="sxs-lookup"><span data-stu-id="e585d-111">The WMPLib.WMPPlayState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e585d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e585d-112">Remarks</span></span>

<span data-ttu-id="e585d-113">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="e585d-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="e585d-114">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="e585d-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="e585d-115">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="e585d-115">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="e585d-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="e585d-116">Examples</span></span>

<span data-ttu-id="e585d-117">Nell'esempio seguente viene usata la proprietà riproduzione per visualizzare lo stato di riproduzione corrente del lettore in un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="e585d-117">The following example uses the playState property to display the current playing status of the player in a label.</span></span> <span data-ttu-id="e585d-118">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="e585d-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Test whether Windows Media Player is in the playing state. 
if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
{
    playStateLabel.Text = "Windows Media Player is playing!";
}
else
{
    playStateLabel.Text = "Windows Media Player is NOT playing!";
}
```


```VB

' Test whether Windows Media Player is in the playing state. 
If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

    playStateLabel.Text = &quot;Windows Media Player is playing!&quot;

Else

    playStateLabel.Text = &quot;Windows Media Player is NOT playing!&quot;

End If
```





## <a name="requirements"></a><span data-ttu-id="e585d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e585d-119">Requirements</span></span>



| <span data-ttu-id="e585d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e585d-120">Requirement</span></span> | <span data-ttu-id="e585d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e585d-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e585d-122">Versione</span><span class="sxs-lookup"><span data-stu-id="e585d-122">Version</span></span><br/>   | <span data-ttu-id="e585d-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e585d-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e585d-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e585d-124">Namespace</span></span><br/> | <span data-ttu-id="e585d-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="e585d-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e585d-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="e585d-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e585d-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e585d-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e585d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e585d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e585d-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e585d-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e585d-130">**Evento AxWindowsMediaPlayer. PlayStateChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e585d-130">**AxWindowsMediaPlayer.PlayStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="e585d-131">**WMPPlayState**</span><span class="sxs-lookup"><span data-stu-id="e585d-131">**WMPPlayState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





