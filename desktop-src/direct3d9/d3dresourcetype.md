---
description: Definisce i tipi di risorse.
ms.assetid: 6b360fb1-4a5a-47a2-bef9-d8234770bf0c
title: Enumerazione D3DRESOURCETYPE (D3D9Types. h)
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
ms.openlocfilehash: 4d7fab861d85a2c0289ba1636dece0e76c7819e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969312"
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
  D3DRTYPE_CubeTexture    = 5,
  D3DRTYPE_VERTEXBUFFER   = 6,
  D3DRTYPE_INDEXBUFFER    = 7,
  D3DRTYPE_FORCE_DWORD    = 0x7fffffff
} D3DRESOURCETYPE, *LPD3DRESOURCETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**\_Superficie D3DRTYPE**
</dt> <dd>

Risorsa superficie.

</dd> <dt>

<span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**\_Volume D3DRTYPE**
</dt> <dd>

Risorsa volume.

</dd> <dt>

<span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**\_Trama D3DRTYPE**
</dt> <dd>

Risorsa trama.

</dd> <dt>

<span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**\_VOLUMETEXTURE D3DRTYPE**
</dt> <dd>

Risorsa trama del volume.

</dd> <dt>

<span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**\_CUBETEXTURE D3DRTYPE**
</dt> <dd>

Risorsa trama cubo.

</dd> <dt>

<span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE \_ VERTEXBUFFER**
</dt> <dd>

Risorsa buffer vertex.

</dd> <dt>

<span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**\_INDEXBUFFER D3DRTYPE**
</dt> <dd>

Risorsa buffer di indice.

</dd> <dt>

<span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DResource9:: GetType**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype)
</dt> </dl>

 

 
