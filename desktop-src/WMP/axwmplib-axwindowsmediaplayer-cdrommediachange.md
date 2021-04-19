---
title: Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer
description: L'evento CdromMediaChange si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD. | Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323924"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c060c-105">Evento CdromMediaChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c060c-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c060c-106">L'evento **CdromMediaChange** si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="c060c-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="c060c-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="c060c-107">Event Data</span></span>

<span data-ttu-id="c060c-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_CdromMediaChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="c060c-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="c060c-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="c060c-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c060c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c060c-110">Property</span></span> | <span data-ttu-id="c060c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c060c-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="c060c-112">CdromNum</span><span class="sxs-lookup"><span data-stu-id="c060c-112">CdromNum</span></span> | <span data-ttu-id="c060c-113">System. Int32Specifies l'indice dell'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="c060c-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c060c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c060c-114">Remarks</span></span>

<span data-ttu-id="c060c-115">L'indice dell'unità CD corrisponde all'indice di un'interfaccia IWMPCdrom accessibile tramite l'interfaccia IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="c060c-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c060c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c060c-116">Requirements</span></span>



| <span data-ttu-id="c060c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c060c-117">Requirement</span></span> | <span data-ttu-id="c060c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c060c-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c060c-119">Versione</span><span class="sxs-lookup"><span data-stu-id="c060c-119">Version</span></span><br/>   | <span data-ttu-id="c060c-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c060c-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c060c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c060c-121">Namespace</span></span><br/> | <span data-ttu-id="c060c-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c060c-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c060c-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="c060c-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c060c-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c060c-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c060c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c060c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c060c-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c060c-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c060c-127">**Interfaccia IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c060c-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c060c-128">**Interfaccia IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c060c-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





