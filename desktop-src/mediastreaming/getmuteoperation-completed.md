---
title: Proprietà GetMuteOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da GetMuteAsync.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia GetMuteOperation
- API di streaming multimediale dell'interfaccia GetMuteOperation, proprietà Completed
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726578"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="54fd3-106">Proprietà GetMuteOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="54fd3-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="54fd3-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) .</span><span class="sxs-lookup"><span data-stu-id="54fd3-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="54fd3-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="54fd3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fd3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54fd3-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="54fd3-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="54fd3-110">Property value</span></span>

<span data-ttu-id="54fd3-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="54fd3-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="54fd3-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54fd3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fd3-113">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="54fd3-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 