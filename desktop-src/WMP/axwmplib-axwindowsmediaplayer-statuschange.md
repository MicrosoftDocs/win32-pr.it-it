---
title: Evento StatusChange dell'oggetto AxWindowsMediaPlayer
description: L'evento StatusChange si verifica quando cambia il valore della proprietà Status. | Evento StatusChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 5295fccb-7be0-46d3-85ba-b481e575d393
keywords:
- Evento StatusChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- StatusChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3ef3224afadb1f98a3067913a8beb095d4e46e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328302"
---
# <a name="statuschange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="350db-105">Evento StatusChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="350db-105">StatusChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="350db-106">L'evento **StatusChange** si verifica quando cambia il valore della proprietà **status** .</span><span class="sxs-lookup"><span data-stu-id="350db-106">The **StatusChange** event occurs when the **status** property changes value.</span></span>

``` syntax
[C#]
private void player_StatusChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_StatusChange(
  sender As Object,
  e As System.EventArgs
) Handles player.StatusChange
```

## <a name="event-data"></a><span data-ttu-id="350db-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="350db-107">Event Data</span></span>

<span data-ttu-id="350db-108">Questo evento non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="350db-108">This event does not contain data.</span></span>

## <a name="requirements"></a><span data-ttu-id="350db-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="350db-109">Requirements</span></span>



| <span data-ttu-id="350db-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="350db-110">Requirement</span></span> | <span data-ttu-id="350db-111">Valore</span><span class="sxs-lookup"><span data-stu-id="350db-111">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="350db-112">Versione</span><span class="sxs-lookup"><span data-stu-id="350db-112">Version</span></span><br/>   | <span data-ttu-id="350db-113">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="350db-113">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="350db-114">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="350db-114">Namespace</span></span><br/> | <span data-ttu-id="350db-115">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="350db-115">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="350db-116">Assembly</span><span class="sxs-lookup"><span data-stu-id="350db-116">Assembly</span></span><br/>  | <dl> <span data-ttu-id="350db-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="350db-117"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="350db-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="350db-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="350db-119">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="350db-119">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="350db-120">**AxWindowsMediaPlayer. Status (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="350db-120">**AxWindowsMediaPlayer.status (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)
</dt> </dl>

 

 





