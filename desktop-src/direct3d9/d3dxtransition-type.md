---
description: Definisce lo stile di transizione tra i valori di un'animazione mesh.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Enumerazione D3DXTRANSITION_TYPE (D3dx9anim. h)
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
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969342"
---
# <a name="d3dxtransition_type-enumeration"></a>\_Enumerazione del tipo D3DXTRANSITION

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

<span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION \_ lineare**
</dt> <dd>

Transizione lineare tra i valori.

</dd> <dt>

<span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**\_EASEINEASEOUT D3DXTRANSITION**
</dt> <dd>

Semplicità di transizione della spline tra i valori.

</dd> <dt>

<span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il calcolo per la rampa da Ease in a Ease Out viene calcolato come segue:

<dl> Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x  
</dl>

dove la rampa è una funzione Q (t) con le proprietà seguenti:

-   Q (t) è una spline cubica.
-   Q (t) esegue l'interpolazione tra x e y come intervallo t compreso tra 0 e 1.
-   Q (t) è orizzontale quando t = 0 e t = 1.

In matematica, questo si traduce in:

<dl> Q (t) = at ³ + BT ² + CT + D (e quindi Q ' (t) = 3At ² + 2Bt + C)  
2a) Q (0) = x  
2b) Q (1) = y  
3a) Q ' (0) = 0  
3B) Q ' (1) = 0  
</dl>

Risoluzione per A, B, C, D:

<dl> D = x (da 2a)  
C = 0 (da 3A)  
3A + 2B = 0 (da 3B)  
A + B = y-x (da 2b e D = x)  
</dl>

Di conseguenza:

<dl> A = 2 (x-y), B = 3 (y-x), C = 0, D = x  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




