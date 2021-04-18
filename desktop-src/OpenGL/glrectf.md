---
title: funzione glRectf (GL. h)
description: La funzione glRectf disegna un rettangolo.
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- funzione glRectf OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c7036ae7395dce66d88f52c30631be801c4af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475251"
---
# <a name="glrectf-function"></a>glRectf (funzione)

La funzione [**glRectf**](glrectd.md) disegna un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*X1* 
</dt> <dd>

Coordinata *x* del vertice di un rettangolo.

</dd> <dt>

*Y1* 
</dt> <dd>

Coordinata *y* del vertice di un rettangolo.

</dd> <dt>

*X2* 
</dt> <dd>

Coordinata *x* del vertice opposto del rettangolo.

</dd> <dt>

*Y2* 
</dt> <dd>

Coordinata *y* del vertice opposto del rettangolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glRectf** supporta una specifica efficiente di rettangoli come due punti d'angolo. Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x*, *y*). Il rettangolo risultante è definito nel piano *z* = 0.

La funzione **glRectf**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:

**glBegin**( \_ poligono GL);

**glVertex2**( *x1,* *Y1* );

**glVertex2**( *X2,* *Y1* );

**glVertex2**( *X2,* *Y2* );

**glVertex2**( *x1,* *Y2* );

**glEnd**();

Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con una bobina in senso antiorario.

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

[**Remo**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





