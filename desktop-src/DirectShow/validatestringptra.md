---
description: Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa ANSI. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Macro ValidateStringPtrA (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333290"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="a385f-104">ValidateStringPtrA (macro)</span><span class="sxs-lookup"><span data-stu-id="a385f-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="a385f-105">Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="a385f-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="a385f-106">In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="a385f-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="a385f-107">Questa macro è deprecata.</span><span class="sxs-lookup"><span data-stu-id="a385f-107">This macro is deprecated.</span></span> <span data-ttu-id="a385f-108">Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="a385f-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a385f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a385f-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="a385f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a385f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a385f-111">*p*</span><span class="sxs-lookup"><span data-stu-id="a385f-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="a385f-112">Puntatore a una stringa ANSI con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="a385f-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a385f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a385f-113">Return value</span></span>

<span data-ttu-id="a385f-114">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a385f-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a385f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a385f-115">Remarks</span></span>

<span data-ttu-id="a385f-116">Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a385f-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="a385f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a385f-117">Requirements</span></span>



| <span data-ttu-id="a385f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a385f-118">Requirement</span></span> | <span data-ttu-id="a385f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a385f-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a385f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a385f-120">Header</span></span><br/> | <dl> <span data-ttu-id="a385f-121"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a385f-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a385f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a385f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a385f-123">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="a385f-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




