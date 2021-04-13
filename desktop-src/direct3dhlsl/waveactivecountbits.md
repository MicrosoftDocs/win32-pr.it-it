---
title: WaveActiveCountBits (funzione)
description: Conta il numero di variabili booleane che restituiscono true tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Funzione WaveActiveCountBits HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2020
ms.locfileid: "104339779"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="04bf2-104">WaveActiveCountBits (funzione)</span><span class="sxs-lookup"><span data-stu-id="04bf2-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="04bf2-105">Conta il numero di variabili booleane che restituiscono true tra tutte le corsie attive nell'onda corrente e replica il risultato in tutte le corsie dell'onda.</span><span class="sxs-lookup"><span data-stu-id="04bf2-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="04bf2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04bf2-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="04bf2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="04bf2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04bf2-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="04bf2-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="04bf2-109">Variabili booleane da valutare.</span><span class="sxs-lookup"><span data-stu-id="04bf2-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="04bf2-110">Se si specifica un valore booleano true esplicito, viene restituito il numero di corsie attive.</span><span class="sxs-lookup"><span data-stu-id="04bf2-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04bf2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04bf2-111">Return value</span></span>

<span data-ttu-id="04bf2-112">Il numero di che restituisce true in tutte le corsie attive nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="04bf2-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="04bf2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="04bf2-113">Remarks</span></span>

<span data-ttu-id="04bf2-114">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="04bf2-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="04bf2-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="04bf2-115">Examples</span></span>

<span data-ttu-id="04bf2-116">Questa operazione può essere implementata in modo più efficiente rispetto a una WaveActiveSum completa, come descritto nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="04bf2-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="04bf2-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04bf2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bf2-118">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="04bf2-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="04bf2-119">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="04bf2-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




