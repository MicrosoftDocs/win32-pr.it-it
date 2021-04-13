---
title: Proprietà GetStreamPropertiesOperation. Completed
description: Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da GetStreamPropertiesAsync.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- API di streaming multimediale delle proprietà completate
- API di streaming multimediale delle proprietà completa, interfaccia GetStreamPropertiesOperation
- API di streaming multimediale dell'interfaccia GetStreamPropertiesOperation, proprietà Completed
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398924"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="82a84-106">Proprietà GetStreamPropertiesOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="82a84-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="82a84-107">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="82a84-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="82a84-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="82a84-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a84-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82a84-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="82a84-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="82a84-110">Property value</span></span>

<span data-ttu-id="82a84-111">Gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="82a84-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="82a84-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82a84-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a84-113">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="82a84-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 