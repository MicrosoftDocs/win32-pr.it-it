---
description: Carica i dati del filtro da un flusso specificato.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Metodo CPersistStream. Load (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328927"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="d19f9-103">Metodo CPersistStream. Load</span><span class="sxs-lookup"><span data-stu-id="d19f9-103">CPersistStream.Load method</span></span>

<span data-ttu-id="d19f9-104">Carica i dati del filtro da un flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="d19f9-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d19f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d19f9-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="d19f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d19f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19f9-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="d19f9-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="d19f9-108">Puntatore al flusso da cui caricare.</span><span class="sxs-lookup"><span data-stu-id="d19f9-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19f9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d19f9-109">Return value</span></span>

<span data-ttu-id="d19f9-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d19f9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d19f9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d19f9-111">Remarks</span></span>

<span data-ttu-id="d19f9-112">Questa funzione membro implementa il metodo **IPersistStream:: Load** .</span><span class="sxs-lookup"><span data-stu-id="d19f9-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d19f9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d19f9-113">Requirements</span></span>



| <span data-ttu-id="d19f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d19f9-114">Requirement</span></span> | <span data-ttu-id="d19f9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d19f9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d19f9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d19f9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d19f9-117"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d19f9-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d19f9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="d19f9-118">Library</span></span><br/> | <dl> <span data-ttu-id="d19f9-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d19f9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d19f9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d19f9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19f9-121">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="d19f9-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




