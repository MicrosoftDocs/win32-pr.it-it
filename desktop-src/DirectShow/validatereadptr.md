---
description: Verifica che il processo chiamante disponga dell'accesso in lettura a un blocco di memoria. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: Macro ValidateReadPtr (Wxdebug. h)
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
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333297"
---
# <a name="validatereadptr-macro"></a><span data-ttu-id="52bcd-104">ValidateReadPtr (macro)</span><span class="sxs-lookup"><span data-stu-id="52bcd-104">ValidateReadPtr macro</span></span>

<span data-ttu-id="52bcd-105">Verifica che il processo chiamante disponga dell'accesso in lettura a un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="52bcd-105">Verifies that the calling process has read access to a memory block.</span></span> <span data-ttu-id="52bcd-106">In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .</span><span class="sxs-lookup"><span data-stu-id="52bcd-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="52bcd-107">Questa macro è deprecata.</span><span class="sxs-lookup"><span data-stu-id="52bcd-107">This macro is deprecated.</span></span> <span data-ttu-id="52bcd-108">Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="52bcd-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="52bcd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52bcd-109">Syntax</span></span>


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="52bcd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="52bcd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52bcd-111">*p*</span><span class="sxs-lookup"><span data-stu-id="52bcd-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="52bcd-112">Puntatore a un blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="52bcd-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="52bcd-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="52bcd-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="52bcd-114">Dimensioni in byte del blocco di memoria.</span><span class="sxs-lookup"><span data-stu-id="52bcd-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52bcd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52bcd-115">Return value</span></span>

<span data-ttu-id="52bcd-116">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="52bcd-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52bcd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="52bcd-117">Remarks</span></span>

<span data-ttu-id="52bcd-118">Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="52bcd-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="52bcd-119">Questa macro può avere un costo significativo per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="52bcd-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="52bcd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52bcd-120">Requirements</span></span>



| <span data-ttu-id="52bcd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="52bcd-121">Requirement</span></span> | <span data-ttu-id="52bcd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="52bcd-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52bcd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52bcd-123">Header</span></span><br/> | <dl> <span data-ttu-id="52bcd-124"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52bcd-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52bcd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52bcd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bcd-126">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="52bcd-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




