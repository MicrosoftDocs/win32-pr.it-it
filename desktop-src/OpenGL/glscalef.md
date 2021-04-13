---
title: funzione glScalef (GL. h)
description: Le funzioni glScaled e glScalef moltiplicano la matrice corrente in base a una matrice di scala generale. | funzione glScalef (GL. h)
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
keywords:
- funzione glScalef OpenGL
topic_type:
- apiref
api_name:
- glScalef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eda183b763f22736370dd5c9ea13ca8793243e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104559550"
---
# <a name="glscalef-function"></a>glScalef (funzione)

Le funzioni [**glScaled**](glscaled.md) e **glScalef** moltiplicano la matrice corrente in base a una matrice di scala generale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glScalef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Fattori di scala lungo l'asse *x* .

</dd> <dt>

*y* 
</dt> <dd>

Fattori di scala lungo l'asse *y* .

</dd> <dt>

*z* 
</dt> <dd>

Fattori di scala lungo l'asse *z* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glScalef** produce una scala generale lungo gli assi *x*, *y* e *z* . I tre argomenti indicano i fattori di scala desiderati lungo ognuno dei tre assi. La matrice risultante viene visualizzata nella figura seguente.

![Diagramma che mostra la matrice di fattori di scala lungo gli assi x, y e z.](images/scale01.png)

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per questa matrice di scala, con il prodotto che sostituisce la matrice corrente. Ovvero, se M è la matrice corrente e S è la matrice di scala, M viene sostituito con M S.

Se la modalità matrice è una \_ proiezione GL MODELVIEW o GL \_ , vengono ridimensionati tutti gli oggetti disegnati dopo **glScalef** . Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non ridimensionato.

Se si applicano fattori di scala diversi da 1,0 alla matrice Modelview e l'illuminazione è abilitata, è probabile che anche la normalizzazione automatica delle normali sia abilitata ([**glEnable**](glenable.md) e [**GLDISABLE**](gldisable.md) con argument GL \_ Normalize).

Le funzioni seguenti consentono di recuperare informazioni correlate a **glScalef**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MODELVIEW \_ Matrix

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con matrice di \_ proiezione GL argomento \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ matrice di trama GL \_

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotated**](glrotated.md)
</dt> <dt>

[**glRotatef**](glrotatef.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





