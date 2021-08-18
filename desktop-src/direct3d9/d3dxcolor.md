---
description: 'Struttura D3DXCOLOR (D3dx9math.h): descrive i valori dei colori.'
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Struttura D3DXCOLOR (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 28f170814988317cd1cdf3300e4cbb3c2a97fa0fac7a43b2231767914a9b103a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988721"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a>Struttura D3DXCOLOR (D3dx9math.h)

Descrive i valori dei colori.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a>Members

<dl> <dt>

**r**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente rosso del colore.

</dd> <dt>

**G**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente verde del colore.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente blu del colore.

</dd> <dt>

**Un**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Componente alfa del colore.

</dd> </dl>

## <a name="remarks"></a>Commenti

I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXCOLOR,**](d3dxcolor-extensions.md)che implementano costruttori di overload, nonché operatori di assegnazione, unari e binari (inclusa l'uguaglianza).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
