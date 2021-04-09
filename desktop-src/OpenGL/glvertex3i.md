---
title: funzione glVertex3i (GL. h)
description: Specifica un vertice. | funzione glVertex3i (GL. h)
ms.assetid: 5f757065-cbe9-401a-855b-f0a9308ae204
keywords:
- funzione glVertex3i OpenGL
topic_type:
- apiref
api_name:
- glVertex3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e216c35a354daead228d6043d2129f6d30d400
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969096"
---
# <a name="glvertex3i-function"></a>glVertex3i (funzione)

Specifica un vertice.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glVertex3i(
   GLint x,
   GLint y,
   GLint z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Specifica la coordinata x di un vertice.

</dd> <dt>

*y* 
</dt> <dd>

Specifica la coordinata y di un vertice.

</dd> <dt>

*z* 
</dt> <dd>

Specifica la coordinata z di un vertice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

I comandi della funzione glVertex vengono usati all'interno delle coppie [**glBegin**](glbegin.md) / [**glEnd**](glend.md) per specificare i vertici punto, linea e poligono. Le coordinate di colore, normali e di trama correnti sono associate al vertice quando viene chiamato glVertex. Quando si specificano solo *x* e *y* , il valore predefinito per *z* è 0,0 e *w* viene impostato su 1,0. Quando vengono specificati *x*, *y* e *z* , il valore predefinito di *w* è 1,0. La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glRect**](glrect-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





