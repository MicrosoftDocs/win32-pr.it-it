---
title: Evento FolderScanStateChange dell'oggetto AxWindowsMediaPlayer
description: L'evento FolderScanStateChange si verifica quando viene modificato lo stato di un'operazione di monitoraggio della cartella.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Evento FolderScanStateChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324386"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="48d08-104">Evento FolderScanStateChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="48d08-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="48d08-105">L'evento FolderScanStateChange si verifica quando viene modificato lo stato di un'operazione di monitoraggio della cartella.</span><span class="sxs-lookup"><span data-stu-id="48d08-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="48d08-106">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="48d08-106">Event Data</span></span>

<span data-ttu-id="48d08-107">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_FolderScanStateChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="48d08-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="48d08-108">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="48d08-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="48d08-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48d08-109">Property</span></span> | <span data-ttu-id="48d08-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48d08-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48d08-111">wmpfss</span><span class="sxs-lookup"><span data-stu-id="48d08-111">wmpfss</span></span>   | <span data-ttu-id="48d08-112">Valore di enumerazione WMPLib. WMPFolderScanStateThe che indica il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="48d08-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48d08-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48d08-113">Requirements</span></span>



| <span data-ttu-id="48d08-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="48d08-114">Requirement</span></span> | <span data-ttu-id="48d08-115">Valore</span><span class="sxs-lookup"><span data-stu-id="48d08-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d08-116">Versione</span><span class="sxs-lookup"><span data-stu-id="48d08-116">Version</span></span><br/>   | <span data-ttu-id="48d08-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="48d08-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="48d08-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="48d08-118">Namespace</span></span><br/> | <span data-ttu-id="48d08-119">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="48d08-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="48d08-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="48d08-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="48d08-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="48d08-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d08-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48d08-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d08-123">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="48d08-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48d08-124">**WMPFolderScanState**</span><span class="sxs-lookup"><span data-stu-id="48d08-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





