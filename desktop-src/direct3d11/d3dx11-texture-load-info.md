---
title: Struttura D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Descrive i parametri usati per caricare una trama da un'altra trama.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- Struttura D3DX11_TEXTURE_LOAD_INFO Direct3D 11
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
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996059"
---
# <a name="d3dx11_texture_load_info-structure"></a>\_Struttura delle \_ informazioni di caricamento della trama D3DX11 \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

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

Tipo: **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Casella trama di origine (vedere [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**pDstBox**
</dt> <dd>

Tipo: **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***

</dd> <dd>

Casella trama di destinazione (vedere [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).

</dd> <dt>

**SrcFirstMip**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Livello di mipmap trama di origine. per altre informazioni, vedere [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .

</dd> <dt>

**DstFirstMip**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Livello di mipmap della trama di destinazione. per altre informazioni, vedere [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .

</dd> <dt>

**NumMips**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di livelli di mipmap nella trama di origine.

</dd> <dt>

**SrcFirstElement**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primo elemento della trama di origine.

</dd> <dt>

**DstFirstElement**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Primo elemento della trama di destinazione.

</dd> <dt>

**NumElements**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi da caricare.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opzioni di filtro durante il ricampionamento (vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md)).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Opzioni di filtro durante la generazione di livelli MIP (vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md)).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata in una chiamata a [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).

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
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

