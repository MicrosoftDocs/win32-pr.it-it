---
description: 'Funzione D3DXFresnelTerm (D3DX10Math.h): calcola il termine Fresnel.'
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Funzione D3DXFresnelTerm (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9efa557d44451674d2ae4c48a58370e939760a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113269"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>Funzione D3DXFresnelTerm (D3DX10Math.h)

Calcolare il termine Fresnel.

## <a name="syntax"></a>Sintassi


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CosTheta* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Il valore deve essere compreso tra 0 e 1.

</dd> <dt>

*RefractionIndex* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Indice di refrazione di un materiale. Il valore deve essere maggiore di 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Questa funzione restituisce il termine Fresnel per la luce nonpolarizzata. CosTheta è il coseno dell'angolo dell'evento imprevisto.

## <a name="remarks"></a>Commenti

Per trovare il termine Fresnel (F):

Se A è l'angolo di incidenza e B è l'angolo di rifrazione,


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Quindi, espandendo usando le identità trigonometriche e semplificando, si ottiene:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
