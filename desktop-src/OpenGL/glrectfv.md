---
title: funzione glRectfv (GL. h)
description: La funzione glRectfv disegna un rettangolo.
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- funzione glRectfv OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871cd3edc44598ba66fb686d9957af7322d77730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400248"
---
# <a name="glrectfv-function"></a>glRectfv (funzione)

La funzione [**glRectfv**](glrectdv.md) disegna un rettangolo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
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

puntatore al vertice opposto del rettangolo.

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

 

 





