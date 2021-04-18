---
description: Il metodo Insert aggiunge un oggetto CDeferredCommand alla coda.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Metodo CCmdQueue. Insert (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324478"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="a09d3-103">CCmdQueue. Insert (metodo)</span><span class="sxs-lookup"><span data-stu-id="a09d3-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="a09d3-104">Il `Insert` metodo aggiunge un oggetto [**CDeferredCommand**](cdeferredcommand.md) alla coda.</span><span class="sxs-lookup"><span data-stu-id="a09d3-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a09d3-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a09d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a09d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09d3-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="a09d3-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="a09d3-108">Puntatore all'oggetto **CDeferredCommand** da aggiungere alla coda.</span><span class="sxs-lookup"><span data-stu-id="a09d3-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09d3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a09d3-109">Return value</span></span>

<span data-ttu-id="a09d3-110">Restituisce \_ OK nell'implementazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a09d3-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a09d3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a09d3-111">Requirements</span></span>



| <span data-ttu-id="a09d3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09d3-112">Requirement</span></span> | <span data-ttu-id="a09d3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a09d3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09d3-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a09d3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a09d3-115"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a09d3-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a09d3-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="a09d3-116">Library</span></span><br/> | <dl> <span data-ttu-id="a09d3-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a09d3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a09d3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a09d3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09d3-119">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="a09d3-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




