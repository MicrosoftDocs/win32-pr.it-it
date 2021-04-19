---
title: Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer
description: L'evento CurrentMediaItemAvailable si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente. | Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331891"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c3678-105">Evento CurrentMediaItemAvailable dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c3678-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c3678-106">L'evento CurrentMediaItemAvailable si verifica quando diventa disponibile un elemento di metadati grafici nell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="c3678-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="c3678-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="c3678-107">Event Data</span></span>

<span data-ttu-id="c3678-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CurrentMediaItemAvailableEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="c3678-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="c3678-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="c3678-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c3678-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c3678-110">Property</span></span>     | <span data-ttu-id="c3678-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3678-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="c3678-112">bstrItemName</span><span class="sxs-lookup"><span data-stu-id="c3678-112">bstrItemName</span></span> | <span data-ttu-id="c3678-113">System. StringThe nome dell'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="c3678-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3678-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3678-114">Remarks</span></span>

<span data-ttu-id="c3678-115">Poiché la riproduzione può iniziare prima che un elemento multimediale venga scaricato completamente, eventuali elementi grafici dei metadati contenuti nell'elemento multimediale, ad esempio Album Cover Art, potrebbero non essere disponibili quando viene avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c3678-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="c3678-116">Questo evento avvisa l'utente al termine del download di un elemento grafico dei metadati.</span><span class="sxs-lookup"><span data-stu-id="c3678-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="c3678-117">È quindi possibile recuperare l'interfaccia **IWMPMedia** passando il valore di **bstrItemName** a *IWMPMediaCollection*. metodo **GetByName** , dopo il quale è possibile accedere all'elemento grafico dei metadati utilizzando *IWMPMedia3*. **getItemInfoByType** e specificando **WM/Picture** per il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="c3678-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3678-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3678-118">Requirements</span></span>



| <span data-ttu-id="c3678-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3678-119">Requirement</span></span> | <span data-ttu-id="c3678-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c3678-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3678-121">Versione</span><span class="sxs-lookup"><span data-stu-id="c3678-121">Version</span></span><br/>   | <span data-ttu-id="c3678-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c3678-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c3678-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3678-123">Namespace</span></span><br/> | <span data-ttu-id="c3678-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3678-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c3678-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3678-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3678-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3678-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3678-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3678-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3678-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3678-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3678-129">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3678-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3678-130">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3678-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3678-131">**IWMPMediaCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3678-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





