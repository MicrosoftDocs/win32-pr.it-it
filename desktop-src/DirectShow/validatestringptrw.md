---
description: Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa di caratteri wide. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Macro ValidateStringPtrW (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333289"
---
# <a name="validatestringptrw-macro"></a><span data-ttu-id="d46c1-104">ValidateStringPtrW (macro)</span><span class="sxs-lookup"><span data-stu-id="d46c1-104">ValidateStringPtrW macro</span></span>

<span data-ttu-id="d46c1-105">Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="d46c1-105">Verifies that the calling process has read access to a wide-character string.</span></span> <span data-ttu-id="d46c1-106">In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="d46c1-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="d46c1-107">Questa macro è deprecata.</span><span class="sxs-lookup"><span data-stu-id="d46c1-107">This macro is deprecated.</span></span> <span data-ttu-id="d46c1-108">Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="d46c1-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d46c1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d46c1-109">Syntax</span></span>


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="d46c1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d46c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d46c1-111">*p*</span><span class="sxs-lookup"><span data-stu-id="d46c1-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="d46c1-112">Puntatore a una stringa di caratteri wide con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="d46c1-112">Pointer to a NULL-terminated wide-character string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d46c1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d46c1-113">Return value</span></span>

<span data-ttu-id="d46c1-114">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d46c1-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d46c1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d46c1-115">Remarks</span></span>

<span data-ttu-id="d46c1-116">Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d46c1-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="d46c1-117">Questa macro può avere un costo significativo per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d46c1-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="d46c1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d46c1-118">Requirements</span></span>



| <span data-ttu-id="d46c1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d46c1-119">Requirement</span></span> | <span data-ttu-id="d46c1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d46c1-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46c1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d46c1-121">Header</span></span><br/> | <dl> <span data-ttu-id="d46c1-122"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d46c1-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d46c1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d46c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46c1-124">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="d46c1-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




