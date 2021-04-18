---
description: Il metodo CreateDIB crea una bitmap (DIB) indipendente dal dispositivo GDI. Il valore DIB viene allocato in un blocco mempory condiviso, che elimina un'operazione di copia quando il filtro proprietario Blits l'immagine.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Metodo CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329772"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="f5234-104">CImageAllocator. CreateDIB, metodo</span><span class="sxs-lookup"><span data-stu-id="f5234-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="f5234-105">Il `CreateDIB` metodo crea una bitmap (DIB) indipendente dal dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="f5234-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="f5234-106">Il valore DIB viene allocato in un blocco mempory condiviso, che elimina un'operazione di copia quando il filtro proprietario Blits l'immagine.</span><span class="sxs-lookup"><span data-stu-id="f5234-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5234-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5234-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="f5234-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5234-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5234-109">*Dimensioni*</span><span class="sxs-lookup"><span data-stu-id="f5234-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f5234-110">Dimensione della bitmap.</span><span class="sxs-lookup"><span data-stu-id="f5234-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f5234-111">*DibData* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="f5234-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f5234-112">Riferimento a una struttura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f5234-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="f5234-113">Il metodo compila questa struttura con le informazioni sulla DIB.</span><span class="sxs-lookup"><span data-stu-id="f5234-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5234-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5234-114">Return value</span></span>

<span data-ttu-id="f5234-115">Restituisce \_ OK se l'esito è positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f5234-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5234-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5234-116">Requirements</span></span>



| <span data-ttu-id="f5234-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5234-117">Requirement</span></span> | <span data-ttu-id="f5234-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5234-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5234-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5234-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f5234-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5234-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5234-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5234-121">Library</span></span><br/> | <dl> <span data-ttu-id="f5234-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f5234-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5234-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5234-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5234-124">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="f5234-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="f5234-125">**CImageAllocator:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="f5234-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




