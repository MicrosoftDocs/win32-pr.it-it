---
title: funzione glRectd (GL. h)
description: La funzione glRectd disegna un rettangolo.
ms.assetid: d5574c22-7ae1-4040-9b95-769693fa41e3
keywords:
- funzione glRectd OpenGL
topic_type:
- apiref
api_name:
- glRectd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad37f2d21891ee47182b484741caabda906b20f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301006"
---
# <a name="glrectd-function"></a>glRectd (funzione)

La funzione **glRectd** disegna un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRectd(
   GLdouble x1,
   GLdouble y1,
   GLdouble x2,
   GLdouble y2
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

La funzione **glRectd** supporta una specifica efficiente di rettangoli come due punti d'angolo. Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x*, *y*). Il rettangolo risultante è definito nel piano *z* = 0.

La funzione **glRectd**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:

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

 

 





