---
title: Funzione D2DSampleInput (D2d1effecthelpers. h)
description: Input di esempio N alla posizione UV. Disponibile solo per gli input complessi.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Direct2D funzione D2DSampleInput
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332786"
---
# <a name="d2dsampleinput-function"></a>D2DSampleInput (funzione)

Input di esempio N alla posizione UV. Disponibile solo per gli input complessi.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Numero di input.

</dd> <dt>

*UV* \[ in\]
</dt> <dd>

Posizione UV.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un **float4** nel formato TEXCOORDN.

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrata la funzione utilizzata per calcolare le normali della superficie.

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
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

 

 





