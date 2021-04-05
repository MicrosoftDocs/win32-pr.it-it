---
description: Definisce le funzioni di confronto supportate.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Enumerazione D3DCMPFUNC (D3D9Types. h)
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
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886273"
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

<span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ mai**
</dt> <dd>

Interrompi sempre il test.

</dd> <dt>

<span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ less**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è minore del valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ uguale a**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**\_LESSEQUAL D3DCMP**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è minore o uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ maggiore**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è maggiore del valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**\_NOTEQUAL D3DCMP**
</dt> <dd>

Accettare il nuovo pixel se il valore non è uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**\_GREATEREQUAL D3DCMP**
</dt> <dd>

Accettare il nuovo pixel se il relativo valore è maggiore o uguale al valore del pixel corrente.

</dd> <dt>

<span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ sempre**
</dt> <dd>

Superare sempre il test.

</dd> <dt>

<span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori in questo tipo enumerato definiscono le funzioni di confronto supportate per gli \_ Stati di rendering D3DRS ZFUNC, D3DRS \_ ALPHAFUNC e D3DRS \_ STENCILFUNC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
