---
description: Definisce le funzioni di confronto supportate.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Enumerazione D3DCMPFUNC (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fa8d0c9288e6c0d516e7fc9b8a07237f553dd6c86072f1895edf9a79c297077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989109"
---
# <a name="d3dcmpfunc-enumeration"></a>Enumerazione D3DCMPFUNC

Definisce le funzioni di confronto supportate.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ NEVER**
</dt> <dd>

Non è sempre possibile eseguire il test.

</dd> <dt>

<span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ LESS**
</dt> <dd>

Accettare il nuovo pixel se il valore è minore del valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ UGUALE**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**
</dt> <dd>

Accettare il nuovo pixel se il valore è minore o uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ GREATER**
</dt> <dd>

Accettare il nuovo pixel se il valore è maggiore del valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP \_ NOTEQUAL**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore non è uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ GREATEREQUAL**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è maggiore o uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ ALWAYS**
</dt> <dd>

Superare sempre il test.

</dd> <dt>

<span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori in questo tipo enumerato definiscono le funzioni di confronto supportate per gli stati di rendering D3DRS \_ ZFUNC, D3DRS \_ ALPHAFUNC e D3DRS \_ STENCILFUNC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
