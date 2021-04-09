---
title: funzione gluNurbsSurface (Glu. h)
description: La funzione gluNurbsSurface definisce la forma di una superficie NURBS (B-spline) razionale non uniforme.
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- funzione gluNurbsSurface OpenGL
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
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963734"
---
# <a name="glunurbssurface-function"></a>gluNurbsSurface (funzione)

La funzione **gluNurbsSurface** definisce la forma di una superficie [NURBS](using-nurbs-curves-and-surfaces.md)(B-spline) razionale non uniforme.

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

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*\_conteggio sknot* 
</dt> <dd>

Numero di nodi nella direzione di *u* parametrica.

</dd> <dt>

*sknot* 
</dt> <dd>

Una matrice di *sknot \_ count* nondecreasing Knot values nella direzione parametrica *u* .

</dd> <dt>

*\_conteggio tknot* 
</dt> <dd>

Numero di nodi nella direzione della *v* parametrica.

</dd> <dt>

*tknot* 
</dt> <dd>

Una matrice di *tknot \_ count* nondecreasing Knot values nella direzione parametrica *v* .

</dd> <dt>

*\_stride s* 
</dt> <dd>

Offset (sotto forma di numero di singoli valori del punto di precisionfloating) tra punti di controllo successivi nella direzione *u* parametrica in *ctlarray*.

</dd> <dt>

*t \_ stride* 
</dt> <dd>

Offset (nei singoli valori del punto di precisionfloating) tra i punti di controllo successivi nella direzione parametrica *v* in *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Matrice contenente i punti di controllo per la superficie NURBS. Gli offset tra i punti di controllo successivi nelle direzioni parametriche *u* e *v* sono forniti da *s \_ stride* e *t \_ stride*.

</dd> <dt>

*sorder* 
</dt> <dd>

Ordine della superficie NURBS nella direzione di *u* parametrica. L'ordine è uno più del grado, quindi una superficie cubica in *u* ha un ordine *u* di 4.

</dd> <dt>

*torder* 
</dt> <dd>

Ordine della superficie NURBS nella direzione della *v* parametrica. L'ordine è uno più del grado, quindi una superficie cubica in *v* ha un ordine *v* pari a 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo della superficie. Il parametro di *tipo* può essere qualsiasi tipo di analizzatore bidimensionale valido, ad esempio GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Color \_ 4.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare **gluNurbsSurface** all'interno di una definizione di superficie NURBS per descrivere la forma di una superficie NURBS (prima di qualsiasi taglio). Per contrassegnare l'inizio di una definizione di superficie NURBS, utilizzare la funzione [**gluBeginSurface**](glubeginsurface.md) . Per contrassegnare la fine di una definizione di superficie NURBS, utilizzare la funzione [**gluEndSurface**](gluendsurface.md) . Chiamare **gluNurbsSurface** solo all'interno di una definizione di superficie NURBS.

Si associano le coordinate posizionali, di trama e di colore a una superficie presentando ognuno come **gluNurbsSurface** separato tra una coppia di  / **gluEndSurface** gluBeginSurface. All'interno di una singola coppia **gluBeginSurface** / **gluEndSurface** , è possibile effettuare una sola chiamata a **gluNurbsSurface** per i dati di colore, posizione e trama. Eseguire esattamente una chiamata per descrivere la posizione della superficie (un *tipo* di GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Vertex \_ 4).

È possibile tagliare una superficie NURBS usando le funzioni [**gluNurbsCurve**](glunurbscurve.md) e [**gluPwlCurve**](glupwlcurve.md) tra le chiamate a [**gluBeginTrim**](glubegintrim.md) e [**gluEndTrim**](gluendtrim.md).

Un **gluNurbsSurface** con *sknot \_ numero* di nodi nella direzione *u* e i nodi *\_ conteggio tknot* nella direzione *v* con Orders *sorder* e *torder* devono avere (*sknot \_ count*  - *sorder*) multipied by (*tknot \_ count*  - *torder*) punti di controllo.

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

 

 





