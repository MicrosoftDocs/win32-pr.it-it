---
description: Definisce le informazioni sulla posizione, sulla trama e sul colore di uno sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Struttura D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323382"
---
# <a name="d3dx10_sprite-structure"></a>\_Struttura d3dx10 sprite

Definisce le informazioni sulla posizione, sulla trama e sul colore di uno sprite.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a>Members

<dl> <dt>

**matWorld**
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Trasformazione del mondo del modello dello sprite. Definisce la posizione e l'orientamento dello sprite nello spazio globale.

</dd> <dt>

**TexCoord**
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Offset dall'angolo superiore sinistro della trama che indica dove deve essere avviata l'immagine sprite nella trama. **TexCoord** è nelle coordinate di trama.

</dd> <dt>

**TexSize**
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Vettore che contiene la larghezza e l'altezza dello sprite nelle coordinate di trama.

</dd> <dt>

**ColorModulate**
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Colore che verrà moltiplicato con il colore del pixel prima del rendering.

</dd> <dt>

**pTexture**
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Puntatore a una visualizzazione risorse dello shader che rappresenta la trama dello sprite. Vedere [**interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).

</dd> <dt>

**TextureIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Indice della trama. Se pTexture non rappresenta una matrice di trama, deve essere 0.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
