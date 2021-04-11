---
description: Incapsula un frame di trasformazione in una gerarchia di frame di trasformazione.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Struttura D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235018"
---
# <a name="d3dxframe-structure"></a>Struttura D3DXFRAME

Incapsula un frame di trasformazione in una gerarchia di frame di trasformazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome del frame.

</dd> <dt>

**TransformationMatrix**
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

Matrice di trasformazione.

</dd> <dt>

**pMeshContainer**
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

Puntatore al contenitore mesh.

</dd> <dt>

**pFrameSibling**
</dt> <dd>

Tipo: * * * * D3DXFRAME **\***

</dd> <dd>

Puntatore a un frame di pari livello.

</dd> <dt>

**pFrameFirstChild**
</dt> <dd>

Tipo: * * * * D3DXFRAME **\***

</dd> <dd>

Puntatore a un frame figlio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un'applicazione può derivare da questa struttura per aggiungere altri dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




