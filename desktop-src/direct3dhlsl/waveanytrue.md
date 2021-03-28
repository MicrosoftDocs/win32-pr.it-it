---
title: WaveActiveAnyTrue (funzione)
description: Restituisce true se l'espressione è true in una delle corsie attive nell'onda corrente.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Funzione WaveActiveAnyTrue HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993613"
---
# <a name="waveactiveanytrue-function"></a>WaveActiveAnyTrue (funzione)

Restituisce true se l'espressione è true in una delle corsie attive nell'onda corrente.

## <a name="syntax"></a>Sintassi

``` syntax
bool WaveActiveAnyTrue(
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

True se l'espressione è true in una corsia.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




