---
title: Funzione D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: Campiona l'input N in una posizione assoluta della scena, anziché una posizione relativa all'input. Disponibile solo per gli input complessi.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Direct2D funzione D2DSampleInputAtPosition
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332784"
---
# <a name="d2dsampleinputatposition-function"></a>D2DSampleInputAtPosition (funzione)

Campiona l'input N in una posizione assoluta della scena, anziché una posizione relativa all'input. Disponibile solo per gli input complessi.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
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

Nell'esempio seguente viene illustrata la funzione utilizzata in un ritorno a capo circolare.

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
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

 

 





