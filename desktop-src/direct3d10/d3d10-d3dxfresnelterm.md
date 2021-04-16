---
description: Calcolare il termine Fresnel.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Funzione D3DXFresnelTerm (D3DX10Math. h)
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
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531051"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a>Funzione D3DXFresnelTerm (D3DX10Math. h)

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

*CosTheta* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Il valore deve essere compreso tra 0 e 1.

</dd> <dt>

*RefractionIndex* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Indice di rifrazione di un materiale. Il valore deve essere maggiore di 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Questa funzione restituisce il termine Fresnel per la luce non polarizzata. CosTheta è il coseno dell'angolo dell'evento imprevisto.

## <a name="remarks"></a>Commenti

Per trovare il termine Fresnel (F):

Se A è angolo di incidenza e B è l'angolo della rifrazione,


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



Quindi, espandendo usando le identità trigonometriche e semplificando, si ottengono:


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni matematiche](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
