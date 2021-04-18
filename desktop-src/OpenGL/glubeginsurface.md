---
title: funzione gluBeginSurface (Glu. h)
description: Le funzioni gluBeginSurface e gluEndSurface delimitano una definizione di superficie B-spline (NURBS) razionale non uniforme. | funzione gluBeginSurface (Glu. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- funzione gluBeginSurface OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321401"
---
# <a name="glubeginsurface-function"></a>gluBeginSurface (funzione)

Le funzioni **gluBeginSurface** e [**gluEndSurface**](gluendsurface.md) delimitano una definizione di superficie B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluBeginSurface(
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

Le funzioni **gluBeginSurface** e **gluEndSurface** contrassegnano l'inizio e la fine delle definizioni della superficie NURBS, definite con le chiamate a **gluNurbsSurface**.

1.  Chiamare **gluBeginSurface** per contrassegnare l'inizio di una definizione di superficie NURBS.
2.  Eseguire una o più chiamate a **gluNurbsSurface** per definire gli attributi della superficie.

    Una di queste chiamate a **gluNurbsSurface** deve avere un tipo di superficie di GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Vertex \_ 4.

3.  Per contrassegnare la fine della definizione della superficie NURBS, chiamare **gluEndSurface**.

Le funzioni [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e [**gluEndTrim**](gluendtrim.md) supportano il taglio di superfici NURBS.

Usare gli analizzatori OpenGL per eseguire il rendering della superficie NURBS come un set di poligoni. Mantenere lo stato dell'analizzatore durante il rendering con [**glPushAttrib**](glpushattrib.md)(bit valutazione GL \_ \_ ) e [**glPopAttrib**](glpopattrib.md).

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

 

 





