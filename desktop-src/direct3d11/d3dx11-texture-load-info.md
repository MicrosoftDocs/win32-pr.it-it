---
title: D3DX11_TEXTURE_LOAD_INFO struttura (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Descrive i parametri usati per caricare una trama da un'altra trama.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO struttura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b441ed81e7054cb84731f204ddbf2a863b7a98a75e5e01ed54cf49b28dba7957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989901"
---
# <a name="d3dx11_texture_load_info-structure"></a>Struttura D3DX11 \_ TEXTURE \_ LOAD \_ INFO

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.

 

Descrive i parametri usati per caricare una trama da un'altra trama.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**pSrcBox**
</dt> <dd>

Tipo: **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Casella trama di origine (vedere [**D3D11 \_ BOX).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **D3D11 \_ BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Casella trama di destinazione (vedere [**D3D11 \_ BOX).**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Livello mipmap della trama di origine. Per altri dettagli, vedere [**D3D11CalcSubresource.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource)

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Livello mipmap della trama di destinazione. Per altri dettagli, vedere [**D3D11CalcSubresource.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource)

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di livelli mipmap nella trama di origine.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primo elemento della trama di origine.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primo elemento della trama di destinazione.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi da caricare.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opzioni di filtro durante il ricampionamento (vedere [**D3DX11 \_ FILTER \_ FLAG).**](d3dx11-filter-flag.md)

</dd> <dt>

**Filtro mip**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opzioni di filtro durante la generazione di livelli mip (vedere [**D3DX11 \_ FILTER \_ FLAG).**](d3dx11-filter-flag.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata in una chiamata a [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).

I valori predefiniti sono:


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

