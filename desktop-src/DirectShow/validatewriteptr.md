---
description: Verifica che il processo chiamante disponga dell'accesso in scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: Macro ValidateWritePtr (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e7c955f31cf9e0bf1050c52b680dfc9b32741bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333287"
---
# <a name="validatewriteptr-macro"></a><span data-ttu-id="05cfd-104">ValidateWritePtr (macro)</span><span class="sxs-lookup"><span data-stu-id="05cfd-104">ValidateWritePtr macro</span></span>

<span data-ttu-id="05cfd-105">Verifica che il processo chiamante disponga dell'accesso in scrittura a un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="05cfd-105">Verifies that the calling process has write access to a memory block.</span></span> <span data-ttu-id="05cfd-106">In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="05cfd-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="05cfd-107">Questa macro è deprecata.</span><span class="sxs-lookup"><span data-stu-id="05cfd-107">This macro is deprecated.</span></span> <span data-ttu-id="05cfd-108">Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="05cfd-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="05cfd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05cfd-109">Syntax</span></span>


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="05cfd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="05cfd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05cfd-111">*p*</span><span class="sxs-lookup"><span data-stu-id="05cfd-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="05cfd-112">Puntatore a un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="05cfd-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="05cfd-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="05cfd-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="05cfd-114">Dimensioni in byte del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="05cfd-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05cfd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05cfd-115">Return value</span></span>

<span data-ttu-id="05cfd-116">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="05cfd-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05cfd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="05cfd-117">Remarks</span></span>

<span data-ttu-id="05cfd-118">Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05cfd-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="05cfd-119">Questa macro può avere un costo significativo per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="05cfd-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="05cfd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05cfd-120">Requirements</span></span>



| <span data-ttu-id="05cfd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05cfd-121">Requirement</span></span> | <span data-ttu-id="05cfd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="05cfd-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05cfd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05cfd-123">Header</span></span><br/> | <dl> <span data-ttu-id="05cfd-124"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05cfd-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05cfd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05cfd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05cfd-126">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="05cfd-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




