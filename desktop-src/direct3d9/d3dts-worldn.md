---
description: Identifica le matrici di trasformazione successive che possono essere utilizzate per fondere i vertici utilizzando la matrice corrispondente e un valore di peso di Blend (beta) specificato in formato vertice.
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: D3DTS_WORLDn (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 004435d278538c788e21ed7dc3482fd5e248895b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322300"
---
# <a name="d3dts_worldn"></a>D3DTS \_ mondo

Identifica le matrici di trasformazione successive che possono essere utilizzate per fondere i vertici utilizzando la matrice corrispondente e un valore di peso di Blend (beta) specificato in formato vertice.

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a>Commenti

Queste macro vengono fornite per semplificare il porting delle applicazioni esistenti a Direct3D 9.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**\_WORLDMATRIX D3DTS**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
