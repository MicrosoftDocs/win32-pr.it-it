---
title: Evento OpenStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento OpenStateChange si verifica in seguito alla modifica del valore della proprietà openState. | Evento OpenStateChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- Evento OpenStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324586"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c62c8-105">Evento OpenStateChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c62c8-105">OpenStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c62c8-106">L'evento OpenStateChange si verifica in seguito alla modifica del valore della proprietà **openState** .</span><span class="sxs-lookup"><span data-stu-id="c62c8-106">The OpenStateChange event occurs when the **openState** property changes value.</span></span>

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a><span data-ttu-id="c62c8-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="c62c8-107">Event Data</span></span>

<span data-ttu-id="c62c8-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_OpenStateChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="c62c8-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEventHandler**.</span></span> <span data-ttu-id="c62c8-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenStateChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="c62c8-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c62c8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c62c8-110">Property</span></span> | <span data-ttu-id="c62c8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c62c8-111">Description</span></span>                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62c8-112">NewState</span><span class="sxs-lookup"><span data-stu-id="c62c8-112">NewState</span></span> | <span data-ttu-id="c62c8-113">System. Int32Specifies il nuovo stato aperto.</span><span class="sxs-lookup"><span data-stu-id="c62c8-113">System.Int32Specifies the new open state.</span></span> <span data-ttu-id="c62c8-114">Per una tabella di valori, vedere [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="c62c8-114">For a table of values, see [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c62c8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c62c8-115">Remarks</span></span>

<span data-ttu-id="c62c8-116">Windows Media Player può passare attraverso diversi stati aperti mentre tenta di aprire un file di rete, ad esempio l'individuazione del server, la connessione al server e infine l'apertura del file.</span><span class="sxs-lookup"><span data-stu-id="c62c8-116">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="c62c8-117">Questo evento verrà generato ogni volta che viene modificato lo stato di apertura.</span><span class="sxs-lookup"><span data-stu-id="c62c8-117">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="c62c8-118">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="c62c8-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="c62c8-119">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="c62c8-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="c62c8-120">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="c62c8-120">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="c62c8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c62c8-121">Requirements</span></span>



| <span data-ttu-id="c62c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c62c8-122">Requirement</span></span> | <span data-ttu-id="c62c8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c62c8-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c62c8-124">Versione</span><span class="sxs-lookup"><span data-stu-id="c62c8-124">Version</span></span><br/>   | <span data-ttu-id="c62c8-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c62c8-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c62c8-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c62c8-126">Namespace</span></span><br/> | <span data-ttu-id="c62c8-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c62c8-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c62c8-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="c62c8-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c62c8-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c62c8-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c62c8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c62c8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c62c8-131">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c62c8-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c62c8-132">**AxWindowsMediaPlayer. openState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c62c8-132">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





