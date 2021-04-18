---
description: Il metodo seformatt Inizializza il blocco di formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Metodo CMediaType. Formatter (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329532"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="b61cf-103">Metodo CMediaType. seformatt</span><span class="sxs-lookup"><span data-stu-id="b61cf-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="b61cf-104">Il `SetFormat` metodo inizializza il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="b61cf-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b61cf-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="b61cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b61cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b61cf-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="b61cf-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="b61cf-108">Puntatore a un blocco di memoria che contiene il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="b61cf-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="b61cf-109">*length*</span><span class="sxs-lookup"><span data-stu-id="b61cf-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="b61cf-110">Lunghezza del blocco di formato, in byte.</span><span class="sxs-lookup"><span data-stu-id="b61cf-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b61cf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b61cf-111">Return value</span></span>

<span data-ttu-id="b61cf-112">Restituisce **true** se ha esito positivo o **false** se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="b61cf-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b61cf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b61cf-113">Remarks</span></span>

<span data-ttu-id="b61cf-114">Questo metodo alloca memoria per il blocco di formato e copia il buffer specificato da *pFormat* nel nuovo blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="b61cf-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="b61cf-115">Se il tipo di supporto contiene già un blocco di formato, viene rilasciato quello precedente.</span><span class="sxs-lookup"><span data-stu-id="b61cf-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="b61cf-116">Il metodo imposta inoltre il membro **cbFormat** della struttura **del \_ \_ tipo di supporto am** .</span><span class="sxs-lookup"><span data-stu-id="b61cf-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="b61cf-117">Per impostare il tipo di formato, chiamare il metodo [**CMediaType:: SetFormatType**](cmediatype-setformattype.md) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b61cf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b61cf-118">Requirements</span></span>



| <span data-ttu-id="b61cf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b61cf-119">Requirement</span></span> | <span data-ttu-id="b61cf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b61cf-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b61cf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b61cf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b61cf-122"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b61cf-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b61cf-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b61cf-123">Library</span></span><br/> | <dl> <span data-ttu-id="b61cf-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b61cf-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61cf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b61cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61cf-126">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="b61cf-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




