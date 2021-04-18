---
title: funzione gluNurbsCurve (Glu. h)
description: La funzione gluNurbsCurve definisce la forma di una curva B-spline (NURBS) razionale non uniforme.
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- funzione gluNurbsCurve OpenGL
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
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301354"
---
# <a name="glunurbscurve-function"></a>gluNurbsCurve (funzione)

La funzione **gluNurbsCurve** definisce la forma di una curva B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.

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

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

Numero di nodi nel *nodo*. Il parametro *nknots* è uguale al numero di punti di controllo più l'ordine.

</dd> <dt>

*forma* 
</dt> <dd>

Matrice di valori dei nodi nondecreasing di *nknots* .

</dd> <dt>

*stride* 
</dt> <dd>

Offset (come numero di valori a virgola mobile e precisione singola) tra i punti di controllo della curva successiva.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Puntatore a una matrice di punti di controllo. Le coordinate devono accettare il *tipo*.

</dd> <dt>

*order* 
</dt> <dd>

Ordine della curva NURBS. Il parametro *Order* è uguale al grado + 1; di conseguenza, una curva cubica ha un ordine di 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo della curva. Se questa curva è definita all'interno di una coppia [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , il tipo può essere uno qualsiasi dei tipi di analizzatore unidimensionali validi, ad esempio GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Color \_ 4. Tra una coppia [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , gli unici tipi validi sono Glu \_ Mappa1 \_ Trim \_ 2 e Glu \_ Mappa1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando **gluNurbsCurve** viene visualizzato tra una coppia **gluBeginCurve** / **gluEndCurve** , descrive una curva di cui eseguire il rendering. Si associano le coordinate posizionali, di trama e di colore presentando ciascuna come **gluNurbsCurve** distinta tra una coppia **gluBeginCurve** / **gluEndCurve** . Non eseguire più di una chiamata a **gluNurbsCurve** per i dati di colore, posizione e trama all'interno di una singola coppia di  / **gluEndCurve** gluBeginCurve. Eseguire esattamente una chiamata per descrivere la posizione della curva (un *tipo* di GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Vertex \_ 4).

Quando **gluNurbsCurve** viene visualizzato tra una coppia [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , descrive una curva di trimming su una superficie NURBS. Se *Type* è Glu \_ Mappa1 \_ Trim \_ 2, descrive una curva nello spazio di parametri bidimensionali (*u* e *v*). Se è GLU \_ Mappa1 \_ Trim \_ 3, descrive una curva in uno spazio di parametri omogeneo (*u*, *v* e *w*) bidimensionale. Per ulteriori informazioni sulle curve di trimming, vedere **gluBeginTrim**.

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
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





