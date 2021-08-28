---
title: Funzione glLoadIdentity (Gl.h)
description: La funzione glLoadIdentity sostituisce la matrice corrente con la matrice di identità.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- Funzione glLoadIdentity OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c0917dae2ae21acd61b6931bcb683a4f3f85f88af45c20fe6137e464254f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493006"
---
# <a name="glloadidentity-function"></a>Funzione glLoadIdentity

La **funzione glLoadIdentity** sostituisce la matrice corrente con la matrice di identità.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLoadIdentity** sostituisce la matrice corrente con la matrice di identità. È semanticamente equivalente alla chiamata [**di glLoadMatrix con**](glloadmatrix.md) la matrice di identità seguente.

![Diagramma che mostra la matrice di identità chiamata da glLoadIdentity.](images/load01.png)

Tuttavia, in alcuni casi, è più efficiente.

Le funzioni seguenti recuperano informazioni correlate **a glLoadIdentity**:

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

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





