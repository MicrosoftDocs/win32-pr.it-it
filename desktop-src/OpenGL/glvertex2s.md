---
title: Funzione glVertex2s (Gl.h)
description: Specifica un vertice. | Funzione glVertex2s (Gl.h)
ms.assetid: e964d7b0-1cb7-4334-8861-1cc2ee37a71a
keywords:
- Funzione glVertex2s OpenGL
topic_type:
- apiref
api_name:
- glVertex2s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe3f48bd8254d15c999a5d3990587a756d61f02fc65fe2faae51473c43c5b79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036201"
---
# <a name="glvertex2s-function"></a>Funzione glVertex2s

Specifica un vertice.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glVertex2s(
   GLshort x,
   GLshort y
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

I comandi della funzione glVertex vengono usati all'interno di coppie [**glBegin**](glbegin.md)glEnd per specificare vertici di / [](glend.md) punti, linee e poligoni. Le coordinate di colore, normale e trama correnti sono associate al vertice quando viene chiamato glVertex. Se si *specificano* *solo x e y,* il valore *predefinito di z* è 0,0 e *w* è 1,0. Quando *si specificano x*, *y* e *z,* *il valore predefinito di w* è 1.0. La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.

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

 

 





