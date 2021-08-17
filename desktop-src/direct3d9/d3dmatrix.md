---
description: Descrive una matrice.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ee4c67a4a743d3bff1cfc5ca88b6691e995f78a9fb01fe36aabc4ae6aca66e6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732366"
---
# <a name="d3dmatrix"></a>D3DMATRIX

Descrive una matrice.

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

Tipi derivati: \* LPD3DMATRIX

## <a name="members"></a>Membri



| Elemento                                                        | Descrizione                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_ij"></span><span id="_IJ"></span>\_Ij<br/> | Matrice di valori float che rappresentano una matrice 4x4, dove i è il numero di riga e j è il numero di colonna. Ad esempio, 34 indica lo stesso ₃₄ , il componente \_ nella terza riga e nella quarta \[ \] colonna.<br/> |



 

## <a name="remarks"></a>Commenti

In Direct3D \_ l'elemento 34 di una matrice di proiezione non può essere un numero negativo. Se l'applicazione deve usare un valore negativo in questa posizione, deve invece ridimensionare l'intera matrice di proiezione di -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**Multiplytransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

**SetTransform**
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> <dt>

[Trasformazioni (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
