---
description: Restituisce le informazioni sul materiale salvate nei file Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Struttura D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322137"
---
# <a name="d3dxmaterial-structure"></a>Struttura D3DXMATERIAL

Restituisce le informazioni sul materiale salvate nei file Direct3D (. x).

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a>Members

<dl> <dt>

**MatD3D**
</dt> <dd>

Tipo: **[ **D3DMATERIAL9**](d3dmaterial9.md)**

</dd> <dd>

Struttura [**D3DMATERIAL9**](d3dmaterial9.md) che descrive le proprietà del materiale.

</dd> <dt>

**pTextureFilename**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Puntatore a una stringa che specifica il nome del file della trama.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le funzioni [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) e [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) restituiscono una matrice di strutture **D3DXMATERIAL** che specificano il colore e il nome del materiale della trama per ogni materiale presente nella rete. L'applicazione è quindi necessaria per caricare la trama.

Il tipo LPD3DXMATERIAL è definito come un puntatore alla struttura **D3DXMATERIAL** .


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md)
</dt> <dt>

[**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




