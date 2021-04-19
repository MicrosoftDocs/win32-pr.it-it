---
description: Metodo del costruttore.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Costruttore CPersistStream. CPersistStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328936"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="b8e3b-103">Costruttore CPersistStream. CPersistStream</span><span class="sxs-lookup"><span data-stu-id="b8e3b-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="b8e3b-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="b8e3b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8e3b-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b8e3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e3b-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="b8e3b-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e3b-108">Puntatore all'interfaccia **IUnknown** dell'oggetto delegato.</span><span class="sxs-lookup"><span data-stu-id="b8e3b-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="b8e3b-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="b8e3b-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e3b-110">Puntatore al valore restituito COM generale.</span><span class="sxs-lookup"><span data-stu-id="b8e3b-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="b8e3b-111">Questo valore viene modificato solo se questa funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b8e3b-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8e3b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8e3b-112">Requirements</span></span>



| <span data-ttu-id="b8e3b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e3b-113">Requirement</span></span> | <span data-ttu-id="b8e3b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b8e3b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e3b-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8e3b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b8e3b-116"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8e3b-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8e3b-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8e3b-117">Library</span></span><br/> | <dl> <span data-ttu-id="b8e3b-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b8e3b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e3b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e3b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e3b-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="b8e3b-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




