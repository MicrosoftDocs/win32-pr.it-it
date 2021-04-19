---
description: Numero di thread di streaming che usano questo pin.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Membro CDynamicOutputPin:: m_dwNumOutstandingOutputPinUsers (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333445"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="d6d7c-103">Membro dwNumOutstandingOutputPinUsers di CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="d6d7c-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="d6d7c-104">Numero di thread di streaming che usano questo pin.</span><span class="sxs-lookup"><span data-stu-id="d6d7c-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d7c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6d7c-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="d6d7c-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d6d7c-106">Remarks</span></span>

<span data-ttu-id="d6d7c-107">Il metodo [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa questa variabile e il metodo [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) decrementa la variabile.</span><span class="sxs-lookup"><span data-stu-id="d6d7c-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="d6d7c-108">Quando il valore è maggiore di zero, un thread usa questo pin per trasmettere i dati o per modificare il tipo di connessione.</span><span class="sxs-lookup"><span data-stu-id="d6d7c-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="d6d7c-109">Il PIN non può essere bloccato in questo caso.</span><span class="sxs-lookup"><span data-stu-id="d6d7c-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="d6d7c-110">Prima di accedere a questa variabile, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.</span><span class="sxs-lookup"><span data-stu-id="d6d7c-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d7c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6d7c-111">Requirements</span></span>



| <span data-ttu-id="d6d7c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6d7c-112">Requirement</span></span> | <span data-ttu-id="d6d7c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d6d7c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d7c-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6d7c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d6d7c-115"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6d7c-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6d7c-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="d6d7c-116">Library</span></span><br/> | <dl> <span data-ttu-id="d6d7c-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d6d7c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d7c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6d7c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d7c-119">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="d6d7c-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="d6d7c-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="d6d7c-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




