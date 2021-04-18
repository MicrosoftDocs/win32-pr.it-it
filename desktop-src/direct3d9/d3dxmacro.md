---
description: Descrive le definizioni del preprocessore utilizzate da un oggetto effetto.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Struttura D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323247"
---
# <a name="d3dxmacro-structure"></a>Struttura D3DXMACRO

Descrive le definizioni del preprocessore utilizzate da un oggetto effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome del preprocessore.

</dd> <dt>

**Definition**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Nome della definizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare **D3DXMACRO** in più di una riga, anteporre a ogni carattere di nuova riga una barra rovesciata (ad esempio, \# define nel linguaggio C). Ad esempio:


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



Si notino i 3 caratteri di barra rovesciata alla fine della riga. I primi due sono necessari per restituire un singolo oggetto ' \\ ', seguito dal carattere di nuova riga " \\ n". Facoltativamente, è anche possibile terminare le righe usando " \\ \\ \\ r \\ n".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
