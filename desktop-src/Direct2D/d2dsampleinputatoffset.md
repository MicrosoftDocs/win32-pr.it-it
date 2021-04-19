---
title: Funzione D2DSampleInputAtOffset (D2d1effecthelpers. h)
description: Campiona l'input N a un offset di offset dalla coordinata di input. Disponibile solo per gli input complessi.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Direct2D funzione D2DSampleInputAtOffset
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332785"
---
# <a name="d2dsampleinputatoffset-function"></a>D2DSampleInputAtOffset (funzione)

Campiona l'input N a un offset di offset dalla coordinata di input. Disponibile solo per gli input complessi.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Numero di input.

</dd> <dt>

*offset* \[ in\]
</dt> <dd>

Offset UV.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un **float4** nel formato TEXCOORDN.

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrata la funzione utilizzata come parte di una maschera di sfumatura di evidenziazione e ombreggiatura.

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
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

 

 





