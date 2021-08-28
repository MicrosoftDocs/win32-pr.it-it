---
title: Funzione gluEndSurface (Glu.h)
description: Le funzioni gluBeginSurface e gluEndSurface delimitano una definizione di superficie B-Spline razionale non uniforme (NURBS). | Funzione gluEndSurface (Glu.h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- Funzione gluEndSurface OpenGL
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
ms.openlocfilehash: 32c8fb5165be78032429dce7957cd0975753515d55969b04415c61be2a7dc5ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675371"
---
# <a name="gluendsurface-function"></a>Funzione gluEndSurface

Le [**funzioni gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** delimitano una definizione di superficie B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluEndSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le [**funzioni gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** contrassegnano l'inizio e la fine delle definizioni di superficie NURBS, definite con chiamate a **gluNurbsSurface.**

1.  Chiamare **gluBeginSurface per** contrassegnare l'inizio di una definizione di superficie NURBS.
2.  Effettuare una o più chiamate a **gluNurbsSurface per** definire gli attributi della superficie.

    Esattamente una di queste chiamate a **gluNurbsSurface** deve avere un tipo di superficie GL \_ MAP2 \_ VERTEX \_ 3 o GL \_ MAP2 \_ VERTEX \_ 4.

3.  Per contrassegnare la fine della definizione della superficie NURBS, chiamare **gluEndSurface**.

Le [**funzioni gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e **gluEndTrim** supportano il trimming delle superfici NURBS.

Usare gli analizzatori OpenGL per eseguire il rendering della superficie NURBS come set di poligoni. Mantenere lo stato dell'analizzatore durante il rendering con [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) e [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Esempio

Le funzioni seguenti eseguono il rendering di una superficie NURBS con trama con normali. Le coordinate e le normali della trama sono descritte anche come superfici NURBS:

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
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





