---
title: Evento EndOfStream dell'oggetto AxWindowsMediaPlayer
description: L'evento EndOfStream è riservato per un utilizzo futuro.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Evento EndOfStream dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324396"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c2e1f-104">Evento EndOfStream dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c2e1f-104">EndOfStream Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c2e1f-105">L'evento EndOfStream è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-105">The EndOfStream event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a><span data-ttu-id="c2e1f-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="c2e1f-106">Event Data</span></span>

<span data-ttu-id="c2e1f-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_EndOfStreamEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEventHandler**.</span></span> <span data-ttu-id="c2e1f-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c2e1f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c2e1f-109">Property</span></span> | <span data-ttu-id="c2e1f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2e1f-110">Description</span></span>                           |
|----------|---------------------------------------|
| <span data-ttu-id="c2e1f-111">result</span><span class="sxs-lookup"><span data-stu-id="c2e1f-111">result</span></span>   | <span data-ttu-id="c2e1f-112">System. Int32Not supportato.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-112">System.Int32Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2e1f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2e1f-113">Remarks</span></span>

<span data-ttu-id="c2e1f-114">Questo evento è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e1f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2e1f-115">Requirements</span></span>



| <span data-ttu-id="c2e1f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e1f-116">Requirement</span></span> | <span data-ttu-id="c2e1f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c2e1f-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e1f-118">Versione</span><span class="sxs-lookup"><span data-stu-id="c2e1f-118">Version</span></span><br/>   | <span data-ttu-id="c2e1f-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c2e1f-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c2e1f-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2e1f-120">Namespace</span></span><br/> | <span data-ttu-id="c2e1f-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c2e1f-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c2e1f-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c2e1f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c2e1f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e1f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e1f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2e1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e1f-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2e1f-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





