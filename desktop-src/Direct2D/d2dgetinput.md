---
title: Funzione D2DGetInput (D2d1effecthelpers. h)
description: Restituisce il colore dell'input N nella coordinata di input. Disponibile solo per gli input semplici.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Direct2D funzione D2DGetInput
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331663"
---
# <a name="d2dgetinput-function"></a>D2DGetInput (funzione)

Restituisce il colore dell'input N nella coordinata di input. Disponibile solo per gli input semplici.

## <a name="syntax"></a>Sintassi

``` syntax
float4 WINAPI D2DGetInput(
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

La funzione restituisce un **float4** contenente il colore RGBA nel formato inputn.

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrata la funzione utilizzata come parte di un effetto composito aritmetico.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Per un altro esempio dell'uso di questa funzione, vedere anche la sezione Osservazioni per la [ \_ \_ voce D2D PS](d2d-ps-entry.md) .

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

 

 





