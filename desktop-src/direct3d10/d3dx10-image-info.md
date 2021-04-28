---
description: 'D3DX10_IMAGE_INFO struttura : restituisce una descrizione del contenuto originale di un file di immagine.'
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO struttura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 228ddf777217e9e61369b0a7fc3b3eb1ca012b1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105479"
---
# <a name="d3dx10_image_info-structure"></a>Struttura D3DX10 \_ IMAGE \_ INFO

Restituisce una descrizione del contenuto originale di un file di immagine.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza dell'immagine originale in pixel.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza dell'immagine originale in pixel.

</dd> <dt>

**Livello nidificazione**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Profondità dell'immagine originale in pixel.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni della matrice di trame. *ArraySize* sarà 1 per una singola immagine.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli mipmap nell'immagine originale.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Proprietà delle risorse varie (vedere [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **FORMATO \_ DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Valore del tipo [**enumerato DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) che descrive più da vicino i dati nell'immagine originale.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **DIMENSIONE RISORSA \_ \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Rappresenta il tipo della trama archiviata nel file. Vedere [**D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md)**

</dd> <dd>

Rappresenta il formato del file di immagine. Vedere [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
