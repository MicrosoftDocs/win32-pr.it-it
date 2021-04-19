---
title: Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer
description: L'evento PlaylistChange si verifica quando viene modificata una playlist. | Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332310"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b56ba-105">Evento PlaylistChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="b56ba-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b56ba-106">L'evento PlaylistChange si verifica quando viene modificata una playlist.</span><span class="sxs-lookup"><span data-stu-id="b56ba-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="b56ba-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="b56ba-107">Event Data</span></span>

<span data-ttu-id="b56ba-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_PlaylistChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="b56ba-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="b56ba-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="b56ba-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="b56ba-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b56ba-110">Property</span></span>     | <span data-ttu-id="b56ba-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b56ba-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56ba-112">**playlist**</span><span class="sxs-lookup"><span data-stu-id="b56ba-112">**playlist**</span></span> | <span data-ttu-id="b56ba-113">Oggetto System. ObjectThe che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="b56ba-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="b56ba-114">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPPlaylist per accedervi.</span><span class="sxs-lookup"><span data-stu-id="b56ba-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="b56ba-115">**change**</span><span class="sxs-lookup"><span data-stu-id="b56ba-115">**change**</span></span>   | <span data-ttu-id="b56ba-116">Valore di enumerazione WMPLib. WMPPlaylistChangeEventTypeAn che indica il tipo di modifica apportata alla playlist.</span><span class="sxs-lookup"><span data-stu-id="b56ba-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b56ba-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b56ba-117">Requirements</span></span>



| <span data-ttu-id="b56ba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b56ba-118">Requirement</span></span> | <span data-ttu-id="b56ba-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b56ba-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b56ba-120">Versione</span><span class="sxs-lookup"><span data-stu-id="b56ba-120">Version</span></span><br/>   | <span data-ttu-id="b56ba-121">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b56ba-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b56ba-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b56ba-122">Namespace</span></span><br/> | <span data-ttu-id="b56ba-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b56ba-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b56ba-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="b56ba-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b56ba-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b56ba-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56ba-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b56ba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56ba-127">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b56ba-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b56ba-128">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b56ba-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





