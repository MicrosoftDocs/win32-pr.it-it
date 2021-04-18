---
title: funzione gluEndSurface (Glu. h)
description: Le funzioni gluBeginSurface e gluEndSurface delimitano una definizione di superficie B-spline (NURBS) razionale non uniforme. | funzione gluEndSurface (Glu. h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- funzione gluEndSurface OpenGL
topic_type:
- apiref
api_name:
- gluEndSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54631d5c4ef752cffd989f8fa02f8cb512c67da3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530720"
---
# <a name="gluendsurface-function"></a>gluEndSurface (funzione)

Le funzioni [**gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** delimitano una definizione di superficie B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluEndSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le funzioni [**gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** contrassegnano l'inizio e la fine delle definizioni della superficie NURBS, definite con le chiamate a **gluNurbsSurface**.

1.  Chiamare **gluBeginSurface** per contrassegnare l'inizio di una definizione di superficie NURBS.
2.  Eseguire una o più chiamate a **gluNurbsSurface** per definire gli attributi della superficie.

    Una di queste chiamate a **gluNurbsSurface** deve avere un tipo di superficie di GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Vertex \_ 4.

3.  Per contrassegnare la fine della definizione della superficie NURBS, chiamare **gluEndSurface**.

Le funzioni [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e **gluEndTrim** supportano il taglio di superfici NURBS.

Usare gli analizzatori OpenGL per eseguire il rendering della superficie NURBS come un set di poligoni. Mantenere lo stato dell'analizzatore durante il rendering con [**glPushAttrib**](glpushattrib.md) (bit valutazione GL \_ \_ ) e [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Esempio

Le funzioni seguenti eseguono il rendering di una superficie NURBS con trama con normali; le coordinate di trama e le normali sono descritte anche come superfici NURBS:

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluNurbsSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





