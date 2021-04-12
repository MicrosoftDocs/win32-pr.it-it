---
description: Incapsula un oggetto mesh in una gerarchia di frame di trasformazione.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Struttura D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354179"
---
# <a name="d3dxmeshcontainer-structure"></a>Struttura D3DXMESHCONTAINER

Incapsula un oggetto mesh in una gerarchia di frame di trasformazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a>Members

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nome della rete.

</dd> <dt>

**MeshData**
</dt> <dd>

Tipo: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**

</dd> <dd>

Tipo di dati nella rete. Vedere [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

**pMaterials**
</dt> <dd>

Tipo: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**

</dd> <dd>

Matrice di materiali mesh. Vedere [**D3DXMATERIAL**](d3dxmaterial.md).

</dd> <dt>

**pEffects**
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**

</dd> <dd>

Puntatore a un set di parametri di effetto predefiniti. Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

**NumMaterials**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di materiali nella rete.

</dd> <dt>

**pAdjacency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Puntatore a una matrice di tre DWORD per triangolo della mesh che contiene informazioni adiacenza.

</dd> <dt>

**pSkinInfo**
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

</dd> <dd>

Puntatore all'interfaccia di informazioni sull'interfaccia personalizzata. Vedere [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

**pNextMeshContainer**
</dt> <dd>

Tipo: * * * * D3DXMESHCONTAINER **\***

</dd> <dd>

Puntatore al contenitore mesh successivo.

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

 

 
