---
description: Descrive i parametri usati per caricare una trama da un'altra trama.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: D3DX10_TEXTURE_LOAD_INFO struttura (D3DX10Tex.h)
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
ms.openlocfilehash: 144475b4b4967ff0a1fd130a658b8276af5d8897cc043000d150417aa01b227e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753471"
---
# <a name="d3dx10_texture_load_info-structure"></a>Struttura D3DX10 \_ TEXTURE \_ LOAD \_ INFO

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

Tipo: **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Casella trama di origine (vedere [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***

</dd> <dd>

Casella trama di destinazione (vedere [**D3D10 \_ BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello mipmap della trama di origine, vedere [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) per altri dettagli.

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello mipmap della trama di destinazione. Per altre informazioni, vedere [**D3D10CalcSubresource.**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli mipmap nella trama di origine.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Primo elemento della trama di origine.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Primo elemento della trama di destinazione.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di elementi da caricare.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni di filtro durante il ricampionamento (vedere [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opzioni di filtro durante la generazione di livelli mip (vedere [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata in una chiamata a [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
