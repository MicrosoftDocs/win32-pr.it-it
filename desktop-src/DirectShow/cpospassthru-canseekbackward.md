---
description: "Il metodo CanSeekBackward determina se è possibile cercare il flusso all'indietro. Questo metodo implementa il metodo IMediaPosition:: CanSeekBackward."
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Metodo CPosPassThru. CanSeekBackward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325659"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="7d7a4-104">CPosPassThru. CanSeekBackward, metodo</span><span class="sxs-lookup"><span data-stu-id="7d7a4-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="7d7a4-105">Il `CanSeekBackward` metodo determina se è possibile cercare il flusso all'indietro.</span><span class="sxs-lookup"><span data-stu-id="7d7a4-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="7d7a4-106">Questo metodo implementa il metodo [**IMediaPosition:: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .</span><span class="sxs-lookup"><span data-stu-id="7d7a4-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7a4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d7a4-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="7d7a4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d7a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d7a4-109">*pCanSeekBackward*</span><span class="sxs-lookup"><span data-stu-id="7d7a4-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="7d7a4-110">Puntatore a una variabile che riceve il valore OATRUE se il filtro può cercare indietro o OAFALSE in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7d7a4-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d7a4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d7a4-111">Return value</span></span>

<span data-ttu-id="7d7a4-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="7d7a4-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d7a4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d7a4-113">Requirements</span></span>



| <span data-ttu-id="7d7a4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d7a4-114">Requirement</span></span> | <span data-ttu-id="7d7a4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7d7a4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7a4-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d7a4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7d7a4-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d7a4-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d7a4-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d7a4-118">Library</span></span><br/> | <dl> <span data-ttu-id="7d7a4-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7d7a4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d7a4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d7a4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7a4-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="7d7a4-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




