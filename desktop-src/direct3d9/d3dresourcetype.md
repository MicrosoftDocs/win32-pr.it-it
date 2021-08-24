---
description: Definisce i tipi di risorse.
ms.assetid: 6b360fb1-4a5a-47a2-bef9-d8234770bf0c
title: Enumerazione D3DRESOURCETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 672fc09f8b35c22711517950e2589bb0ea68232d8243a370c8aae4165724b5a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750711"
---
# <a name="d3dresourcetype-enumeration"></a>Enumerazione D3DRESOURCETYPE

Definisce i tipi di risorse.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DRESOURCETYPE { 
  D3DRTYPE_SURFACE        = 1,
  D3DRTYPE_VOLUME         = 2,
  D3DRTYPE_TEXTURE        = 3,
  D3DRTYPE_VOLUMETEXTURE  = 4,
  D3DRTYPE_CUBETEXTURE    = 5,
  D3DRTYPE_VERTEXBUFFER   = 6,
  D3DRTYPE_INDEXBUFFER    = 7,
  D3DRTYPE_FORCE_DWORD    = 0x7fffffff
} D3DRESOURCETYPE, *LPD3DRESOURCETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**SUPERFICIE D3DRTYPE \_**
</dt> <dd>

Risorsa Surface.

</dd> <dt>

<span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE \_ VOLUME**
</dt> <dd>

Risorsa volume.

</dd> <dt>

<span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**TRAMA D3DRTYPE \_**
</dt> <dd>

Risorsa trama.

</dd> <dt>

<span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE \_ VOLUMETEXTURE**
</dt> <dd>

Risorsa trama del volume.

</dd> <dt>

<span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE \_ CUBETEXTURE**
</dt> <dd>

Risorsa trama cubo.

</dd> <dt>

<span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE \_ VERTEXBUFFER**
</dt> <dd>

Risorsa vertex buffer.

</dd> <dt>

<span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE \_ INDEXBUFFER**
</dt> <dd>

Risorsa buffer dell'indice.

</dd> <dt>

<span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DResource9::GetType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype)
</dt> </dl>

 

 
