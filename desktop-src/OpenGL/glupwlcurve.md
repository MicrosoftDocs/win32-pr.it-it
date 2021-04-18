---
title: funzione gluPwlCurve (Glu. h)
description: La funzione gluPwlCurve descrive una curva di taglio a tratti lineare non uniforme (NURBS, B-spline).
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- funzione gluPwlCurve OpenGL
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
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302106"
---
# <a name="glupwlcurve-function"></a>gluPwlCurve (funzione)

La funzione **gluPwlCurve** descrive una curva di taglio A tratti lineare non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md), B-spline).

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

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*count* 
</dt> <dd>

Numero di punti sulla curva.

</dd> <dt>

*array* 
</dt> <dd>

Matrice contenente i punti della curva.

</dd> <dt>

*stride* 
</dt> <dd>

Offset (un numero di valori a virgola mobile e precisione singola) tra i punti sulla curva.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di curva. Deve essere GLU \_ Mappa1 \_ Trim \_ 2 o Glu \_ Mappa1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluPwlCurve** descrive una curva di trimming lineare a tratti per una superficie NURBS. Una curva lineare a tratti è costituita da un elenco di coordinate dei punti nello spazio dei parametri per la superficie NURBS da tagliare. Questi punti sono connessi con segmenti di linea per formare una curva. Se la curva è un'approssimazione a una curva reale, è necessario che i punti siano sufficientemente vicini che il tracciato risultante appaia curvo in corrispondenza della risoluzione utilizzata nell'applicazione.

Se *Type* è Glu \_ Mappa1 \_ Trim \_ 2, descrive una curva nello spazio di parametri bidimensionali (*u* e *v*). Se è GLU \_ Mappa1 \_ Trim \_ 3, descrive una curva in uno spazio di parametri omogeneo (*u*, *v* e *w*) bidimensionale. Per ulteriori informazioni sulle curve di trimming, vedere [**gluBeginTrim**](glubegintrim.md).

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
</dt> </dl>

 

 





