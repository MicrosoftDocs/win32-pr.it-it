---
title: Funzione glRects (Gl.h)
description: La funzione glRects disegna un rettangolo.
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- Funzione glRects OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e7207f46ec8bb25f22b3b620f00994bf88e929dac318abf14bd09af78cd3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937921"
---
# <a name="glrects-function"></a>Funzione glRects

La **funzione glRects** disegna un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
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

La **funzione glRects** supporta una specifica efficiente dei rettangoli come due punti d'angolo. Ogni comando rettangolo accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (x, *y*) o come due puntatori alle matrici, ognuno contenente una coppia (*x*, *y*). Il rettangolo risultante è definito nel *piano z* = 0.

La **funzione glRects**(*x1,* *y1,* *x2,* *y2*) è esattamente equivalente alla sequenza seguente:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Si noti che se il secondo vertice si trova sopra e a destra del primo vertice, il rettangolo viene costruito con una avvolgimento in senso antiorario.

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

 

 





