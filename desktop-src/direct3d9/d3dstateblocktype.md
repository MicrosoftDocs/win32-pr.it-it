---
description: Set predefiniti di stato della pipeline usato dai blocchi di stato (vedere lo stato di salvataggio e ripristino del blocco di stato (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumerazione D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104562357"
---
# <a name="d3dstateblocktype-enumeration"></a>Enumerazione D3DSTATEBLOCKTYPE

Set predefiniti di stato della pipeline usato dai blocchi di stato (vedere lo stato di [salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ tutto**
</dt> <dd>

Acquisisce lo [stato](saving-all-device-states-with-a-stateblock.md)corrente del dispositivo.

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**\_PIXELSTATE D3DSBT**
</dt> <dd>

Acquisisce lo [stato](saving-pixel-states-with-a-stateblock.md)corrente dei pixel.

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**\_VERTEXSTATE D3DSBT**
</dt> <dd>

Acquisisce lo [stato del vertice](saving-vertex-states-with-a-stateblock.md)corrente.

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Non usare questo valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Come illustrato nel diagramma seguente, lo stato del vertice e del pixel è costituito da entrambi i subset dello stato del dispositivo.

![diagramma dello stato del dispositivo, con stato del vertice e stato del pixel come subset](images/statesets.png)

Esistono solo alcuni Stati che sono considerati lo stato del vertice e del pixel. Questi stati sono:

-   Stato di rendering: D3DRS \_ FOGDENSITY
-   Stato di rendering: D3DRS \_ FOGSTART
-   Stato di rendering: D3DRS \_ FOGEND
-   Stato trama: D3DTSS \_ TEXCOORDINDEX
-   Stato trama: D3DTSS \_ TEXTURETRANSFORMFLAGS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9:: CreateStateBlock**
</dt> </dl>

 

 
