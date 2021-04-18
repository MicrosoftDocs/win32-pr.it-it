---
description: Verifica se un puntatore è NULL. Se il puntatore è NULL, la funzione o il metodo in cui viene visualizzata la macro restituisce il valore specificato.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro CheckPoint (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329781"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="00c9e-104">CheckPoint (macro)</span><span class="sxs-lookup"><span data-stu-id="00c9e-104">CheckPointer macro</span></span>

<span data-ttu-id="00c9e-105">Verifica se un puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="00c9e-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="00c9e-106">Se il puntatore è **null**, la funzione o il metodo in cui viene visualizzata la macro restituisce il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="00c9e-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c9e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00c9e-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="00c9e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="00c9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c9e-109">*p*</span><span class="sxs-lookup"><span data-stu-id="00c9e-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="00c9e-110">Puntatore da verificare.</span><span class="sxs-lookup"><span data-stu-id="00c9e-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="00c9e-111">*RET*</span><span class="sxs-lookup"><span data-stu-id="00c9e-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="00c9e-112">Valore restituito dalla funzione o dal metodo se *p* è **null**.</span><span class="sxs-lookup"><span data-stu-id="00c9e-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c9e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00c9e-113">Return value</span></span>

<span data-ttu-id="00c9e-114">La funzione circostante restituisce *ret* se *p* è **null**.</span><span class="sxs-lookup"><span data-stu-id="00c9e-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="00c9e-115">In caso contrario, la macro non determina la restituzione della funzione circostante.</span><span class="sxs-lookup"><span data-stu-id="00c9e-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="00c9e-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="00c9e-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="00c9e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00c9e-117">Requirements</span></span>



| <span data-ttu-id="00c9e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="00c9e-118">Requirement</span></span> | <span data-ttu-id="00c9e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="00c9e-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c9e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00c9e-120">Header</span></span><br/> | <dl> <span data-ttu-id="00c9e-121"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00c9e-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00c9e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00c9e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c9e-123">Macro di convalida del puntatore</span><span class="sxs-lookup"><span data-stu-id="00c9e-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




