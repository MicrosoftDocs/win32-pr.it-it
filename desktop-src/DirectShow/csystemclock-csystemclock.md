---
description: 'Costruttore CSystemClock.CSystemClock : metodo costruttore.'
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: Costruttore CSystemClock.CSystemClock (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095199"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="f317c-103">Costruttore CSystemClock.CSystemClock</span><span class="sxs-lookup"><span data-stu-id="f317c-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="f317c-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="f317c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f317c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f317c-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f317c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f317c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f317c-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="f317c-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f317c-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f317c-108">String containing the debug name of the object.</span></span> <span data-ttu-id="f317c-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="f317c-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f317c-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="f317c-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f317c-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f317c-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="f317c-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="f317c-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f317c-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f317c-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f317c-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="f317c-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f317c-115">Puntatore al **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f317c-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="f317c-116">Se si verifica un errore, il metodo restituisce un codice di errore in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f317c-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f317c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f317c-117">Requirements</span></span>



| <span data-ttu-id="f317c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f317c-118">Requirement</span></span> | <span data-ttu-id="f317c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f317c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f317c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f317c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f317c-121"><dt>Sysclock.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f317c-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f317c-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f317c-122">Library</span></span><br/> | <dl> <span data-ttu-id="f317c-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f317c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




