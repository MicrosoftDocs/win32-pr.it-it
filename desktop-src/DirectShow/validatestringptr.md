---
description: Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333291"
---
# <a name="validatestringptr-macro"></a><span data-ttu-id="cd347-104">ValidateStringPtr (macro)</span><span class="sxs-lookup"><span data-stu-id="cd347-104">ValidateStringPtr macro</span></span>

<span data-ttu-id="cd347-105">Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa.</span><span class="sxs-lookup"><span data-stu-id="cd347-105">Verifies that the calling process has read access to a string.</span></span> <span data-ttu-id="cd347-106">In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="cd347-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="cd347-107">Questa macro è deprecata.</span><span class="sxs-lookup"><span data-stu-id="cd347-107">This macro is deprecated.</span></span> <span data-ttu-id="cd347-108">Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="cd347-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cd347-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd347-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="cd347-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd347-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd347-111">*p*</span><span class="sxs-lookup"><span data-stu-id="cd347-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="cd347-112">Puntatore a una stringa **TCHAR** con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="cd347-112">Pointer to a NULL-terminated **TCHAR** string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd347-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd347-113">Return value</span></span>

<span data-ttu-id="cd347-114">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cd347-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd347-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd347-115">Remarks</span></span>

<span data-ttu-id="cd347-116">Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cd347-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="cd347-117">Questa macro può avere un costo significativo per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="cd347-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd347-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd347-118">Requirements</span></span>



| <span data-ttu-id="cd347-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd347-119">Requirement</span></span> | <span data-ttu-id="cd347-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cd347-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd347-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd347-121">Header</span></span><br/> | <dl> <span data-ttu-id="cd347-122"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd347-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd347-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd347-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd347-124">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="cd347-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




