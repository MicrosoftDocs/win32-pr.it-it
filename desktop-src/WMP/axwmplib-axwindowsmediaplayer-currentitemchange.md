---
title: Evento CurrentItemChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CurrentItemChange si verifica quando cambia il valore di IWMPControls. currentItem.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Evento CurrentItemChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325265"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="489a8-104">Evento CurrentItemChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="489a8-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="489a8-105">L'evento CurrentItemChange si verifica quando il valore di IWMPControls. **CurrentItem** modifiche.</span><span class="sxs-lookup"><span data-stu-id="489a8-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="489a8-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="489a8-106">Event Data</span></span>

<span data-ttu-id="489a8-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CurrentItemChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="489a8-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="489a8-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="489a8-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="489a8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="489a8-109">Property</span></span>   | <span data-ttu-id="489a8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="489a8-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489a8-111">pdispMedia</span><span class="sxs-lookup"><span data-stu-id="489a8-111">pdispMedia</span></span> | <span data-ttu-id="489a8-112">System. ObjectThe nuovo elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="489a8-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="489a8-113">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="489a8-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="489a8-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="489a8-114">Examples</span></span>

<span data-ttu-id="489a8-115">Nell'esempio seguente viene illustrato un gestore eventi per l'evento CurrentItemChange.</span><span class="sxs-lookup"><span data-stu-id="489a8-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="489a8-116">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="489a8-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="489a8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="489a8-117">Requirements</span></span>



| <span data-ttu-id="489a8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="489a8-118">Requirement</span></span> | <span data-ttu-id="489a8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="489a8-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489a8-120">Versione</span><span class="sxs-lookup"><span data-stu-id="489a8-120">Version</span></span><br/>   | <span data-ttu-id="489a8-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="489a8-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="489a8-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="489a8-122">Namespace</span></span><br/> | <span data-ttu-id="489a8-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="489a8-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="489a8-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="489a8-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="489a8-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="489a8-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489a8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="489a8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489a8-127">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="489a8-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="489a8-128">**IWMPControls. currentItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="489a8-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="489a8-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="489a8-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





