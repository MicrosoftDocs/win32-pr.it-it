---
title: Evento di buffering dell'oggetto AxWindowsMediaPlayer
description: L'evento di buffering si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download. | Evento di buffering dell'oggetto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento di buffering dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323929"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="49604-105">Evento di buffering dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="49604-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="49604-106">L'evento di buffering si verifica quando il controllo Media Player Windows inizia o termina il buffering o il download.</span><span class="sxs-lookup"><span data-stu-id="49604-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="49604-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="49604-107">Event Data</span></span>

<span data-ttu-id="49604-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_BufferingEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="49604-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="49604-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="49604-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="49604-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="49604-110">Property</span></span> | <span data-ttu-id="49604-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49604-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49604-112">Inizia</span><span class="sxs-lookup"><span data-stu-id="49604-112">Start</span></span>    | <span data-ttu-id="49604-113">System. BooleanSpecifies se la memorizzazione nel buffer è iniziata o terminata.</span><span class="sxs-lookup"><span data-stu-id="49604-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="49604-114">Il valore true indica che è iniziata. il valore false indica che è terminato.</span><span class="sxs-lookup"><span data-stu-id="49604-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="49604-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="49604-115">Remarks</span></span>

<span data-ttu-id="49604-116">Utilizzare questo evento per determinare quando viene avviata o arrestata la memorizzazione nel buffer o il download.</span><span class="sxs-lookup"><span data-stu-id="49604-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="49604-117">È possibile usare lo stesso blocco di eventi per entrambi i casi e *IWMPNetwork* di test. **bufferingProgress** e *IWMPNetwork*. **downloadProgress** per determinare se Windows Media Player sta attualmente memorizzando nel buffer o scaricando il contenuto.</span><span class="sxs-lookup"><span data-stu-id="49604-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="49604-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49604-118">Requirements</span></span>



| <span data-ttu-id="49604-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="49604-119">Requirement</span></span> | <span data-ttu-id="49604-120">Valore</span><span class="sxs-lookup"><span data-stu-id="49604-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49604-121">Versione</span><span class="sxs-lookup"><span data-stu-id="49604-121">Version</span></span><br/>   | <span data-ttu-id="49604-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="49604-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="49604-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49604-123">Namespace</span></span><br/> | <span data-ttu-id="49604-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="49604-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="49604-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="49604-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="49604-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="49604-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49604-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49604-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49604-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49604-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49604-129">**IWMPNetwork. bufferingProgress (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49604-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49604-130">**IWMPNetwork. downloadProgress (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49604-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





