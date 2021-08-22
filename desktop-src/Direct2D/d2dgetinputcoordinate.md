---
title: Funzione D2DGetInputCoordinate (D2d1effecthelpers.h)
description: Restituisce il valore dell'oggetto TEXCOORDN di input. Disponibile solo per input complessi.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Funzione D2DGetInputCoordinate Direct2D
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
ms.openlocfilehash: 5a3fe0d825dea70c8e5211b8c13f1e850fa513670bbc93de98f1f8e2b87ef046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075295"
---
# <a name="d2dgetinputcoordinate-function"></a>Funzione D2DGetInputCoordinate

Restituisce il valore dell'oggetto TEXCOORDN di input. Disponibile solo per input complessi.

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

La funzione restituisce **un valore float4** nel formato TEXCOORDN.

## <a name="remarks"></a>Commenti

La coordinata restituita da questa funzione si trova nello spazio texel. Uno shader non deve assumere alcuna dipendenza dal modo in cui viene calcolato questo valore. Deve usarlo solo per campionare l'pixel shader'input dell'utente. Per altre informazioni, vedere [Aggiunta di un pixel shader a una trasformazione personalizzata.](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform)

Nell'esempio seguente viene illustrata la funzione utilizzata per un effetto mappa di spostamento.

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
| Intestazione<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Collegamento degli shader degli effetti](effect-shader-linking.md)
</dt> <dt>

[Helper HLSL](hlsl-helpers.md)
</dt> </dl>

 

