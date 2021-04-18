---
title: Proprietà PlaybackOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da uno dei metodi di riproduzione MediaRenderer.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia PlaybackOperation
- API di streaming multimediale dell'interfaccia PlaybackOperation, proprietà Completed
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299047"
---
# <a name="playbackoperationcompleted-property"></a><span data-ttu-id="1f53f-106">Proprietà PlaybackOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="1f53f-106">PlaybackOperation.Completed property</span></span>

<span data-ttu-id="1f53f-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da uno dei metodi di riproduzione [**MediaRenderer**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="1f53f-107">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span>

<span data-ttu-id="1f53f-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1f53f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f53f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f53f-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="1f53f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1f53f-110">Property value</span></span>

<span data-ttu-id="1f53f-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="1f53f-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f53f-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f53f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f53f-113">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="1f53f-113">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 




