---
description: Il metodo CreateInstance crea una nuova istanza di questo oggetto.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Metodo CSystemClock. CreateInstance (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333712"
---
# <a name="csystemclockcreateinstance-method"></a><span data-ttu-id="cc3d4-103">Metodo CSystemClock. CreateInstance</span><span class="sxs-lookup"><span data-stu-id="cc3d4-103">CSystemClock.CreateInstance method</span></span>

<span data-ttu-id="cc3d4-104">Il `CreateInstance` metodo crea una nuova istanza di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc3d4-104">The `CreateInstance` method creates a new instance of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3d4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc3d4-105">Syntax</span></span>


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="cc3d4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3d4-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="cc3d4-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="cc3d4-108">Puntatore all'interfaccia **IUnknown** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="cc3d4-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="cc3d4-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="cc3d4-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cc3d4-110">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="cc3d4-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3d4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc3d4-111">Return value</span></span>

<span data-ttu-id="cc3d4-112">Restituisce un puntatore a una nuova istanza di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc3d4-112">Returns a pointer to a new instance of this object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc3d4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc3d4-113">Remarks</span></span>

<span data-ttu-id="cc3d4-114">Il class factory chiama questo metodo per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc3d4-114">The class factory calls this method to create the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3d4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc3d4-115">Requirements</span></span>



| <span data-ttu-id="cc3d4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc3d4-116">Requirement</span></span> | <span data-ttu-id="cc3d4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cc3d4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3d4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc3d4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc3d4-119"><dt>Sysclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc3d4-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc3d4-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc3d4-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc3d4-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cc3d4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




