---
title: Proprietà CreateMediaRendererOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da CreateMediaRendererAsync o CreateMediaRendererFromBasicDeviceAsync.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia CreateMediaRendererOperation
- API di streaming multimediale dell'interfaccia CreateMediaRendererOperation, proprietà Completed
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718418"
---
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="6ca78-106">Proprietà CreateMediaRendererOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="6ca78-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="6ca78-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) o [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .</span><span class="sxs-lookup"><span data-stu-id="6ca78-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="6ca78-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6ca78-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca78-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ca78-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="6ca78-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6ca78-110">Property value</span></span>

<span data-ttu-id="6ca78-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="6ca78-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ca78-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ca78-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca78-113">**CreateMediaRendererOperation**</span><span class="sxs-lookup"><span data-stu-id="6ca78-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




