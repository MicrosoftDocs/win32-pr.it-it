---
title: D1114 puntatore non facoltativo NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: "Il parametro per Interface:: Method non è facoltativo. È stato passato un puntatore NULL. Questo provocherà l'arresto anomalo di Direct2D."
keywords:
- D1114 non facoltativo puntatore NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334159"
---
# <a name="d1114-non-optional-pointer-null"></a><span data-ttu-id="4c304-106">D1114: puntatore NULL non facoltativo</span><span class="sxs-lookup"><span data-stu-id="4c304-106">D1114: Non Optional Pointer NULL</span></span>

<span data-ttu-id="4c304-107">Il parametro \[ *Parameter* \] per *Interface*::*Method* non è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4c304-107">The parameter \[*parameter*\] for *interface*::*method* is not optional.</span></span> <span data-ttu-id="4c304-108">È stato passato un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="4c304-108">A **NULL** pointer was passed.</span></span> <span data-ttu-id="4c304-109">Questo provocherà l'arresto anomalo di Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4c304-109">This will cause Direct2D to crash.</span></span>

### <a name="placeholders"></a><span data-ttu-id="4c304-110">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="4c304-110">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="4c304-111"><span id="parameter"></span><span id="PARAMETER"></span>*parametro*</span><span class="sxs-lookup"><span data-stu-id="4c304-111"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="4c304-112">Nome del parametro che contiene il puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="4c304-112">The name of the parameter that contains the **NULL** pointer.</span></span>

</dd> <dt>

<span data-ttu-id="4c304-113"><span id="interface"></span><span id="INTERFACE"></span>*interfaccia*</span><span class="sxs-lookup"><span data-stu-id="4c304-113"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="4c304-114">Nome dell'interfaccia a cui appartiene il *Metodo* .</span><span class="sxs-lookup"><span data-stu-id="4c304-114">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="4c304-115"><span id="method"></span><span id="METHOD"></span>*Metodo*</span><span class="sxs-lookup"><span data-stu-id="4c304-115"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="4c304-116">Nome del metodo che ha ricevuto il parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="4c304-116">The name of the method that received the invalid parameter.</span></span>

</dd> </dl> 




 

### <a name="examples"></a><span data-ttu-id="4c304-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="4c304-117">Examples</span></span>

<span data-ttu-id="4c304-118">Nell'esempio seguente viene illustrato che il metodo [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) riceve un puntatore null per il parametro *Geometry* non facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4c304-118">The following example shows that the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method receives a NULL pointer for the non-optional *geometry* parameter.</span></span>


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



<span data-ttu-id="4c304-119">Questo esempio produce il seguente messaggio di debug:</span><span class="sxs-lookup"><span data-stu-id="4c304-119">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a><span data-ttu-id="4c304-120">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="4c304-120">Possible Causes</span></span>

<span data-ttu-id="4c304-121">È stato passato un puntatore NULL per un parametro non facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4c304-121">A NULL pointer was passed for a non-optional parameter.</span></span>

## <a name="fixes"></a><span data-ttu-id="4c304-122">Correzioni</span><span class="sxs-lookup"><span data-stu-id="4c304-122">Fixes</span></span>

<span data-ttu-id="4c304-123">Verificare che un parametro non facoltativo non disponga di un puntatore NULL.</span><span class="sxs-lookup"><span data-stu-id="4c304-123">Ensure that a non-optional parameter does not have a NULL pointer.</span></span>

 

 
