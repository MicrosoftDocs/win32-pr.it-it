---
title: Proprietà GetPositionInformationOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da GetPositionInformationAsync.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia GetPositionInformationOperation
- API di streaming multimediale dell'interfaccia GetPositionInformationOperation, proprietà Completed
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398992"
---
# <a name="getpositioninformationoperationcompleted-property"></a><span data-ttu-id="d2a84-106">Proprietà GetPositionInformationOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="d2a84-106">GetPositionInformationOperation.Completed property</span></span>

<span data-ttu-id="d2a84-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) .</span><span class="sxs-lookup"><span data-stu-id="d2a84-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) is completed.</span></span>

<span data-ttu-id="d2a84-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d2a84-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a84-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2a84-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="d2a84-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d2a84-110">Property value</span></span>

<span data-ttu-id="d2a84-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="d2a84-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2a84-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a84-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a84-113">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="d2a84-113">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

 