---
title: funzione Abort (Corecrt \_ Terminate. h)
description: Invia un messaggio di errore alla coda di informazioni e termina la chiamata di progetto o di invio corrente eseguita.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- funzione Abort HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982635"
---
# <a name="abort-function"></a><span data-ttu-id="8e98a-104">abort (funzione)</span><span class="sxs-lookup"><span data-stu-id="8e98a-104">abort function</span></span>

<span data-ttu-id="8e98a-105">Invia un messaggio di errore alla coda di informazioni e termina la chiamata di progetto o di invio corrente eseguita.</span><span class="sxs-lookup"><span data-stu-id="8e98a-105">Submits an error message to the information queue and terminates the current draw or dispatch call being executed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e98a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e98a-106">Syntax</span></span>

``` syntax
void abort(
    
);
```

## <a name="parameters"></a><span data-ttu-id="8e98a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e98a-107">Parameters</span></span>

<dl> <dt>

 
</dt> <dd>

<span data-ttu-id="8e98a-108">nessuno</span><span class="sxs-lookup"><span data-stu-id="8e98a-108">None</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e98a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e98a-109">Return value</span></span>

<span data-ttu-id="8e98a-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8e98a-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e98a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e98a-111">Remarks</span></span>

<span data-ttu-id="8e98a-112">Questa operazione non esegue alcuna operazione nei rasterizzatori che non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="8e98a-112">This operation does nothing on rasterizers that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="8e98a-113">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8e98a-113">Minimum Shader Model</span></span>

<span data-ttu-id="8e98a-114">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e98a-114">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8e98a-115">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8e98a-115">Shader Model</span></span>                                                        | <span data-ttu-id="8e98a-116">Supportato</span><span class="sxs-lookup"><span data-stu-id="8e98a-116">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="8e98a-117">Shader Model 4 (DirectX HLSL) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8e98a-117">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e98a-118">sì</span><span class="sxs-lookup"><span data-stu-id="8e98a-118">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="8e98a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e98a-119">Requirements</span></span>



| <span data-ttu-id="8e98a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e98a-120">Requirement</span></span> | <span data-ttu-id="8e98a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8e98a-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e98a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e98a-122">Header</span></span><br/> | <dl> <span data-ttu-id="8e98a-123"><dt>Corecrt \_ termina. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e98a-123"><dt>Corecrt\_terminate.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e98a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e98a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e98a-125">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="8e98a-125">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





