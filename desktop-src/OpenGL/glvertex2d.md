---
title: Funzione glVertex2d (Gl.h)
description: Specifica un vertice. | Funzione glVertex2d (Gl.h)
ms.assetid: 96398c2a-35d9-4e40-8471-28a1630c81fd
keywords:
- Funzione glVertex2d OpenGL
topic_type:
- apiref
api_name:
- glVertex2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995e629b198f804f1d2a2893fb733f60be550ee16f9cf6c58cee919bd1c6281f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488341"
---
# <a name="glvertex2d-function"></a>Funzione glVertex2d

Specifica un vertice.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glVertex2d(
   GLdouble x,
   GLdouble y
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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

I comandi della funzione glVertex vengono usati all'interno [**delle coppie glBegin**](glbegin.md)glEnd per specificare i vertici di / [](glend.md) punto, linea e poligono. Le coordinate di colore, normale e trama correnti sono associate al vertice quando viene chiamato glVertex. Se si *specificano solo x* e *y,* il valore predefinito *di z* è 0,0 e il valore predefinito *di w* è 1,0. Quando *si specifica x*, *y* e *z,* *w* viene utilizzato il valore predefinito 1.0. La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento indefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

[**glEnd**](glend.md)
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

 

 





