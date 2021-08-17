---
description: Specifica come combinare i dati del glifo dalle superfici di origine e di destinazione in una chiamata a ComposeRects.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: Enumerazione D3DCOMPOSERECTSOP (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8d968770eb58d9d3dd59f178b05e8e6536079e8de601ddef602a41da4b52ee51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911169"
---
# <a name="d3dcomposerectsop-enumeration"></a>Enumerazione D3DCOMPOSERECTSOP

Specifica come combinare i dati del glifo dalle superfici di origine e di destinazione in una chiamata a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**COPIA D3DCOMPOSERECTS \_**
</dt> <dd>

Copiare l'origine nella destinazione.

</dd> <dt>

<span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ O**
</dt> <dd>

OR bit per bit l'origine e la destinazione.

</dd> <dt>

<span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ E**
</dt> <dd>

AND bit per bit l'origine e la destinazione.

</dd> <dt>

<span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ NEG**
</dt> <dd>

Copiare l'origine negata nella destinazione (Dst & ~Src).

</dd> <dt>

<span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ FORZA \_ DWORD**
</dt> <dd>

Riservato. Utilizzato per forzare l'enumerazione a dimensioni a 32 bit.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




