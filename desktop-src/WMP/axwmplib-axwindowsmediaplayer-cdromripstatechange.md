---
title: Evento CdromRipStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromRipStateChange si verifica quando viene modificato lo stato di un'operazione di copia del CD.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Evento CdromRipStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323919"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="54808-104">Evento CdromRipStateChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="54808-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="54808-105">L'evento CdromRipStateChange si verifica quando viene modificato lo stato di un'operazione di copia del CD.</span><span class="sxs-lookup"><span data-stu-id="54808-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="54808-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="54808-106">Event Data</span></span>

<span data-ttu-id="54808-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromRipStateChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="54808-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="54808-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="54808-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="54808-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="54808-109">Property</span></span>  | <span data-ttu-id="54808-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54808-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54808-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="54808-111">pCdromRip</span></span> | <span data-ttu-id="54808-112">Interfaccia WMPLib. IWMPCdromRipThe che rappresenta l'operazione di strappo che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="54808-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="54808-113">wmprs</span><span class="sxs-lookup"><span data-stu-id="54808-113">wmprs</span></span>     | <span data-ttu-id="54808-114">Valore di enumerazione WMPLib. WMPRipStateThe che indica il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="54808-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="54808-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54808-115">Requirements</span></span>



| <span data-ttu-id="54808-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="54808-116">Requirement</span></span> | <span data-ttu-id="54808-117">Valore</span><span class="sxs-lookup"><span data-stu-id="54808-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54808-118">Versione</span><span class="sxs-lookup"><span data-stu-id="54808-118">Version</span></span><br/>   | <span data-ttu-id="54808-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="54808-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="54808-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="54808-120">Namespace</span></span><br/> | <span data-ttu-id="54808-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="54808-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="54808-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="54808-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="54808-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="54808-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54808-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54808-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54808-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="54808-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54808-126">**Interfaccia IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="54808-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="54808-127">**WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="54808-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





