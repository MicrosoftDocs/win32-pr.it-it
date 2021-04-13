---
description: La semantica esegue il mapping di un parametro ai registri vertici o pixel shader. Possono anche essere stringhe descrittive facoltative associate a parametri non di registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Struttura D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401951"
---
# <a name="d3dxsemantic-structure"></a>Struttura D3DXSEMANTIC

La semantica esegue il mapping di un parametro ai registri vertici o pixel shader. Possono anche essere stringhe descrittive facoltative associate a parametri non di registro.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>Members

<dl> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni che identificano la modalità di utilizzo delle risorse. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni che modificano il modo in cui viene interpretato l'utilizzo. L'utilizzo e l'indice di utilizzo costituiscono una dichiarazione di vertice. Vedere [dichiarazione vertici (Direct3D 9)](vertex-declaration.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La semantica è obbligatoria per i registri Vertex e pixel shader, di input e di output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
