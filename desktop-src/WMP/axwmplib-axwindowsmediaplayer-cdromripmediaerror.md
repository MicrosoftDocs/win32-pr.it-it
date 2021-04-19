---
title: Evento CdromRipMediaError dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromRipMediaError si verifica quando si verifica un errore durante l'estrazione di una singola traccia da un CD.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- Evento CdromRipMediaError dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b429505996cd5e85bc1e0e2e85c3f47103d244
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323922"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7804c-104">Evento CdromRipMediaError dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7804c-104">CdromRipMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7804c-105">L'evento CdromRipMediaError si verifica quando si verifica un errore durante l'estrazione di una singola traccia da un CD.</span><span class="sxs-lookup"><span data-stu-id="7804c-105">The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.</span></span>

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a><span data-ttu-id="7804c-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="7804c-106">Event Data</span></span>

<span data-ttu-id="7804c-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromRipMediaErrorEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="7804c-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEventHandler**.</span></span> <span data-ttu-id="7804c-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipMediaErrorEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="7804c-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="7804c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7804c-109">Property</span></span>  | <span data-ttu-id="7804c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7804c-110">Description</span></span>                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7804c-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="7804c-111">pCdromRip</span></span> | <span data-ttu-id="7804c-112">Interfaccia WMPLib. IWMPCdromRipThe che rappresenta l'operazione di strappo che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="7804c-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/>                |
| <span data-ttu-id="7804c-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="7804c-113">pMedia</span></span>    | <span data-ttu-id="7804c-114">Elemento multimediale System. ObjectThe che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="7804c-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="7804c-115">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="7804c-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7804c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7804c-116">Requirements</span></span>



| <span data-ttu-id="7804c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7804c-117">Requirement</span></span> | <span data-ttu-id="7804c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7804c-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7804c-119">Versione</span><span class="sxs-lookup"><span data-stu-id="7804c-119">Version</span></span><br/>   | <span data-ttu-id="7804c-120">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="7804c-120">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="7804c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7804c-121">Namespace</span></span><br/> | <span data-ttu-id="7804c-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7804c-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7804c-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="7804c-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7804c-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7804c-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7804c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7804c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7804c-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7804c-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7804c-127">**Interfaccia IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7804c-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7804c-128">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7804c-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





