---
title: Evento Disconnect dell'oggetto AxWindowsMediaPlayer
description: L'evento di disconnessione è riservato per un utilizzo futuro.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Evento Disconnect dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325587"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="fc1b4-104">Evento Disconnect dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="fc1b4-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="fc1b4-105">L'evento di disconnessione è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="fc1b4-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="fc1b4-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="fc1b4-106">Event Data</span></span>

<span data-ttu-id="fc1b4-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_DisconnectEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="fc1b4-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="fc1b4-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="fc1b4-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="fc1b4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc1b4-109">Property</span></span> | <span data-ttu-id="fc1b4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc1b4-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="fc1b4-111">result</span><span class="sxs-lookup"><span data-stu-id="fc1b4-111">result</span></span>   | <span data-ttu-id="fc1b4-112">**System. Int32** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="fc1b4-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fc1b4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc1b4-113">Remarks</span></span>

<span data-ttu-id="fc1b4-114">Questo evento è riservato per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="fc1b4-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1b4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc1b4-115">Requirements</span></span>



| <span data-ttu-id="fc1b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc1b4-116">Requirement</span></span> | <span data-ttu-id="fc1b4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fc1b4-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1b4-118">Versione</span><span class="sxs-lookup"><span data-stu-id="fc1b4-118">Version</span></span><br/>   | <span data-ttu-id="fc1b4-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fc1b4-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="fc1b4-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc1b4-120">Namespace</span></span><br/> | <span data-ttu-id="fc1b4-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="fc1b4-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="fc1b4-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="fc1b4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fc1b4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1b4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1b4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc1b4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1b4-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fc1b4-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





