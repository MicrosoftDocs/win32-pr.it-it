---
title: WavePrefixCountBits (funzione)
description: Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- Funzione WavePrefixCountBits HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047599"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="936eb-104">WavePrefixCountBits (funzione)</span><span class="sxs-lookup"><span data-stu-id="936eb-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="936eb-105">Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente.</span><span class="sxs-lookup"><span data-stu-id="936eb-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="936eb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="936eb-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="936eb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="936eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936eb-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="936eb-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="936eb-109">Variabili booleane specificate.</span><span class="sxs-lookup"><span data-stu-id="936eb-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936eb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="936eb-110">Return value</span></span>

<span data-ttu-id="936eb-111">Somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente.</span><span class="sxs-lookup"><span data-stu-id="936eb-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="936eb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="936eb-112">Remarks</span></span>

<span data-ttu-id="936eb-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="936eb-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="936eb-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="936eb-114">Examples</span></span>

<span data-ttu-id="936eb-115">Il codice seguente descrive come implementare una scrittura compattata in un flusso ordinato in cui il numero di elementi scritti per corsia è 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="936eb-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a><span data-ttu-id="936eb-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="936eb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936eb-117">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="936eb-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="936eb-118">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="936eb-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




