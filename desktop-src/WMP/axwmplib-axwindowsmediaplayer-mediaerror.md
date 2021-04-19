---
title: Evento errore MediaError dell'oggetto AxWindowsMediaPlayer
description: L'evento errore MediaError si verifica quando un oggetto multimediale presenta una condizione di errore.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Evento errore MediaError dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331869"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cb574-104">Evento errore MediaError dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cb574-104">MediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cb574-105">L'evento errore MediaError si verifica quando un oggetto multimediale presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="cb574-105">The MediaError event occurs when a media object has an error condition.</span></span>

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a><span data-ttu-id="cb574-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="cb574-106">Event Data</span></span>

<span data-ttu-id="cb574-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_MediaErrorEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="cb574-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEventHandler**.</span></span> <span data-ttu-id="cb574-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="cb574-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaErrorEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="cb574-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cb574-109">Property</span></span>     | <span data-ttu-id="cb574-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb574-110">Description</span></span>                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb574-111">pMediaObject</span><span class="sxs-lookup"><span data-stu-id="cb574-111">pMediaObject</span></span> | <span data-ttu-id="cb574-112">System. ObjectObject che presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="cb574-112">System.ObjectObject that has an error condition.</span></span> <span data-ttu-id="cb574-113">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPMedia per accedervi.</span><span class="sxs-lookup"><span data-stu-id="cb574-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb574-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb574-114">Requirements</span></span>



| <span data-ttu-id="cb574-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb574-115">Requirement</span></span> | <span data-ttu-id="cb574-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cb574-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb574-117">Versione</span><span class="sxs-lookup"><span data-stu-id="cb574-117">Version</span></span><br/>   | <span data-ttu-id="cb574-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cb574-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cb574-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cb574-119">Namespace</span></span><br/> | <span data-ttu-id="cb574-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cb574-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cb574-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="cb574-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cb574-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cb574-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb574-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb574-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb574-124">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb574-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb574-125">**Interfaccia IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb574-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





