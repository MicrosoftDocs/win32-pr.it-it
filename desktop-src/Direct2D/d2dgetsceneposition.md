---
title: Funzione D2DGetScenePosition (D2d1effecthelpers. h)
description: Restituisce il valore della posizione della scena di input \_ . Disponibile solo quando D2D \_ richiede \_ che \_ la posizione della scena sia dichiarata nel file di origine.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Direct2D funzione D2DGetScenePosition
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
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332359"
---
# <a name="d2dgetsceneposition-function"></a>D2DGetScenePosition (funzione)

Restituisce il valore della posizione della scena di input \_ . Disponibile solo quando D2D \_ richiede \_ che \_ la posizione della scena sia dichiarata nel file di origine.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

La funzione restituisce un **float4** nella posizione della scena del formato \_ .

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato l'uso della funzione nella generazione di un modello di dissolvenza.

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
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamento Effect shader](effect-shader-linking.md)
</dt> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





