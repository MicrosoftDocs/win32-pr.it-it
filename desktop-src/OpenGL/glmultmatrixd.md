---
title: Funzione glMultMatrixd (Gl.h)
description: La funzione glMultMatrixd moltiplica la matrice corrente per una matrice arbitraria. | Funzione glMultMatrixd (Gl.h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- Funzione glMultMatrixd OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd31b3f84bbc8c75a3622b7b87f7a7577a33927bd489a06b8691377badaf0b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358800"
---
# <a name="glmultmatrixd-function"></a>Funzione glMultMatrixd

Le **funzioni glMultMatrixd** e [**glMultMatrixf**](glmultmatrixf.md) moltiplicano la matrice corrente per una matrice arbitraria.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*m* 
</dt> <dd>

Puntatore a una matrice 4x4 archiviata nell'ordine principale della colonna come 16 valori consecutivi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glMultMatrix** moltiplica la matrice corrente per quella specificata in *m*. In altri punti, se M è la matrice corrente e T è la matrice passata a **glMultMatrix**, M viene sostituito con M T.

La matrice corrente è la matrice di proiezione, la matrice modelview o la matrice di trama, determinata dalla modalità matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)).

Il *parametro m* punta a una matrice 4x4 di valori a virgola mobile a precisione singola o a precisione doppia archiviati nell'ordine delle colonne principali. In altri modi, la matrice viene archiviata come illustrato nell'immagine seguente.

![! [Diagramma che mostra la matrice 4x4 a cui punta il parametro m.]](images/multi01.png)

Le funzioni seguenti recuperano informazioni correlate **a glMultMatrix**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MATRIX \_ MODE

**glGet con** argomento GL \_ MODELVIEW \_ MATRIX

**glGet con** argomento GL \_ PROJECTION \_ MATRIX

**glGet con** argomento GL \_ TEXTURE \_ MATRIX

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





