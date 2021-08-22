---
title: Funzione glLoadMatrixf (Gl.h)
description: La funzione glLoadMatrixf sostituisce la matrice corrente con una matrice arbitraria. | Funzione glLoadMatrixf (Gl.h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- Funzione glLoadMatrixf OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3d822d784d6e24b15296a29da1c77b37b55af4211d2d9b5ce40a3c6a43c7fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492846"
---
# <a name="glloadmatrixf-function"></a>Funzione glLoadMatrixf

Le [**funzioni glLoadMatrixd**](glloadmatrixd.md) **e glLoadMatrixf** sostituiscono la matrice corrente con una matrice arbitraria.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*m* 
</dt> <dd>

Puntatore a una matrice 4x4 archiviata nell'ordine delle colonne principali come 16 valori consecutivi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLoadMatrix** sostituisce la matrice corrente con quella specificata in *m*. La matrice corrente è la matrice di proiezione, la matrice della visualizzazione modello o la matrice di trama, determinata dalla modalità matrice corrente (vedere [**glMatrixMode).**](glmatrixmode.md)

Il *parametro m* punta a una matrice 4x4 di valori a virgola mobile a precisione singola o a precisione doppia archiviati nell'ordine delle colonne principali. In altri modi, la matrice viene archiviata come illustrato nell'immagine seguente.

![Diagramma che mostra la matrice 4x4 a cui punta il parametro m.](images/load02.png)

Le funzioni seguenti recuperano informazioni correlate **a glLoadMatrix:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MATRIX \_ MODE

**glGet** con argomento GL \_ MODELVIEW \_ MATRIX

**glGet con** argomento GL \_ PROJECTION \_ MATRIX

**glGet** con argomento GL \_ TEXTURE \_ MATRIX

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





