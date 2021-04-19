---
title: Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe. | Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324105"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cd333-105">Evento StringCollectionChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cd333-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cd333-106">L'evento StringCollectionChange si verifica quando viene modificata una raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="cd333-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="cd333-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="cd333-107">Event Data</span></span>

<span data-ttu-id="cd333-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_StringCollectionChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="cd333-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="cd333-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="cd333-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="cd333-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd333-110">Property</span></span>              | <span data-ttu-id="cd333-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd333-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd333-112">pdispStringCollection</span><span class="sxs-lookup"><span data-stu-id="cd333-112">pdispStringCollection</span></span> | <span data-ttu-id="cd333-113">Elemento della raccolta di stringhe System. ObjectThe modificato.</span><span class="sxs-lookup"><span data-stu-id="cd333-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="cd333-114">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPStringCollection per accedervi.</span><span class="sxs-lookup"><span data-stu-id="cd333-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="cd333-115">lCollectionIndex</span><span class="sxs-lookup"><span data-stu-id="cd333-115">lCollectionIndex</span></span>      | <span data-ttu-id="cd333-116">Indice System. Int32The dell'elemento della raccolta di stringhe modificato.</span><span class="sxs-lookup"><span data-stu-id="cd333-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="cd333-117">change (modifica)</span><span class="sxs-lookup"><span data-stu-id="cd333-117">change</span></span>                | <span data-ttu-id="cd333-118">Valore di enumerazione WMPLib. WMPStringCollectionChangeEventTypeAn che indica il tipo di modifica che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="cd333-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="cd333-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd333-119">Requirements</span></span>



| <span data-ttu-id="cd333-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd333-120">Requirement</span></span> | <span data-ttu-id="cd333-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cd333-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd333-122">Versione</span><span class="sxs-lookup"><span data-stu-id="cd333-122">Version</span></span><br/>   | <span data-ttu-id="cd333-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cd333-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cd333-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd333-124">Namespace</span></span><br/> | <span data-ttu-id="cd333-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cd333-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cd333-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="cd333-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cd333-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cd333-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd333-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd333-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd333-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cd333-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cd333-130">**Interfaccia IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cd333-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cd333-131">**WMPStringCollectionChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="cd333-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





