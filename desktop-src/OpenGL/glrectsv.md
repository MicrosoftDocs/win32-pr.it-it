---
title: Funzione glRectsv (Gl.h)
description: La funzione glRectsv disegna un rettangolo.
ms.assetid: 0f7dc4fc-b6ce-4240-89d9-69f54c0c9f2b
keywords:
- Funzione glRectsv OpenGL
topic_type:
- apiref
api_name:
- glRectsv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd497def5255d8c3875721fa53f6a742c8a0714c0e4d8e7146d3c20423c29752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519841"
---
# <a name="glrectsv-function"></a>Funzione glRectsv

La **funzione glRectsv** disegna un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRectsv(
   const GLshort *v1,
   const GLshort *v2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*v1* 
</dt> <dd>

Puntatore a un vertice di un rettangolo.

</dd> <dt>

*v2* 
</dt> <dd>

Puntatore al vertice opposto del rettangolo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glRects** supporta una specifica efficiente dei rettangoli come due punti d'angolo. Ogni comando rettangolo accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori alle matrici, ognuno contenente una coppia (*x,* *y*). Il rettangolo risultante è definito nel *piano z* = 0.

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

 

 





