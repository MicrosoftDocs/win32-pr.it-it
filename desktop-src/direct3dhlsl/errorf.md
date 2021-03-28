---
title: errorf (funzione)
description: Invia un messaggio di errore alla coda delle informazioni.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- funzione errorf HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045602"
---
# <a name="errorf-function"></a><span data-ttu-id="72b87-104">errorf (funzione)</span><span class="sxs-lookup"><span data-stu-id="72b87-104">errorf function</span></span>

<span data-ttu-id="72b87-105">Invia un messaggio di errore alla coda delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="72b87-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b87-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72b87-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="72b87-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="72b87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b87-108">*format*</span><span class="sxs-lookup"><span data-stu-id="72b87-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="72b87-109">Stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="72b87-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="72b87-110">*argomento...*</span><span class="sxs-lookup"><span data-stu-id="72b87-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="72b87-111">Argomenti facoltativi.</span><span class="sxs-lookup"><span data-stu-id="72b87-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72b87-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72b87-112">Return value</span></span>

<span data-ttu-id="72b87-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="72b87-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b87-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="72b87-114">Remarks</span></span>

<span data-ttu-id="72b87-115">Questa operazione non esegue alcuna operazione nei dispositivi che non lo supportano.</span><span class="sxs-lookup"><span data-stu-id="72b87-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="72b87-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="72b87-116">Minimum Shader Model</span></span>

<span data-ttu-id="72b87-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="72b87-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="72b87-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="72b87-118">Shader Model</span></span>                                                        | <span data-ttu-id="72b87-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="72b87-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="72b87-120">Shader Model 4 (DirectX HLSL) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="72b87-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="72b87-121">sì</span><span class="sxs-lookup"><span data-stu-id="72b87-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="72b87-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72b87-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b87-123">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="72b87-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




