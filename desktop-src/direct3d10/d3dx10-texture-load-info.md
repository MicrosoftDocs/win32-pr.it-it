---
description: Descrive i parametri usati per caricare una trama da un'altra trama.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: Struttura D3DX10_TEXTURE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322952"
---
# <a name="d3dx10_texture_load_info-structure"></a>\_Struttura delle \_ informazioni di caricamento della trama d3dx10 \_

Descrive i parametri usati per caricare una trama da un'altra trama.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**pSrcBox**
</dt> <dd>

Tipo: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Casella trama di origine (vedere [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Casella trama di destinazione (vedere [**D3D10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello di mipmap trama di origine. per altre informazioni, vedere [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello di mipmap della trama di destinazione. per altre informazioni, vedere [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli di mipmap nella trama di origine.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Primo elemento della trama di origine.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Primo elemento della trama di destinazione.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di elementi da caricare.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni di filtro durante il ricampionamento (vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni di filtro durante la generazione di livelli MIP (vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata in una chiamata a [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
