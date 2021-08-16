---
title: Funzione gluPwlCurve (Glu.h)
description: La funzione gluPwlCurve descrive una curva di taglio NURBS (Non-Uniform Rational B-Spline) lineare a punti.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- Funzione gluPwlCurve OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9911619e54247c633d4b3cecc69327f92da6a7f27c3cebf9231ec86ad0f0a20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061569"
---
# <a name="glupwlcurve-function"></a>Funzione gluPwlCurve

La **funzione gluPwlCurve** descrive una curva di taglio non uniforme B-Spline razionale non uniforme [(NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*count* 
</dt> <dd>

Numero di punti sulla curva.

</dd> <dt>

*array* 
</dt> <dd>

Matrice contenente i punti della curva.

</dd> <dt>

*Passo* 
</dt> <dd>

Offset (numero di valori a virgola mobile e precisione singola) tra i punti della curva.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di curva. Deve essere GLU \_ MAP1 \_ TRIM \_ 2 o GLU \_ MAP1 \_ TRIM \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluPwlCurve** descrive una curva di taglio lineare a un punto per una superficie NURBS. Una curva lineare a un punto è costituita da un elenco di coordinate di punti nello spazio dei parametri per la superficie NURBS da tagliare. Questi punti sono collegati a segmenti di linea per formare una curva. Se la curva è un'approssimazione a una curva reale, i punti devono essere abbastanza vicini che il percorso risultante appare curvo alla risoluzione usata nell'applicazione.

Se *type* è GLU MAP1 TRIM 2, descrive una curva nello spazio dei parametri \_ \_ \_ bidimensionale (*u* *e v*). Se è GLU MAP1 TRIM 3, descrive una curva nello spazio dei parametri \_ \_ omogeneo \_ bidimensionale (*u*, *v* e *w*). Per altre informazioni sul trimming delle curve, vedere [**gluBeginTrim.**](glubegintrim.md)

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
</dt> </dl>

 

 





