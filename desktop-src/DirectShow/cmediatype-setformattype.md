---
description: Il metodo SetFormatType specifica il tipo di formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Metodo CMediaType. SetFormatType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330224"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="49a83-103">CMediaType. SetFormatType, metodo</span><span class="sxs-lookup"><span data-stu-id="49a83-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="49a83-104">Il metodo SetFormatType '' specifica il tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="49a83-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49a83-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="49a83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49a83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a83-107">*pformattype*</span><span class="sxs-lookup"><span data-stu-id="49a83-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="49a83-108">Puntatore a un **GUID** che specifica il tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="49a83-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a83-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49a83-109">Return value</span></span>

<span data-ttu-id="49a83-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="49a83-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a83-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="49a83-111">Remarks</span></span>

<span data-ttu-id="49a83-112">Questo metodo imposta il membro **formatType** .</span><span class="sxs-lookup"><span data-stu-id="49a83-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="49a83-113">Il tipo di formato definisce il layout del blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="49a83-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="49a83-114">Se ad esempio il formato del tipo è \_ videoinfo, il blocco di formato deve contenere una struttura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="49a83-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="49a83-115">Per impostare il blocco di formato, chiamare il metodo [**CMediaType:: Seformatt**](cmediatype-setformat.md) .</span><span class="sxs-lookup"><span data-stu-id="49a83-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="49a83-116">Il chiamante è responsabile di assicurarsi che il blocco di formato corrisponda al tipo di formato.</span><span class="sxs-lookup"><span data-stu-id="49a83-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a83-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49a83-117">Requirements</span></span>



| <span data-ttu-id="49a83-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49a83-118">Requirement</span></span> | <span data-ttu-id="49a83-119">Valore</span><span class="sxs-lookup"><span data-stu-id="49a83-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a83-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49a83-120">Header</span></span><br/>  | <dl> <span data-ttu-id="49a83-121"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49a83-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="49a83-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="49a83-122">Library</span></span><br/> | <dl> <span data-ttu-id="49a83-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49a83-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49a83-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49a83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a83-125">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="49a83-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
