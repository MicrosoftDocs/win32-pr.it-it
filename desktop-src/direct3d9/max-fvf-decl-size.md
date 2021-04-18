---
description: Questa costante è il numero massimo di dichiaratori di vertici per una mesh.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Enumerazione MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322526"
---
# <a name="max_fvf_decl_size-enumeration"></a>\_Enumerazione max FVF \_ decl \_ size

Questa costante è il numero massimo di dichiaratori di vertici per una mesh.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**dimensioni MASSIMe \_ \_ decl FVF \_**
</dt> <dd>

Numero massimo di elementi nella dichiarazione del vertice. Il (+ 1) aggiuntivo è per [**D3DDECL \_ end**](d3ddecl-end.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

MAXD3DDECLLENGTH è definito come massimo 64 (vedere d3d9types. h). Non include l'elemento del vertice del marcatore "end".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**GetDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
