---
title: Proprietà GetTransportInformationOperation completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da GetTransportInformationAsync.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia GetTransportInformationOperation
- API di streaming multimediale dell'interfaccia GetTransportInformationOperation, proprietà Completed
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299689"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="486bb-106">Proprietà GetTransportInformationOperation:: Completed</span><span class="sxs-lookup"><span data-stu-id="486bb-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="486bb-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) .</span><span class="sxs-lookup"><span data-stu-id="486bb-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="486bb-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="486bb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="486bb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="486bb-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="486bb-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="486bb-110">Property value</span></span>

<span data-ttu-id="486bb-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="486bb-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="486bb-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="486bb-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="486bb-113">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="486bb-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 