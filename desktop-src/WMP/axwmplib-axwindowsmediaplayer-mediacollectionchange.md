---
title: Evento MediaCollectionChange dell'oggetto AxWindowsMediaPlayer
description: L'evento MediaCollectionChange si verifica quando viene modificata la raccolta di supporti. | Evento MediaCollectionChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 99a6d512-ed8e-4f1b-856a-22ca8092741d
keywords:
- Evento MediaCollectionChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- MediaCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720207de3475544074b87c56686d0a47da97785c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331873"
---
# <a name="mediacollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cf45e-105">Evento MediaCollectionChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cf45e-105">MediaCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cf45e-106">L'evento MediaCollectionChange si verifica quando viene modificata la raccolta di supporti.</span><span class="sxs-lookup"><span data-stu-id="cf45e-106">The MediaCollectionChange event occurs when the media collection changes.</span></span>

``` syntax
[C#]
private void player_MediaCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_MediaCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.MediaCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="cf45e-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="cf45e-107">Event Data</span></span>

<span data-ttu-id="cf45e-108">Questo evento non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="cf45e-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf45e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf45e-109">Requirements</span></span>



| <span data-ttu-id="cf45e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf45e-110">Requirement</span></span> | <span data-ttu-id="cf45e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="cf45e-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf45e-112">Versione</span><span class="sxs-lookup"><span data-stu-id="cf45e-112">Version</span></span><br/>   | <span data-ttu-id="cf45e-113">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cf45e-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cf45e-114">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf45e-114">Namespace</span></span><br/> | <span data-ttu-id="cf45e-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="cf45e-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cf45e-116">Assembly</span><span class="sxs-lookup"><span data-stu-id="cf45e-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf45e-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf45e-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf45e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf45e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf45e-119">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cf45e-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf45e-120">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cf45e-120">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf45e-121">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cf45e-121">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





