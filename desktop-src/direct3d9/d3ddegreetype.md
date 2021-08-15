---
description: Definisce il grado delle variabili nell'equazione che descrive una curva.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Enumerazione D3DDEGREETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6daacc007438903d3f003a19038b4ea6909814e3a5d024d3df6daa95a0c60602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989051"
---
# <a name="d3ddegreetype-enumeration"></a>Enumerazione D3DDEGREETYPE

Definisce il grado delle variabili nell'equazione che descrive una curva.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**LINEARE D3DDEGREE \_**
</dt> <dd>

La curva è descritta da variabili di primo ordine.

</dd> <dt>

<span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**QUADRATICA D3DDEGREE \_**
</dt> <dd>

La curva è descritta da variabili di secondo ordine.

</dd> <dt>

<span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**CUBO D3DDEGREE \_**
</dt> <dd>

La curva è descritta da variabili di terzo ordine.

</dd> <dt>

<span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ QUINTIC**
</dt> <dd>

La curva è descritta da variabili di quarto ordine.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori di questa enumerazione vengono usati per descrivere le curve usate dalle patch di rettangolo e triangolo. Per altre informazioni, vedere D3DRS \_ CULLMODE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
