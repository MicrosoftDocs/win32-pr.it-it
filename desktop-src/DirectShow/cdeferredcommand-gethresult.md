---
description: Il Metodo GetHRESULT Recupera il valore HRESULT dal comando richiamato.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Metodo CDeferredCommand. GetHRESULT (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333475"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="6ab17-103">CDeferredCommand. GetHRESULT, metodo</span><span class="sxs-lookup"><span data-stu-id="6ab17-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="6ab17-104">Il `GetHResult` metodo recupera il valore **HRESULT** dal comando richiamato.</span><span class="sxs-lookup"><span data-stu-id="6ab17-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab17-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ab17-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="6ab17-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ab17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab17-107">*phrResult*</span><span class="sxs-lookup"><span data-stu-id="6ab17-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab17-108">Puntatore al valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ab17-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab17-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ab17-109">Return value</span></span>

<span data-ttu-id="6ab17-110">Restituisce E \_ Interrompi se **m \_ pQueue** è **null**.</span><span class="sxs-lookup"><span data-stu-id="6ab17-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="6ab17-111">In caso contrario, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ab17-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab17-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ab17-112">Remarks</span></span>

<span data-ttu-id="6ab17-113">Questa funzione membro implementa il metodo [**IDeferredCommand:: GetHRESULT**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .</span><span class="sxs-lookup"><span data-stu-id="6ab17-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab17-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ab17-114">Requirements</span></span>



| <span data-ttu-id="6ab17-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab17-115">Requirement</span></span> | <span data-ttu-id="6ab17-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6ab17-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab17-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ab17-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6ab17-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab17-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ab17-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ab17-119">Library</span></span><br/> | <dl> <span data-ttu-id="6ab17-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab17-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab17-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ab17-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab17-122">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="6ab17-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




