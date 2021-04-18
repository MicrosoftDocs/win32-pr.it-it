---
description: Il metodo Unadvise rimuove una richiesta di notifica.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Metodo CAMSchedule. Unadvise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329561"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="dd9d1-103">Metodo CAMSchedule. Unadvise</span><span class="sxs-lookup"><span data-stu-id="dd9d1-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="dd9d1-104">Il `Unadvise` metodo rimuove una richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="dd9d1-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd9d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd9d1-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="dd9d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd9d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd9d1-107">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="dd9d1-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="dd9d1-108">Identificatore della richiesta di notifica, restituito dal metodo [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="dd9d1-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd9d1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd9d1-109">Return value</span></span>

<span data-ttu-id="dd9d1-110">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dd9d1-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="dd9d1-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dd9d1-111">Return code</span></span>                                                                             | <span data-ttu-id="dd9d1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd9d1-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="dd9d1-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="dd9d1-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="dd9d1-114">Non trovato</span><span class="sxs-lookup"><span data-stu-id="dd9d1-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="dd9d1-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd9d1-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="dd9d1-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="dd9d1-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="dd9d1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd9d1-117">Requirements</span></span>



| <span data-ttu-id="dd9d1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd9d1-118">Requirement</span></span> | <span data-ttu-id="dd9d1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dd9d1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9d1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd9d1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dd9d1-121"><dt>Dsschedule. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd9d1-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="dd9d1-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd9d1-122">Library</span></span><br/> | <dl> <span data-ttu-id="dd9d1-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dd9d1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd9d1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd9d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd9d1-125">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="dd9d1-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




