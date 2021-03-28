---
title: Struttura D3DX11_IMAGE_INFO (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. | Struttura D3DX11_IMAGE_INFO (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- Struttura D3DX11_IMAGE_INFO Direct3D 11
- Puntatore alla struttura LPD3DX11_IMAGE_INFO Direct3D 11
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
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982558"
---
# <a name="d3dx11_image_info-structure"></a>Struttura delle informazioni sull' \_ immagine D3DX11 \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Fornire facoltativamente informazioni alle API del caricatore di trama per controllare la modalità di caricamento delle trame. Il valore predefinito D3DX11 \_ per uno di questi parametri provocherà l'uso automatico del valore del file di origine da parte di D3DX.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Larghezza di destinazione della trama. Se la larghezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa larghezza di destinazione.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Altezza di destinazione della trama. Se l'altezza effettiva della trama è maggiore o minore di questo valore, la trama verrà ridimensionata verso l'alto o verso il basso per adattarla a questa altezza di destinazione.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondità della trama. Questo vale solo per le trame del volume.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero di elementi nella matrice.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Numero massimo di livelli di mipmap nella trama. Vedere la sezione Osservazioni in [**d3d11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Se \_ si usa il valore predefinito 0 o D3DX11, verrà creata una catena mipmap completa.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Proprietà delle risorse varie specificate con un flag di [**\_ \_ \_ flag varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Enumerazione [**del \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) che specifica il formato in cui si troverà la trama dopo il caricamento.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **\_ \_ dimensione della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Valore [**della \_ \_ dimensione della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , che identifica il tipo di risorsa.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**

</dd> <dd>

Valore [**del \_ \_ \_ formato di file di immagine D3DX11**](d3dx11-image-file-format.md) , che identifica il formato dell'immagine.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata da metodi quali: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

