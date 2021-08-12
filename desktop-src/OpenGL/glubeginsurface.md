---
title: Funzione gluBeginSurface (Glu.h)
description: Le funzioni gluBeginSurface e gluEndSurface delimitano una definizione di superficie NURBS (Non-Uniform Rational B-Spline). | Funzione gluBeginSurface (Glu.h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- Funzione gluBeginSurface OpenGL
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
ms.openlocfilehash: 3398561b3587c5cceda0e31906c20a0163c0d249092745fe3a404e5c5c6a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613046"
---
# <a name="glubeginsurface-function"></a>Funzione gluBeginSurface

Le **funzioni gluBeginSurface** e [**gluEndSurface**](gluendsurface.md) delimitano una definizione di superficie B-Spline razionale non uniforme [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le **funzioni gluBeginSurface** e **gluEndSurface** contrassegnano l'inizio e la fine delle definizioni di superficie NURBS, definite con chiamate a **gluNurbsSurface.**

1.  Chiamare **gluBeginSurface per** contrassegnare l'inizio di una definizione di superficie NURBS.
2.  Effettuare una o più chiamate a **gluNurbsSurface** per definire gli attributi della superficie.

    Esattamente una di queste chiamate a **gluNurbsSurface** deve avere un tipo di superficie GL \_ MAP2 \_ VERTEX \_ 3 o GL \_ MAP2 \_ VERTEX \_ 4.

3.  Per contrassegnare la fine della definizione della superficie NURBS, chiamare **gluEndSurface.**

Le [**funzioni gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e [**gluEndTrim**](gluendtrim.md) supportano il trimming delle superfici NURBS.

Usare gli analizzatori OpenGL per eseguire il rendering della superficie NURBS come set di poligoni. Mantenere lo stato dell'analizzatore durante il rendering [**con glPushAttrib**](glpushattrib.md)(GL \_ EVAL \_ BIT) e [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Esempio

Le funzioni seguenti eseguono il rendering di una superficie NURBS con trame con normali. Le coordinate e le normali della trama sono descritte anche come superfici NURBS:

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

 

 





