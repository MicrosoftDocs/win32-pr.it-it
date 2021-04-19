---
description: Verifica che il processo chiamante disponga dell'accesso in lettura/scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333292"
---
# <a name="validatereadwriteptr-macro"></a><span data-ttu-id="f7292-104">ValidateReadWritePtr (macro)</span><span class="sxs-lookup"><span data-stu-id="f7292-104">ValidateReadWritePtr macro</span></span>

<span data-ttu-id="f7292-105">Verifica che il processo chiamante disponga dell'accesso in lettura/scrittura a un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="f7292-105">Verifies that the calling process has read/write access to a memory block.</span></span> <span data-ttu-id="f7292-106">In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="f7292-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="f7292-107">Questa macro è deprecata.</span><span class="sxs-lookup"><span data-stu-id="f7292-107">This macro is deprecated.</span></span> <span data-ttu-id="f7292-108">Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f7292-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f7292-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7292-109">Syntax</span></span>


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="f7292-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7292-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7292-111">*p*</span><span class="sxs-lookup"><span data-stu-id="f7292-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="f7292-112">Puntatore a un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="f7292-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="f7292-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="f7292-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="f7292-114">Dimensioni in byte del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="f7292-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7292-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7292-115">Return value</span></span>

<span data-ttu-id="f7292-116">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f7292-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7292-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7292-117">Remarks</span></span>

<span data-ttu-id="f7292-118">Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f7292-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="f7292-119">Questa macro può avere un costo significativo per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f7292-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7292-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7292-120">Requirements</span></span>



| <span data-ttu-id="f7292-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7292-121">Requirement</span></span> | <span data-ttu-id="f7292-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f7292-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7292-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7292-123">Header</span></span><br/> | <dl> <span data-ttu-id="f7292-124"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7292-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7292-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7292-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7292-126">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="f7292-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




