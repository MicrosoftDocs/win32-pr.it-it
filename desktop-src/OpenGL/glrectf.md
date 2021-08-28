---
title: Funzione glRectf (Gl.h)
description: La funzione glRectf disegna un rettangolo.
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- Funzione glRectf OpenGL
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
ms.openlocfilehash: 3323979ba2cd5c76c96ac8eb8f85d93e90f90c4b231cdf15b9a18ca363219ae6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492061"
---
# <a name="glrectf-function"></a>Funzione glRectf

La [**funzione glRectf**](glrectd.md) disegna un rettangolo.

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

*x1* 
</dt> <dd>

Coordinata *x* del vertice di un rettangolo.

</dd> <dt>

*y1* 
</dt> <dd>

Coordinata *y* del vertice di un rettangolo.

</dd> <dt>

*x2* 
</dt> <dd>

Coordinata *x* del vertice opposto del rettangolo.

</dd> <dt>

*y2* 
</dt> <dd>

Coordinata *y* del vertice opposto del rettangolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glRectf** supporta una specifica efficiente dei rettangoli come due punti angolo. Ogni comando rettangolo accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori alle matrici, ognuno contenente una coppia (*x*, *y*). Il rettangolo risultante è definito nel *piano z* = 0.

La **funzione glRectf**(*x1,* *y1,* *x2,* *y2*) equivale esattamente alla sequenza seguente:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con un avvolgimento in senso antiorario.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





