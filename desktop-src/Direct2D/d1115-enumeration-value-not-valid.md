---
title: Valore di enumerazione D1115 non valido
description: Valore di enumerazione D1115 non valido
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- Valore di enumerazione D1115 non valido Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334277"
---
# <a name="d1115-enumeration-value-not-valid"></a><span data-ttu-id="117bc-104">D1115: valore di enumerazione non valido</span><span class="sxs-lookup"><span data-stu-id="117bc-104">D1115: Enumeration Value Not Valid</span></span>

<span data-ttu-id="117bc-105">Il parametro Parameter con valore Value \[  \] \[  \] per *Interface*::*Method* non è un valore di enumerazione valido.</span><span class="sxs-lookup"><span data-stu-id="117bc-105">The parameter \[*parameter*\] with value \[*value*\] for *interface*::*method* is not a valid enumeration value.</span></span>

## <a name="placeholders"></a><span data-ttu-id="117bc-106">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="117bc-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="117bc-107"><span id="parameter"></span><span id="PARAMETER"></span>*parametro*</span><span class="sxs-lookup"><span data-stu-id="117bc-107"><span id="parameter"></span><span id="PARAMETER"></span>*parameter*</span></span>
</dt> <dd>

<span data-ttu-id="117bc-108">Nome del parametro che ha ricevuto il tipo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="117bc-108">The name of the parameter that received the unexpected type.</span></span>

</dd> <dt>

<span data-ttu-id="117bc-109"><span id="value"></span><span id="VALUE"></span>*valore*</span><span class="sxs-lookup"><span data-stu-id="117bc-109"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="117bc-110">Valore di enumerazione non valido.</span><span class="sxs-lookup"><span data-stu-id="117bc-110">The invalid enumeration value.</span></span>

</dd> <dt>

<span data-ttu-id="117bc-111"><span id="interface"></span><span id="INTERFACE"></span>*interfaccia*</span><span class="sxs-lookup"><span data-stu-id="117bc-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="117bc-112">Nome dell'interfaccia a cui appartiene il *Metodo* .</span><span class="sxs-lookup"><span data-stu-id="117bc-112">The name of the interface to which the *method* belongs.</span></span>

</dd> <dt>

<span data-ttu-id="117bc-113"><span id="method"></span><span id="METHOD"></span>*Metodo*</span><span class="sxs-lookup"><span data-stu-id="117bc-113"><span id="method"></span><span id="METHOD"></span>*method*</span></span>
</dt> <dd>

<span data-ttu-id="117bc-114">Nome del metodo che ha ricevuto il valore di enumerazione non valido.</span><span class="sxs-lookup"><span data-stu-id="117bc-114">The name of the method that received the invalid enumeration value.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="117bc-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="117bc-115">Examples</span></span>

<span data-ttu-id="117bc-116">Nell'esempio seguente viene specificato un valore di enumerazione del [**\_ tipo di \_ destinazione \_ di rendering d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) pari a 30, che non è compreso nell'intervallo previsto.</span><span class="sxs-lookup"><span data-stu-id="117bc-116">The following example specifies a [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) enumeration value of 30, which is outside the expected range.</span></span>


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



<span data-ttu-id="117bc-117">Questo esempio produce il seguente messaggio di debug:</span><span class="sxs-lookup"><span data-stu-id="117bc-117">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a><span data-ttu-id="117bc-118">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="117bc-118">Possible Causes</span></span>

<span data-ttu-id="117bc-119">Un parametro usava un valore di enumerazione non valido.</span><span class="sxs-lookup"><span data-stu-id="117bc-119">A parameter used an invalid enumeration value.</span></span>

## <a name="fixes"></a><span data-ttu-id="117bc-120">Correzioni</span><span class="sxs-lookup"><span data-stu-id="117bc-120">Fixes</span></span>

<span data-ttu-id="117bc-121">Usare un valore di enumerazione valido.</span><span class="sxs-lookup"><span data-stu-id="117bc-121">Use a valid enumeration value.</span></span>

> [!Note]  
> <span data-ttu-id="117bc-122">Il livello di debug controlla attualmente solo i singoli valori di enumerazione. non verifica se una combinazione bit per bit è valida.</span><span class="sxs-lookup"><span data-stu-id="117bc-122">The debug layer currently checks only the individual enumeration values; it does not check whether a bitwise combination is valid.</span></span>

 

 

 
