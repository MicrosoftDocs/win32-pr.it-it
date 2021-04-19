---
title: Funzione D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Restituisce il valore di TEXCOORDN di input. Disponibile solo per gli input complessi.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Direct2D funzione D2DGetInputCoordinate
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332365"
---
# <a name="d2dgetinputcoordinate-function"></a>D2DGetInputCoordinate (funzione)

Restituisce il valore di TEXCOORDN di input. Disponibile solo per gli input complessi.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Numero di input.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un **float4** nel formato TEXCOORDN.

## <a name="remarks"></a>Commenti

La coordinata restituita da questa funzione è nello spazio Texel. Uno shader non deve prendere alcuna dipendenza dal modo in cui questo valore viene calcolato. Deve utilizzarlo solo per campionare l'input del pixel shader. Per altre informazioni, vedere [aggiunta di un pixel shader a una trasformazione personalizzata](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).

Nell'esempio seguente viene illustrata la funzione utilizzata per un effetto Mappa di spostamento.

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
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

 

