---
description: Modifica il flag Dirty per il flusso corrente.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Metodo CPersistStream. IsDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328922"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="bd24e-103">Metodo CPersistStream. IsDirty</span><span class="sxs-lookup"><span data-stu-id="bd24e-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="bd24e-104">Modifica il flag Dirty per il flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="bd24e-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd24e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd24e-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="bd24e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd24e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd24e-107">*fDirty*</span><span class="sxs-lookup"><span data-stu-id="bd24e-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="bd24e-108">Nuovo flag Dirty per questo flusso.</span><span class="sxs-lookup"><span data-stu-id="bd24e-108">New dirty flag for this stream.</span></span> <span data-ttu-id="bd24e-109">**True** indica che i dati non sono stati salvati.</span><span class="sxs-lookup"><span data-stu-id="bd24e-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd24e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd24e-110">Return value</span></span>

<span data-ttu-id="bd24e-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd24e-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd24e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd24e-112">Requirements</span></span>



| <span data-ttu-id="bd24e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd24e-113">Requirement</span></span> | <span data-ttu-id="bd24e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bd24e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd24e-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd24e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bd24e-116"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd24e-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bd24e-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd24e-117">Library</span></span><br/> | <dl> <span data-ttu-id="bd24e-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bd24e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd24e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd24e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd24e-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="bd24e-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




