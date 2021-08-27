---
title: Funzione glRectdv (Gl.h)
description: La funzione glRectdv disegna un rettangolo.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- Funzione glRectdv OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 814638997c62b0248bae834f2acd1cd04f0723593533c2fc9237f84c1a4fcd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036661"
---
# <a name="glrectdv-function"></a>Funzione glRectdv

La **funzione glRectdv** disegna un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
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

La **funzione glRectd** supporta una specifica efficiente dei rettangoli come due punti d'angolo. Ogni comando rettangolo accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori alle matrici, ognuno contenente una coppia (*x*, *y*). Il rettangolo risultante è definito nel *piano z* = 0.

La **funzione glRectd**(*x1,* *y1,* *x2,* *y2*) è esattamente equivalente alla sequenza seguente:

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

 

 





