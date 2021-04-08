---
description: Restituisce una descrizione del contenuto originale di un file di immagine.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Struttura D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762035"
---
# <a name="d3dximage_info-structure"></a>Struttura delle informazioni di D3DXIMAGE \_

Restituisce una descrizione del contenuto originale di un file di immagine.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza dell'immagine originale in pixel.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza dell'immagine originale in pixel.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondità dell'immagine originale in pixel.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli MIP nell'immagine originale.

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Valore del tipo enumerato [D3DFORMAT](d3dformat.md) che descrive più accuratamente i dati nell'immagine originale.

</dd> <dt>

**ResourceType**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Rappresenta il tipo di trama archiviato nel file. Si tratta di una \_ trama D3DRTYPE, D3DRTYPE \_ VOLUMETEXTURE o D3DRTYPE \_ CubeTexture.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**

</dd> <dd>

Rappresenta il formato del file di immagine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
