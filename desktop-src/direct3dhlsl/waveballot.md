---
title: WaveActiveBallot (funzione)
description: Restituisce un uint4 contenente una maschera di maschera della valutazione dell'espressione booleana per tutte le corsie attive nell'onda corrente.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Funzione WaveActiveBallot HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517211"
---
# <a name="waveactiveballot-function"></a>WaveActiveBallot (funzione)

Restituisce un uint4 contenente una maschera di maschera della valutazione dell'espressione booleana per tutte le corsie attive nell'onda corrente. 

## <a name="syntax"></a>Sintassi

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*expr* 
</dt> <dd>

Espressione booleana da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Uint4 contenente una maschera di maschera della valutazione dell'espressione booleana per tutte le corsie attive nell'onda corrente. Il bit meno significativo corrisponde alla corsia con indice zero. I bit corrispondenti alle linee inattive saranno pari a zero. I bit maggiori o uguali a [**WaveGetLaneCount**](wavegetlanecount.md) saranno pari a zero.

## <a name="remarks"></a>Commenti

Diverse GPU hanno larghezze del processore SIMD diverse (conteggi della corsia). La maggior parte di queste funzioni **WaveXXX** è in grado di funzionare al livello dell'astrazione in cui la larghezza del computer SIMD è nascosta. Per ottimizzare la portabilità del codice tra le GPU, usare le funzioni intrinseche che non si basano sulla larghezza del computer. Ad esempio, usare:

``` syntax
uint result = WaveActiveCountBits( bBit );
```

Anziché:

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="examples"></a>Esempi

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




