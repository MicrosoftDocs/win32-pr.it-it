---
description: La semantica esegue il mapping di un parametro ai pixel shader vertice. Possono anche essere stringhe descrittive facoltative associate a parametri non di registrazione.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Struttura D3DXSEMANTIC (D3dx9shader.h)
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
ms.openlocfilehash: 2534df72c246fdec361597a8e156f7f19b341ae35fcc04b3bdc6eb71c2903fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631021"
---
# <a name="d3dxsemantic-structure"></a>Struttura D3DXSEMANTIC

La semantica esegue il mapping di un parametro ai pixel shader vertice. Possono anche essere stringhe descrittive facoltative associate a parametri non di registrazione.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni che identificano la modalità di utilizzo delle risorse. Vedere [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni che modificano la modalità di interpretazione dell'utilizzo. L'indice di utilizzo e di utilizzo costituiscono una dichiarazione di vertice. Vedere [Dichiarazione dei vertici (Direct3D 9).](vertex-declaration.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La semantica è necessaria per i pixel shader vertice, i registri di input e output.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture degli effetti](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
