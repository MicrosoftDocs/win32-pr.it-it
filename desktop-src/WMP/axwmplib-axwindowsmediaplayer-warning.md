---
title: Evento di avviso dell'oggetto AxWindowsMediaPlayer
description: L'evento di avviso è riservato per un utilizzo futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento di avviso dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330896"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="5615b-104">Evento di avviso dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="5615b-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="5615b-105">L'evento di avviso è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="5615b-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="5615b-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="5615b-106">Event Data</span></span>

<span data-ttu-id="5615b-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_WarningEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="5615b-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="5615b-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="5615b-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="5615b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5615b-109">Property</span></span>    | <span data-ttu-id="5615b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5615b-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="5615b-111">warningType</span><span class="sxs-lookup"><span data-stu-id="5615b-111">warningType</span></span> | <span data-ttu-id="5615b-112">**System. Int32** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="5615b-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="5615b-113">param</span><span class="sxs-lookup"><span data-stu-id="5615b-113">param</span></span>       | <span data-ttu-id="5615b-114">**System. Int32** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="5615b-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="5615b-115">description</span><span class="sxs-lookup"><span data-stu-id="5615b-115">description</span></span> | <span data-ttu-id="5615b-116">**System. String** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="5615b-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5615b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5615b-117">Remarks</span></span>

<span data-ttu-id="5615b-118">Questo evento è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="5615b-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="5615b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5615b-119">Requirements</span></span>



| <span data-ttu-id="5615b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5615b-120">Requirement</span></span> | <span data-ttu-id="5615b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5615b-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5615b-122">Versione</span><span class="sxs-lookup"><span data-stu-id="5615b-122">Version</span></span><br/>   | <span data-ttu-id="5615b-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5615b-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="5615b-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5615b-124">Namespace</span></span><br/> | <span data-ttu-id="5615b-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="5615b-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="5615b-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="5615b-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5615b-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5615b-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5615b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5615b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5615b-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5615b-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





