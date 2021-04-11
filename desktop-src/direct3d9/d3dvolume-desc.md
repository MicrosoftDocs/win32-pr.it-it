---
description: Descrive un volume.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Struttura D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355189"
---
# <a name="d3dvolume_desc-structure"></a>\_Struttura D3DVOLUME DESC

Descrive un volume.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di superficie del volume.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) , che identifica questa risorsa come volume.

</dd> <dt>

**Utilizzo**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Attualmente non usato. Restituito sempre come 0.

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che specifica la classe di memoria allocata per questo volume.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza, in pixel, del volume.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza, in pixel, del volume.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondità del volume, in pixel.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getdesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
