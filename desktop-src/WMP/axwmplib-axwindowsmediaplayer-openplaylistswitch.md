---
title: Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer
description: L'evento OpenPlaylistSwitch si verifica quando viene avviata la riproduzione di un titolo su un DVD. | Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325868"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cfe31-105">Evento OpenPlaylistSwitch dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cfe31-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cfe31-106">L'evento OpenPlaylistSwitch si verifica quando viene avviata la riproduzione di un titolo su un DVD.</span><span class="sxs-lookup"><span data-stu-id="cfe31-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="cfe31-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="cfe31-107">Event Data</span></span>

<span data-ttu-id="cfe31-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_OpenPlaylistSwitchEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="cfe31-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="cfe31-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="cfe31-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="cfe31-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cfe31-110">Property</span></span>  | <span data-ttu-id="cfe31-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe31-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe31-112">**pItem**</span><span class="sxs-lookup"><span data-stu-id="cfe31-112">**pItem**</span></span> | <span data-ttu-id="cfe31-113">System. ObjectObject che rappresenta il titolo.</span><span class="sxs-lookup"><span data-stu-id="cfe31-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="cfe31-114">È possibile eseguire il cast di questo oggetto a un'interfaccia IWMPPlaylist per accedervi.</span><span class="sxs-lookup"><span data-stu-id="cfe31-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cfe31-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfe31-115">Requirements</span></span>



| <span data-ttu-id="cfe31-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe31-116">Requirement</span></span> | <span data-ttu-id="cfe31-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cfe31-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe31-118">Versione</span><span class="sxs-lookup"><span data-stu-id="cfe31-118">Version</span></span><br/>   | <span data-ttu-id="cfe31-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cfe31-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cfe31-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cfe31-120">Namespace</span></span><br/> | <span data-ttu-id="cfe31-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cfe31-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cfe31-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="cfe31-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cfe31-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cfe31-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe31-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfe31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe31-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cfe31-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cfe31-126">**Interfaccia IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cfe31-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





