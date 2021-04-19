---
description: La funzione GetBitmapSubtype restituisce il GUID del sottotipo di supporto per la bitmap specificata.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Funzione GetBitmapSubtype (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328244"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="7e611-103">GetBitmapSubtype (funzione)</span><span class="sxs-lookup"><span data-stu-id="7e611-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="7e611-104">La `GetBitmapSubtype` funzione restituisce il **GUID** del sottotipo di supporto per la bitmap specificata.</span><span class="sxs-lookup"><span data-stu-id="7e611-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e611-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e611-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="7e611-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e611-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="7e611-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="7e611-108">Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="7e611-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e611-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e611-109">Return value</span></span>

<span data-ttu-id="7e611-110">Restituisce il **GUID** del sottotipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="7e611-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e611-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e611-111">Remarks</span></span>

<span data-ttu-id="7e611-112">Per i tipi RGB non compressi, questa funzione esegue il mapping del campo **biBitCount** al sottotipo.</span><span class="sxs-lookup"><span data-stu-id="7e611-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="7e611-113">Per i tipi di video compressi, questa funzione usa la classe [**FOURCCMap**](fourccmap.md) per eseguire il mapping del campo di **biCompression** al sottotipo.</span><span class="sxs-lookup"><span data-stu-id="7e611-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="7e611-114">Se la funzione non può corrispondere al formato a un sottotipo, il valore restituito è il GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="7e611-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e611-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e611-115">Requirements</span></span>



| <span data-ttu-id="7e611-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e611-116">Requirement</span></span> | <span data-ttu-id="7e611-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7e611-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e611-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e611-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7e611-119"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e611-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7e611-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="7e611-120">Library</span></span><br/> | <dl> <span data-ttu-id="7e611-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7e611-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e611-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e611-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e611-123">Funzioni video e immagine</span><span class="sxs-lookup"><span data-stu-id="7e611-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




