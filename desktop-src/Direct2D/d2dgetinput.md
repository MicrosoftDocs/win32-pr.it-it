---
title: Funzione D2DGetInput (D2d1effecthelpers.h)
description: Restituisce il colore dell'input N in corrispondenza della coordinata di input. Disponibile solo per input semplici.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Funzione D2DGetInput Direct2D
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
ms.openlocfilehash: 37de536eb6ac36af3e8aa1ffca61c3840cf6c84e585466a56a447522c4d628d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075315"
---
# <a name="d2dgetinput-function"></a>Funzione D2DGetInput

Restituisce il colore dell'input N in corrispondenza della coordinata di input. Disponibile solo per input semplici.

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

La funzione restituisce un **valore float4** contenente il colore RGBA nel formato INPUTN.

## <a name="remarks"></a>Commenti

L'esempio seguente illustra la funzione usata come parte di un effetto composito aritmetico.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Per un altro esempio dell'uso di questa funzione, vedere anche le osservazioni relative a [D2D \_ PS \_ ENTRY.](d2d-ps-entry.md)

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

 

 





