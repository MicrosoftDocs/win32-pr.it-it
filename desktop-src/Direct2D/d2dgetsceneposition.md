---
title: Funzione D2DGetScenePosition (D2d1effecthelpers.h)
description: Restituisce il valore dell'oggetto SCENE \_ POSITION di input. Disponibile solo quando D2D \_ REQUIRES SCENE POSITION è dichiarato nel file di \_ \_ origine.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Funzione D2DGetScenePosition Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd7a1ee987cf64a92aa76b0f8910bee1c9a15465872bbd3ccfe2502629f700
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641641"
---
# <a name="d2dgetsceneposition-function"></a>Funzione D2DGetScenePosition

Restituisce il valore dell'oggetto SCENE \_ POSITION di input. Disponibile solo quando D2D \_ REQUIRES SCENE POSITION è dichiarato nel file di \_ \_ origine.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

La funzione restituisce un **valore float4** nel formato SCENE \_ POSITION.

## <a name="remarks"></a>Commenti

L'esempio seguente illustra l'uso della funzione nella generazione di un modello di dissolvimento.

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamento degli effetti shader](effect-shader-linking.md)
</dt> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





