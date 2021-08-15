---
title: Funzione glPushMatrix (Gl.h)
description: Le funzioni glPushMatrix e glPopMatrix esegono il push e il pop dello stack di matrici corrente. | Funzione glPushMatrix (Gl.h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- Funzione glPushMatrix OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0d6af41bb02c82a28b667a2b5ad62d942c036c7f744a68fa9bb79188e26ae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795136"
---
# <a name="glpushmatrix-function"></a>Funzione glPushMatrix

Le **funzioni glPushMatrix** e [**glPopMatrix**](glpopmatrix.md) esegono il push e il pop dello stack di matrici corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

È un errore eseguire il push di uno stack di matrici completo o di popolare uno stack di matrici che contiene una sola matrice. In entrambi i casi, il flag di errore viene impostato e non vengono apportate altre modifiche allo stato OpenGL.

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OVERFLOW DELLO STACK GL \_ \_**</dt> </dl>    | La funzione è stata chiamata mentre lo stack di matrici corrente era pieno.<br/>                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

È disponibile uno stack di matrici per ognuna delle modalità matrice. In modalità \_ GL MODELVIEW la profondità dello stack è almeno 32. Nelle altre due modalità, GL \_ PROJECTION e GL \_ TEXTURE, la profondità è almeno 2. La matrice corrente in qualsiasi modalità è la matrice all'inizio dello stack per tale modalità.

La **funzione glPushMatrix** consente di eseguire il push dello stack della matrice corrente di uno verso il basso, duplicando la matrice corrente. Ciò significa che, dopo una chiamata **glPushMatrix,** la matrice all'inizio dello stack è identica a quella sottostante. La **funzione glPopMatrix** popola lo stack di matrici corrente, sostituendo la matrice corrente con quella sottostante nello stack. Inizialmente, ognuno degli stack contiene una matrice, una matrice di identità.

Le funzioni seguenti recuperano informazioni correlate **a glPushMatrix** e **glPopMatrix**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MATRIX \_ MODE

**glGet con** argomento GL \_ MODELVIEW \_ MATRIX

**glGet con** argomento GL \_ PROJECTION \_ MATRIX

**glGet con** argomento GL \_ TEXTURE \_ MATRIX

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

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





