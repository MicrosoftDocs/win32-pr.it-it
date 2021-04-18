---
title: Evento MarkerHit dell'oggetto AxWindowsMediaPlayer
description: L'evento MarkerHit si verifica quando viene raggiunto un marcatore. | Evento MarkerHit dell'oggetto AxWindowsMediaPlayer
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Evento MarkerHit dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331883"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9abe1-105">Evento MarkerHit dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9abe1-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9abe1-106">L'evento MarkerHit si verifica quando viene raggiunto un marcatore.</span><span class="sxs-lookup"><span data-stu-id="9abe1-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="9abe1-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="9abe1-107">Event Data</span></span>

<span data-ttu-id="9abe1-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MarkerHitEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="9abe1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="9abe1-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="9abe1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9abe1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9abe1-110">Property</span></span>      | <span data-ttu-id="9abe1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9abe1-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9abe1-112">**MarkerNum**</span><span class="sxs-lookup"><span data-stu-id="9abe1-112">**MarkerNum**</span></span> | <span data-ttu-id="9abe1-113">System. Int32Indicates il numero del marcatore raggiunto.</span><span class="sxs-lookup"><span data-stu-id="9abe1-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9abe1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9abe1-114">Requirements</span></span>



| <span data-ttu-id="9abe1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9abe1-115">Requirement</span></span> | <span data-ttu-id="9abe1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9abe1-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9abe1-117">Versione</span><span class="sxs-lookup"><span data-stu-id="9abe1-117">Version</span></span><br/>   | <span data-ttu-id="9abe1-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9abe1-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9abe1-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9abe1-119">Namespace</span></span><br/> | <span data-ttu-id="9abe1-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9abe1-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9abe1-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="9abe1-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9abe1-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9abe1-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abe1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9abe1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abe1-124">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9abe1-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





