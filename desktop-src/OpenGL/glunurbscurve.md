---
title: Funzione gluNurbsCurve (Glu.h)
description: La funzione gluNurbsCurve definisce la forma di una curva B-Spline razionale non uniforme (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- Funzione gluNurbsCurve OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5973ce3cb4d1ac05ea353fd78359f6b3b1bc9a3a0ab3180807b0834cc4bb20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489041"
---
# <a name="glunurbscurve-function"></a>Funzione gluNurbsCurve

La **funzione gluNurbsCurve** definisce la forma di una curva B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

Numero di nodi in *nodo*. Il *parametro nknots* è uguale al numero di punti di controllo più l'ordine.

</dd> <dt>

*Nodo* 
</dt> <dd>

Matrice di *nknots* che non crea valori di nodo.

</dd> <dt>

*Passo* 
</dt> <dd>

Offset (come numero di valori a virgola mobile a precisione singola) tra i punti di controllo della curva successivi.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Puntatore a una matrice di punti di controllo. Le coordinate devono essere d'accordo *con il tipo*.

</dd> <dt>

*order* 
</dt> <dd>

Ordine della curva NURBS. Il *parametro order* è uguale a degree + 1; di conseguenza una curva cubica ha un ordine di 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo della curva. Se questa curva è definita all'interno di una coppia [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve,**](gluendcurve.md) il tipo può essere uno dei tipi di analizzatore unidimensionali validi (ad esempio GL \_ MAP1 \_ VERTEX 3 o \_ GL \_ MAP1 COLOR \_ \_ 4). Tra una [**coppia gluBeginTrim**](glubegintrim.md)gluEndTrim, gli unici tipi validi / [](gluendtrim.md) sono GLU \_ MAP1 \_ TRIM \_ 2 e GLU \_ MAP1 TRIM \_ \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando **gluNurbsCurve** viene visualizzato tra una coppia **gluBeginCurve** / **gluEndCurve,** descrive una curva di cui eseguire il rendering. È possibile associare coordinate posizionali, trame e colori presentando ognuna come **gluNurbsCurve** separata tra una coppia **gluBeginCurve** / **gluEndCurve.** Non effettuare più chiamate a **gluNurbsCurve** per i dati di colore, posizione e trama all'interno di una singola coppia **gluBeginCurve** / **gluEndCurve.** Effettuare esattamente una chiamata per descrivere la posizione della curva *(tipo* GL \_ MAP1 \_ VERTEX \_ 3 o GL \_ MAP1 \_ VERTEX \_ 4).

Quando **gluNurbsCurve** viene visualizzato tra una coppia [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim,**](gluendtrim.md) descrive una curva di taglio su una superficie NURBS. Se *type* è GLU MAP1 TRIM 2, descrive una curva nello spazio dei parametri \_ \_ \_ bidimensionale (*u* *e v).* Se è GLU \_ MAP1 TRIM 3, descrive una curva nello spazio dei parametri omogeneo \_ bidimensionale ( \_ *u*, *v* e *w*). Per altre informazioni sul trimming delle curve, **vedere gluBeginTrim**.

## <a name="examples"></a>Esempio

Le funzioni seguenti eseguono il rendering di una curva NURBS con trama con normali:

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
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

[**gluEndCurve**](gluendcurve.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





