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
ms.openlocfilehash: bf3aa2eeb3e908a76e05588940927fff53dd1583c937d95a1c862f6021bd630f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989521"
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

Proprietà varie delle risorse (vedere [**D3D10 \_ RESOURCE \_ MISC \_ FLAG).**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)

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

Rappresenta il formato del file di immagine. Vedere FORMATO DEL FILE DI IMMAGINE [**D3DX10 \_ \_ \_**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
