---
description: Tipi di patch mesh.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Enumerazione D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322112"
---
# <a name="d3dxpatchmeshtype-enumeration"></a>Enumerazione D3DXPATCHMESHTYPE

Tipi di patch mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**
</dt> <dd>

Tipo di mesh patch rettangolo.

</dd> <dt>

<span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**
</dt> <dd>

Tipo mesh patch del triangolo.

</dd> <dt>

<span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**\_NPATCH D3DXPATCHMESH**
</dt> <dd>

N: tipo di mesh della patch.

</dd> <dt>

<span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le patch del triangolo hanno tre lati e sono descritte in [**D3DTRIPATCH \_ info**](d3dtripatch-info.md). Le patch rettangolari sono a quattro lati e sono descritte in [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[Uso di Higher-Order primitive (Direct3D 9)](using-higher-order-primitives.md)
</dt> </dl>

 

 




