---
description: Definisce lo stile di transizione tra i valori di un'animazione mesh.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: D3DXTRANSITION_TYPE enumerazione (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f451b94fe204a82cd15c65e424cc214025aa670f82af5224897100cbc6f8f6e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730938"
---
# <a name="d3dxtransition_type-enumeration"></a>Enumerazione D3DXTRANSITION \_ TYPE

Definisce lo stile di transizione tra i valori di un'animazione mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ LINEAR**
</dt> <dd>

Transizione lineare tra valori.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ EASEINEASEOUT**
</dt> <dd>

Transizione spline semplice e semplice tra valori.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il calcolo della rampa dalla facilità all'uscita viene calcolato come segue:

<dl> Q(t) = 2(x - y)t² + 3(y - x)t² + x  
</dl>

dove ramp è una funzione Q(t) con le proprietà seguenti:

-   Q(t) è una spline cubica.
-   Q(t) interpola tra x e y come t compreso tra 0 e 1.
-   Q(t) è orizzontale quando t = 0 e t = 1.

Matematicamente, ciò si traduce in:

<dl> Q(t) = Atdare + Bt² + Ct + D (e quindi Q'(t) = 3At² + 2Bt + C)  
2a) Q(0) = x  
2b) Q(1) = y  
3a) Q'(0) = 0  
3b) Q'(1) = 0  
</dl>

Risoluzione per A, B, C, D:

<dl> D = x (da 2a)  
C = 0 (da 3a)  
3A + 2B = 0 (da 3b)  
A + B = y - x (da 2b e D = x)  
</dl>

Di conseguenza:

<dl> A = 2(x - y), B = 3(y - x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




