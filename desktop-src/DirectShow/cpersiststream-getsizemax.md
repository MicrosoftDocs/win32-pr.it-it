---
description: Recupera la dimensione massima in byte necessaria per il flusso corrente, incluso il numero di versione.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Metodo CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328931"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="98488-103">CPersistStream. GetSizeMax, metodo</span><span class="sxs-lookup"><span data-stu-id="98488-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="98488-104">Recupera la dimensione massima in byte necessaria per il flusso corrente, incluso il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="98488-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="98488-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98488-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="98488-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98488-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98488-107">*pcbSize*</span><span class="sxs-lookup"><span data-stu-id="98488-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="98488-108">Puntatore alla dimensione in byte necessaria per salvare il flusso, incluso il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="98488-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98488-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98488-109">Return value</span></span>

<span data-ttu-id="98488-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98488-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98488-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="98488-111">Remarks</span></span>

<span data-ttu-id="98488-112">Questa funzione membro implementa il metodo **IPersistStream:: GetSizeMax** .</span><span class="sxs-lookup"><span data-stu-id="98488-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="98488-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98488-113">Requirements</span></span>



| <span data-ttu-id="98488-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98488-114">Requirement</span></span> | <span data-ttu-id="98488-115">Valore</span><span class="sxs-lookup"><span data-stu-id="98488-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98488-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98488-116">Header</span></span><br/>  | <dl> <span data-ttu-id="98488-117"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98488-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98488-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="98488-118">Library</span></span><br/> | <dl> <span data-ttu-id="98488-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="98488-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98488-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98488-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98488-121">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="98488-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




