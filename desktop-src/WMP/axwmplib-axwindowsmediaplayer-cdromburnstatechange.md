---
title: Evento CdromBurnStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromBurnStateChange si verifica quando cambia lo stato di un'operazione di masterizzazione CD.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromBurnStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323926"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="60c7f-104">Evento CdromBurnStateChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="60c7f-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="60c7f-105">L'evento CdromBurnStateChange si verifica quando cambia lo stato di un'operazione di masterizzazione CD.</span><span class="sxs-lookup"><span data-stu-id="60c7f-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="60c7f-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="60c7f-106">Event Data</span></span>

<span data-ttu-id="60c7f-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromBurnStateChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="60c7f-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="60c7f-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, che contiene le seguenti proprietà correlate a questo evento.</span><span class="sxs-lookup"><span data-stu-id="60c7f-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="60c7f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="60c7f-109">Property</span></span>   | <span data-ttu-id="60c7f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60c7f-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c7f-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="60c7f-111">pCdromBurn</span></span> | <span data-ttu-id="60c7f-112">Interfaccia WMPLib. IWMPCdromBurnThe che rappresenta l'operazione di masterizzazione che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="60c7f-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="60c7f-113">wmpbs</span><span class="sxs-lookup"><span data-stu-id="60c7f-113">wmpbs</span></span>      | <span data-ttu-id="60c7f-114">Valore di enumerazione WMPLib. WMPBurnStateThe che indica il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="60c7f-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="60c7f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60c7f-115">Requirements</span></span>



| <span data-ttu-id="60c7f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c7f-116">Requirement</span></span> | <span data-ttu-id="60c7f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="60c7f-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c7f-118">Versione</span><span class="sxs-lookup"><span data-stu-id="60c7f-118">Version</span></span><br/>   | <span data-ttu-id="60c7f-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="60c7f-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="60c7f-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="60c7f-120">Namespace</span></span><br/> | <span data-ttu-id="60c7f-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="60c7f-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="60c7f-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="60c7f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="60c7f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="60c7f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c7f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60c7f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c7f-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="60c7f-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="60c7f-126">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="60c7f-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="60c7f-127">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="60c7f-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





