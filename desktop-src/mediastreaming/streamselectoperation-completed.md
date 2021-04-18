---
title: Proprietà StreamSelectOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da SelectBestStreamAsync.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia StreamSelectOperation
- API di streaming multimediale dell'interfaccia StreamSelectOperation, proprietà Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299667"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="260a9-106">Proprietà StreamSelectOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="260a9-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="260a9-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="260a9-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="260a9-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="260a9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="260a9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="260a9-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="260a9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="260a9-110">Property value</span></span>

<span data-ttu-id="260a9-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="260a9-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="260a9-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="260a9-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260a9-113">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="260a9-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 