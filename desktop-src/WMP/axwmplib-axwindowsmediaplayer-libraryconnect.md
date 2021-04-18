---
title: Evento LibraryConnect dell'oggetto AxWindowsMediaPlayer
description: L'evento LibraryConnect si verifica quando una raccolta diventa disponibile.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Evento LibraryConnect dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331886"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="906d4-104">Evento LibraryConnect dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="906d4-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="906d4-105">L'evento LibraryConnect si verifica quando una raccolta diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="906d4-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="906d4-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="906d4-106">Event Data</span></span>

<span data-ttu-id="906d4-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_LibraryConnectEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="906d4-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="906d4-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="906d4-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="906d4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="906d4-109">Property</span></span> | <span data-ttu-id="906d4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="906d4-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="906d4-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="906d4-111">pLibrary</span></span> | <span data-ttu-id="906d4-112">**Wmplib. IWMPLibrary** Interfaccia che rappresenta la libreria connessa.</span><span class="sxs-lookup"><span data-stu-id="906d4-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="906d4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="906d4-113">Remarks</span></span>

<span data-ttu-id="906d4-114">Questo evento non si verifica per la libreria locale.</span><span class="sxs-lookup"><span data-stu-id="906d4-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="906d4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="906d4-115">Requirements</span></span>



| <span data-ttu-id="906d4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="906d4-116">Requirement</span></span> | <span data-ttu-id="906d4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="906d4-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="906d4-118">Versione</span><span class="sxs-lookup"><span data-stu-id="906d4-118">Version</span></span><br/>   | <span data-ttu-id="906d4-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="906d4-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="906d4-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="906d4-120">Namespace</span></span><br/> | <span data-ttu-id="906d4-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="906d4-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="906d4-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="906d4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="906d4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="906d4-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="906d4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="906d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906d4-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="906d4-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="906d4-126">**Interfaccia IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="906d4-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





