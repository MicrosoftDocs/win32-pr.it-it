---
title: Funzione glPopMatrix (Gl.h)
description: Le funzioni glPushMatrix e glPopMatrix esegono il push e il pop dello stack di matrici corrente. | Funzione glPopMatrix (Gl.h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- Funzione glPopMatrix OpenGL
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
ms.openlocfilehash: d1c0f10456c1038da46d9070689713a8237f876bec7ce7da40acf3d81d89ad15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128021"
---
# <a name="glpopmatrix-function"></a>Funzione glPopMatrix

Le [**funzioni glPushMatrix**](glpushmatrix.md) e **glPopMatrix** esegono il push e il pop dello stack di matrici corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

È un errore eseguire il push di uno stack di matrici completo o inserire uno stack di matrici che contiene una sola matrice. In entrambi i casi, il flag di errore viene impostato e non vengono apportate altre modifiche allo stato OpenGL.

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ UNDERFLOW**</dt> </dl>   | La funzione è stata chiamata mentre lo stack di matrici corrente conteneva una sola matrice.<br/>                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

È disponibile uno stack di matrici per ognuna delle modalità di matrice. In modalità \_ GL MODELVIEW la profondità dello stack è almeno 32. Nelle altre due modalità, GL \_ PROJECTION e GL \_ TEXTURE, la profondità è almeno 2. La matrice corrente in qualsiasi modalità è la matrice all'inizio dello stack per tale modalità.

La [**funzione glPushMatrix**](glpushmatrix.md) inserisce di uno verso il basso lo stack di matrici corrente, duplicando la matrice corrente. Ciò significa che, dopo una chiamata **glPushMatrix,** la matrice all'inizio dello stack è identica a quella sottostante. La **funzione glPopMatrix** popola lo stack di matrici corrente, sostituendo la matrice corrente con quella sottostante nello stack. Inizialmente, ognuno degli stack contiene una matrice, una matrice di identità.

Le funzioni seguenti recuperano informazioni correlate [**a glPushMatrix**](glpushmatrix.md) e **glPopMatrix:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MATRIX \_ MODE

**glGet** con argomento GL \_ MODELVIEW \_ MATRIX

**glGet con** argomento GL \_ PROJECTION \_ MATRIX

**glGet** con argomento GL \_ TEXTURE \_ MATRIX

**glGet con** argomento GL \_ MODELVIEW \_ STACK \_ DEPTH

**glGet con** argomento GL \_ PROJECTION STACK \_ \_ DEPTH

**glGet con** argomento GL \_ TEXTURE STACK \_ \_ DEPTH

**glGet con** argomento GL \_ MAX \_ MODELVIEW STACK \_ \_ DEPTH

**glGet con** argomento GL \_ MAX PROJECTION STACK \_ \_ \_ DEPTH

**glGet con** argomento GL \_ MAX TEXTURE STACK \_ \_ \_ DEPTH

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

 

 





