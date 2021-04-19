---
description: Il metodo Remove rimuove l'oggetto CDeferredCommand dalla coda.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Metodo CCmdQueue. Remove (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332767"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="5c56e-103">Metodo CCmdQueue. Remove</span><span class="sxs-lookup"><span data-stu-id="5c56e-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="5c56e-104">Il `Remove` metodo rimuove l'oggetto [**CDeferredCommand**](cdeferredcommand.md) dalla coda.</span><span class="sxs-lookup"><span data-stu-id="5c56e-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c56e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c56e-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="5c56e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c56e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c56e-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="5c56e-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="5c56e-108">Puntatore all'oggetto **CDeferredCommand** da rimuovere dalla coda.</span><span class="sxs-lookup"><span data-stu-id="5c56e-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c56e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c56e-109">Return value</span></span>

<span data-ttu-id="5c56e-110">Restituisce VFW \_ E \_ non \_ trovato se l'oggetto non viene trovato nella coda.</span><span class="sxs-lookup"><span data-stu-id="5c56e-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="5c56e-111">In caso contrario, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c56e-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c56e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c56e-112">Requirements</span></span>



| <span data-ttu-id="5c56e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c56e-113">Requirement</span></span> | <span data-ttu-id="5c56e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5c56e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c56e-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c56e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5c56e-116"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c56e-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5c56e-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c56e-117">Library</span></span><br/> | <dl> <span data-ttu-id="5c56e-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5c56e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c56e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c56e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c56e-120">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="5c56e-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




