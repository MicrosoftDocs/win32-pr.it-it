---
description: Il metodo seallocator specifica un allocatore per la connessione.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Metodo CTransInPlaceOutputPin. seallocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326169"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a><span data-ttu-id="26981-103">Metodo CTransInPlaceOutputPin. seallocator</span><span class="sxs-lookup"><span data-stu-id="26981-103">CTransInPlaceOutputPin.SetAllocator method</span></span>

<span data-ttu-id="26981-104">Il `SetAllocator` metodo specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="26981-104">The `SetAllocator` method specifies an allocator for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="26981-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26981-105">Syntax</span></span>


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="26981-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26981-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26981-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="26981-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="26981-108">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="26981-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26981-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26981-109">Return value</span></span>

<span data-ttu-id="26981-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="26981-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26981-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="26981-111">Remarks</span></span>

<span data-ttu-id="26981-112">Il pin di output per questo filtro non fornisce mai un allocatore.</span><span class="sxs-lookup"><span data-stu-id="26981-112">The output pin for this filter never provides an allocator.</span></span> <span data-ttu-id="26981-113">Questo metodo specifica l'allocatore per il pin di output.</span><span class="sxs-lookup"><span data-stu-id="26981-113">This method specifies the allocator for the output pin.</span></span> <span data-ttu-id="26981-114">Viene impostato il valore della variabile membro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="26981-114">It sets the value of the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="26981-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26981-115">Requirements</span></span>



| <span data-ttu-id="26981-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="26981-116">Requirement</span></span> | <span data-ttu-id="26981-117">Valore</span><span class="sxs-lookup"><span data-stu-id="26981-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26981-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26981-118">Header</span></span><br/>  | <dl> <span data-ttu-id="26981-119"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26981-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26981-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="26981-120">Library</span></span><br/> | <dl> <span data-ttu-id="26981-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="26981-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26981-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26981-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26981-123">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="26981-123">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




