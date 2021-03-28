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
# <a name="waveprefixcountbits-function"></a>WavePrefixCountBits (funzione)

Restituisce la somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente.

## <a name="syntax"></a>Sintassi


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bBit* 
</dt> <dd>

Variabili booleane specificate.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Somma di tutte le variabili booleane specificate impostate su true in tutte le corsie attive con indici più piccoli della corsia corrente.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempio

Il codice seguente descrive come implementare una scrittura compattata in un flusso ordinato in cui il numero di elementi scritti per corsia è 1 o 0.

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

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




