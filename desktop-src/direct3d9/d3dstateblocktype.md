---
description: Set predefiniti di stato della pipeline usati dai blocchi di stato (vedere State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumerazione D3DSTATEBLOCKTYPE (D3D9Types.h)
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
ms.openlocfilehash: 7780b7ded37ba976f32f4439ab793ae711be2f5790d03555a6a8be4f031571e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850187"
---
# <a name="d3dstateblocktype-enumeration"></a>Enumerazione D3DSTATEBLOCKTYPE

Set predefiniti di stato della pipeline usati dai blocchi di stato (vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)(Salvataggio e ripristino dello stato dei blocchi di stato (Direct3D 9) ).

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

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ ALL**
</dt> <dd>

Acquisire lo stato [corrente del dispositivo](saving-all-device-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

Acquisisci lo stato [pixel corrente.](saving-pixel-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

Acquisire lo stato [del vertice corrente.](saving-vertex-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Non usare questo valore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Come illustrato nel diagramma seguente, lo stato dei vertici e dei pixel è entrambi subset dello stato del dispositivo.

![diagramma dello stato del dispositivo, con stato vertice e stato pixel come subset](images/statesets.png)

Esistono solo alcuni stati considerati sia stato vertice che stato pixel. Questi stati sono:

-   Stato di rendering: \_ D3DRSDENSITY
-   Stato di rendering: \_ D3DRSBIESTART
-   Stato di rendering: \_ D3DRSBIEEND
-   Stato trama: D3DTSS \_ TEXCOORDINDEX
-   Stato trama: \_ TEXTURETRANSFORMFLAGS D3DTSS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
