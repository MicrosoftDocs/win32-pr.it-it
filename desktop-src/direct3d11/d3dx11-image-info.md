---
title: D3DX11_IMAGE_INFO struttura (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Facoltativamente, fornire informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. | D3DX11_IMAGE_INFO struttura (D3DX11tex.h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO struttura Direct3D 11
- LPD3DX11_IMAGE_INFO puntatore alla struttura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64366755e9bb9398e8107d931ee5425d2fcee78fdd9d03487b9533270cc17c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536868"
---
# <a name="d3dx11_image_info-structure"></a>Struttura D3DX11 \_ IMAGE \_ INFO

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Facoltativamente, fornire informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. Il valore D3DX11 DEFAULT per uno di questi parametri determina l'uso automatico del valore del file di origine da parte di \_ D3DX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Larghezza di destinazione della trama. Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Altezza di destinazione della trama. Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondità della trama. Questo vale solo per le trame di volume.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi nella matrice.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero massimo di livelli mipmap nella trama. Vedere le osservazioni in [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Se si usa 0 o D3DX11 DEFAULT, verrà creata una catena \_ mipmap completa.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Proprietà di risorse varie specificate con un flag [**D3D11 \_ RESOURCE \_ MISC \_ FLAG.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Enumerazione [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) che specifica il formato in cui si trova la trama dopo il caricamento.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **DIMENSIONE RISORSA \_ \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Valore [**D3D11 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) che identifica il tipo di risorsa.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ FILE \_ FORMAT**](d3dx11-image-file-format.md)**

</dd> <dd>

Valore [**D3DX11 \_ IMAGE FILE \_ \_ FORMAT**](d3dx11-image-file-format.md) che identifica il formato dell'immagine.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata da metodi come [**D3DX11GetImageInfoFromFile,**](d3dx11getimageinfofromfile.md) [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource.**](d3dx11getimageinfofromresource.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

