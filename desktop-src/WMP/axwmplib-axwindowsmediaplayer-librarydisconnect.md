---
title: Evento LibraryDisconnect dell'oggetto AxWindowsMediaPlayer
description: L'evento LibraryDisconnect si verifica quando una libreria non è più disponibile.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Evento LibraryDisconnect dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331884"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="187f8-104">Evento LibraryDisconnect dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="187f8-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="187f8-105">L'evento LibraryDisconnect si verifica quando una libreria non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="187f8-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="187f8-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="187f8-106">Event Data</span></span>

<span data-ttu-id="187f8-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_LibraryDisconnectEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="187f8-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="187f8-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="187f8-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="187f8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="187f8-109">Property</span></span> | <span data-ttu-id="187f8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="187f8-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="187f8-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="187f8-111">pLibrary</span></span> | <span data-ttu-id="187f8-112">**Wmplib. IWMPLibrary** Interfaccia che rappresenta la libreria disconnessa.</span><span class="sxs-lookup"><span data-stu-id="187f8-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="187f8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="187f8-113">Remarks</span></span>

<span data-ttu-id="187f8-114">Questo evento non si verifica per la libreria locale.</span><span class="sxs-lookup"><span data-stu-id="187f8-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="187f8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="187f8-115">Requirements</span></span>



| <span data-ttu-id="187f8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="187f8-116">Requirement</span></span> | <span data-ttu-id="187f8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="187f8-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="187f8-118">Versione</span><span class="sxs-lookup"><span data-stu-id="187f8-118">Version</span></span><br/>   | <span data-ttu-id="187f8-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="187f8-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="187f8-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="187f8-120">Namespace</span></span><br/> | <span data-ttu-id="187f8-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="187f8-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="187f8-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="187f8-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="187f8-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="187f8-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187f8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="187f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187f8-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="187f8-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="187f8-126">**Interfaccia IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="187f8-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





