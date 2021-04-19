---
description: Stato di blocco.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Membro CDynamicOutputPin:: m_BlockState (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333323"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="aedac-103">Membro BlockState di CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="aedac-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="aedac-104">Stato di blocco.</span><span class="sxs-lookup"><span data-stu-id="aedac-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="aedac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aedac-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="aedac-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="aedac-106">Remarks</span></span>

<span data-ttu-id="aedac-107">Sono definiti gli Stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="aedac-107">The following states are defined:</span></span>

-   <span data-ttu-id="aedac-108">NON \_ bloccato</span><span class="sxs-lookup"><span data-stu-id="aedac-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="aedac-109">PENDING</span><span class="sxs-lookup"><span data-stu-id="aedac-109">PENDING</span></span>
-   <span data-ttu-id="aedac-110">BLOCCATO</span><span class="sxs-lookup"><span data-stu-id="aedac-110">BLOCKED</span></span>

<span data-ttu-id="aedac-111">Prima di accedere a questa variabile, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.</span><span class="sxs-lookup"><span data-stu-id="aedac-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="aedac-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aedac-112">Requirements</span></span>



| <span data-ttu-id="aedac-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aedac-113">Requirement</span></span> | <span data-ttu-id="aedac-114">Valore</span><span class="sxs-lookup"><span data-stu-id="aedac-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aedac-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aedac-115">Header</span></span><br/>  | <dl> <span data-ttu-id="aedac-116"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aedac-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aedac-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="aedac-117">Library</span></span><br/> | <dl> <span data-ttu-id="aedac-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="aedac-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aedac-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aedac-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aedac-120">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="aedac-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




