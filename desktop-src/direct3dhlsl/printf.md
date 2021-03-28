---
title: printf (funzione)
description: Invia un messaggio shader personalizzato alla coda di informazioni.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- funzione printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103956008"
---
# <a name="printf-function"></a><span data-ttu-id="5e6e1-104">printf (funzione)</span><span class="sxs-lookup"><span data-stu-id="5e6e1-104">printf function</span></span>

<span data-ttu-id="5e6e1-105">Invia un messaggio shader personalizzato alla coda di informazioni.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-105">Submits a custom shader message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6e1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e6e1-106">Syntax</span></span>

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="5e6e1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e6e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e6e1-108">*format*</span><span class="sxs-lookup"><span data-stu-id="5e6e1-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="5e6e1-109">Stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="5e6e1-110">*argomento...*</span><span class="sxs-lookup"><span data-stu-id="5e6e1-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="5e6e1-111">Argomenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e6e1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e6e1-112">Return value</span></span>

<span data-ttu-id="5e6e1-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6e1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e6e1-114">Remarks</span></span>

<span data-ttu-id="5e6e1-115">Questa operazione non esegue alcuna operazione nei dispositivi che non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="5e6e1-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="5e6e1-116">Minimum Shader Model</span></span>

<span data-ttu-id="5e6e1-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5e6e1-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="5e6e1-118">Shader Model</span></span>                                                        | <span data-ttu-id="5e6e1-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="5e6e1-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="5e6e1-120">Shader Model 4 (DirectX HLSL) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="5e6e1-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5e6e1-121">sì</span><span class="sxs-lookup"><span data-stu-id="5e6e1-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5e6e1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e6e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6e1-123">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="5e6e1-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




