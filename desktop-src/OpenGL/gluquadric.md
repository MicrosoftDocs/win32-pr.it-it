---
title: funzione gluQuadricCallback (Glu. h)
description: La funzione gluQuadricCallback definisce un callback per un oggetto quadrica.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- funzione gluQuadricCallback OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518412"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="aa98a-104">gluQuadricCallback (funzione)</span><span class="sxs-lookup"><span data-stu-id="aa98a-104">gluQuadricCallback function</span></span>

<span data-ttu-id="aa98a-105">La funzione **gluQuadricCallback** definisce un callback per un oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="aa98a-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa98a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa98a-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="aa98a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa98a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa98a-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="aa98a-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="aa98a-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="aa98a-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="aa98a-110">*che*</span><span class="sxs-lookup"><span data-stu-id="aa98a-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="aa98a-111">Callback da definire.</span><span class="sxs-lookup"><span data-stu-id="aa98a-111">The callback being defined.</span></span> <span data-ttu-id="aa98a-112">L'unico valore valido è GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="aa98a-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="aa98a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aa98a-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="aa98a-114">Significato</span><span class="sxs-lookup"><span data-stu-id="aa98a-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="aa98a-115"><dt>**\_errore Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="aa98a-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="aa98a-116">La funzione **gluQuadricCallback** viene chiamata quando viene rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="aa98a-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="aa98a-117">Il suo singolo argomento è di tipo **GLEnum** e indica l'errore specifico che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="aa98a-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="aa98a-118">È possibile recuperare le stringhe di caratteri che descrivono questi errori con la chiamata a [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="aa98a-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aa98a-119">*FN*</span><span class="sxs-lookup"><span data-stu-id="aa98a-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="aa98a-120">Funzione da chiamare.</span><span class="sxs-lookup"><span data-stu-id="aa98a-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa98a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa98a-121">Return value</span></span>

<span data-ttu-id="aa98a-122">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="aa98a-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa98a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa98a-123">Remarks</span></span>

<span data-ttu-id="aa98a-124">Usare **gluQuadricCallback** per definire un nuovo callback che verrà usato da un oggetto quadrica.</span><span class="sxs-lookup"><span data-stu-id="aa98a-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="aa98a-125">Se il callback specificato è già definito, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="aa98a-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="aa98a-126">Se *FN* è **null**, qualsiasi callback esistente verrà cancellato.</span><span class="sxs-lookup"><span data-stu-id="aa98a-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa98a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa98a-127">Requirements</span></span>



| <span data-ttu-id="aa98a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa98a-128">Requirement</span></span> | <span data-ttu-id="aa98a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="aa98a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa98a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa98a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa98a-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa98a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aa98a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa98a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa98a-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa98a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa98a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa98a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa98a-135"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa98a-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="aa98a-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa98a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa98a-137"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa98a-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa98a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aa98a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa98a-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa98a-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa98a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa98a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa98a-141">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="aa98a-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="aa98a-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="aa98a-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





