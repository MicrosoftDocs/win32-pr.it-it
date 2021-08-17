---
title: Funzione WaveActiveAnyTrue
description: Restituisce true se l'espressione è true in una delle corsie attive nell'ondata corrente.
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
ms.openlocfilehash: 2c49c9727461d316d7d2c9d8f048971384e568476d1ca693aeec49cdf14a4795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721731"
---
# <a name="waveactiveanytrue-function"></a>Funzione WaveActiveAnyTrue

Restituisce true se l'espressione è true in una delle corsie attive nell'ondata corrente.

## <a name="syntax"></a>Sintassi

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Expr* 
</dt> <dd>

Espressione booleana da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

True se l'espressione è true in qualsiasi corsia.

## <a name="remarks"></a>Commenti

Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader. 



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del modello shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modello shader 6](shader-model-6-0.md)
</dt> </dl>

 

 




