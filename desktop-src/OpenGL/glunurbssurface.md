---
title: Funzione gluNurbsSurface (Glu.h)
description: La funzione gluNurbsSurface definisce la forma di una superficie B-Spline razionale non uniforme (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- Funzione gluNurbsSurface OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f56232ac891cbdfba18195741d875ecc5436112772ed4fa665903374e96602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554191"
---
# <a name="glunurbssurface-function"></a>Funzione gluNurbsSurface

La **funzione gluNurbsSurface** definisce la forma di una superficie B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*conteggio sknot \_* 
</dt> <dd>

Numero di nodi nella direzione *parametrica u.*

</dd> <dt>

*sknot* 
</dt> <dd>

Matrice di *sknot \_ count* che non crea valori di nodi nella direzione *u parametrica.*

</dd> <dt>

*tknot \_ count* 
</dt> <dd>

Numero di nodi nella direzione *parametrica v.*

</dd> <dt>

*tknot* 
</dt> <dd>

Matrice di *valori tknot \_ count* nondecreasing dei nodi nella direzione *parametrica v.*

</dd> <dt>

*s \_ stride* 
</dt> <dd>

Offset (come numero di singoli valori precisionfloating-point) tra i punti di controllo successivi nella direzione *u* parametrica in *ctlarray*.

</dd> <dt>

*t \_ stride* 
</dt> <dd>

Offset (in valori a precisione singola del punto di flessione) tra i punti di controllo successivi nella direzione *parametrica v* in *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Matrice contenente i punti di controllo per la superficie NURBS. Gli offset tra i punti di controllo successivi nelle direzioni *parametrica u* *e v* sono specificati da *s \_ stride* e *t \_ stride*.

</dd> <dt>

*sorder* 
</dt> <dd>

Ordine della superficie NURBS nella direzione *u* parametrica. L'ordine è superiore al grado, quindi una superficie cubica in *u* ha un *ordine u* di 4.

</dd> <dt>

*torder* 
</dt> <dd>

Ordine della superficie NURBS nella direzione *parametrica v.* L'ordine è superiore al grado, quindi una superficie cubica in *v* ha un ordine *v* di 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo della superficie. Il *parametro* di tipo può essere uno dei tipi di analizzatore bidimensionali validi, ad esempio GL \_ MAP2 \_ VERTEX \_ 3 o GL \_ MAP2 COLOR \_ \_ 4.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluNurbsSurface all'interno** di una definizione di superficie NURBS per descrivere la forma di una superficie NURBS (prima di qualsiasi taglio). Per contrassegnare l'inizio di una definizione di superficie NURBS, usare la [**funzione gluBeginSurface.**](glubeginsurface.md) Per contrassegnare la fine di una definizione di superficie NURBS, usare la [**funzione gluEndSurface.**](gluendsurface.md) Chiamare **gluNurbsSurface solo all'interno** di una definizione di superficie NURBS.

È possibile associare coordinate posizionali, trame e colori a una superficie presentando ognuna come **gluNurbsSurface** separata tra una coppia **gluBeginSurface** / **gluEndSurface.** All'interno di una singola coppia **gluBeginSurface** gluEndSurface, è possibile effettuare una sola chiamata a /  **gluNurbsSurface** per i dati di colore, posizione e trama. Effettuare esattamente una chiamata per descrivere la posizione della superficie *(tipo* GL \_ MAP2 \_ VERTEX \_ 3 o GL \_ MAP2 \_ VERTEX \_ 4).

È possibile tagliare una superficie NURBS usando le funzioni [**gluNurbsCurve**](glunurbscurve.md) e [**gluPwlCurve**](glupwlcurve.md) tra le chiamate a [**gluBeginTrim**](glubegintrim.md) [**e gluEndTrim**](gluendtrim.md).

Un **gluNurbsSurface** con *sknot \_ count* nodi nella direzione *u* e *tknot \_* count nodi nella direzione *v* con ordini *sorder* e *torder* deve avere (*sknot \_ count*  - *sorder*) multipied by (*tknot \_ count*  - *torder*) punti di controllo.

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





