---
description: Restituisce una descrizione del contenuto originale di un file di immagine.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Struttura D3DX10_IMAGE_INFO (D3DX10. h)
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
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354439"
---
# <a name="d3dx10_image_info-structure"></a>Struttura delle informazioni sull' \_ immagine d3dx10 \_

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

**ArraySize**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensioni della matrice di trama. *ArraySize* sarà 1 per una singola immagine.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Numero di livelli di mipmap nell'immagine originale.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Proprietà delle risorse varie ( [**vedere \_ \_ \_ flag varie della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Valore del tipo enumerato del [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) che descrive più accuratamente i dati nell'immagine originale.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **\_ \_ dimensione della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Rappresenta il tipo di trama archiviato nel file. Vedere [**\_ \_ dimensione della risorsa D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**

</dd> <dd>

Rappresenta il formato del file di immagine. Vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
