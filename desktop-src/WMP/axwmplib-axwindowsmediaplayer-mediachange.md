---
title: Evento MediaChange dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaChange si verifica quando viene modificato un elemento multimediale. | Evento MediaChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- Evento MediaChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329445"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="401b7-105">Evento MediaChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="401b7-105">MediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="401b7-106">L'evento MediaChange si verifica quando viene modificato un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="401b7-106">The MediaChange event occurs when a media item changes.</span></span>

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a><span data-ttu-id="401b7-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="401b7-107">Event Data</span></span>

<span data-ttu-id="401b7-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="401b7-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEventHandler**.</span></span> <span data-ttu-id="401b7-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="401b7-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="401b7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="401b7-110">Property</span></span> | <span data-ttu-id="401b7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="401b7-111">Description</span></span>                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="401b7-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="401b7-112">Item</span></span>     | <span data-ttu-id="401b7-113">Elemento multimediale System. ObjectThe modificato.</span><span class="sxs-lookup"><span data-stu-id="401b7-113">System.ObjectThe media item that changed.</span></span> <span data-ttu-id="401b7-114">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="401b7-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="401b7-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="401b7-115">Examples</span></span>

<span data-ttu-id="401b7-116">Nell'esempio seguente viene utilizzata un'etichetta per visualizzare il nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="401b7-116">The following example uses a label to display the name of the current media item.</span></span> <span data-ttu-id="401b7-117">Il codice aggiorna il testo nell'etichetta a ogni occorrenza dell'evento MediaChange.</span><span class="sxs-lookup"><span data-stu-id="401b7-117">The code updates the text in the label with each occurrence of the MediaChange Event.</span></span> <span data-ttu-id="401b7-118">L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="401b7-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="401b7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="401b7-119">Requirements</span></span>



| <span data-ttu-id="401b7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="401b7-120">Requirement</span></span> | <span data-ttu-id="401b7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="401b7-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="401b7-122">Versione</span><span class="sxs-lookup"><span data-stu-id="401b7-122">Version</span></span><br/>   | <span data-ttu-id="401b7-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="401b7-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="401b7-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="401b7-124">Namespace</span></span><br/> | <span data-ttu-id="401b7-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="401b7-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="401b7-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="401b7-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="401b7-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="401b7-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="401b7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="401b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401b7-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="401b7-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="401b7-130">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="401b7-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





