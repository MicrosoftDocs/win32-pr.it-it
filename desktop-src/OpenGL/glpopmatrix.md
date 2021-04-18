---
title: funzione glPopMatrix (GL. h)
description: Le funzioni glPushMatrix e glPopMatrix effettuano il push e lo schiocco dello stack della matrice corrente. | funzione glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- funzione glPopMatrix OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321404"
---
# <a name="glpopmatrix-function"></a>glPopMatrix (funzione)

Le funzioni [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** effettuano il push e lo schiocco dello stack della matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Non è possibile eseguire il push di uno stack di matrici completo oppure per estrarre uno stack della matrice che contiene una sola matrice. In entrambi i casi, viene impostato il flag di errore e non viene apportata alcuna modifica allo stato OpenGL.

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_underflow dello stack GL \_**</dt> </dl>   | La funzione è stata chiamata mentre lo stack della matrice corrente contiene una sola matrice.<br/>                                     |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

È disponibile una pila di matrici per ogni modalità della matrice. In \_ modalità GL MODELVIEW, la profondità dello stack è almeno 32. Nelle altre due modalità, proiezione GL \_ e trama GL \_ , la profondità è almeno 2. La matrice corrente in qualsiasi modalità è la matrice nella parte superiore dello stack per tale modalità.

La funzione [**glPushMatrix**](glpushmatrix.md) esegue il push dello stack della matrice corrente verso il basso di uno, duplicando la matrice corrente. Ovvero, dopo una chiamata a **glPushMatrix** , la matrice nella parte superiore dello stack è identica a quella sotto. La funzione **glPopMatrix** estrae lo stack della matrice corrente, sostituendo la matrice corrente con quella sotto di essa nello stack. Inizialmente, ogni stack contiene una matrice, una matrice di identità.

Le funzioni seguenti recuperano informazioni relative a [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_

**glGet** con argomento GL \_ MODELVIEW \_ Matrix

**glGet** con matrice di \_ proiezione GL argomento \_

**glGet** con argomento della \_ matrice di trama GL \_

**glGet** con argomento \_ MODELVIEW \_ Stack \_ Depth

**glGet** con \_ \_ profondità dello stack di proiezione GL argomento \_

**glGet** con argomento \_ \_ profondità dello stack di trama GL \_

**glGet** con argomento con \_ \_ profondità massima \_ dello stack MODELVIEW \_

**glGet** con argomento \_ \_ \_ profondità dello stack di proiezione max \_

**glGet** con argomento di \_ \_ profondità max trama \_ Stack \_

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





