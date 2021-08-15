---
title: Funzione glScaled (Gl.h)
description: Le funzioni glScaled e glScalef moltiplicano la matrice corrente per una matrice di ridimensionamento generale. | Funzione glScaled (Gl.h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- Funzione glScaled OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46742831eaa0a014de0f6ae50271b28c922893133588758119cbf5bff7ba628b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491791"
---
# <a name="glscaled-function"></a>Funzione glScaled

Le **funzioni glScaled** [**e glScalef**](glscalef.md) moltiplicano la matrice corrente per una matrice di ridimensionamento generale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Fattori di scala lungo *l'asse x.*

</dd> <dt>

*y* 
</dt> <dd>

Fattori di scala lungo *l'asse* y.

</dd> <dt>

*z* 
</dt> <dd>

Fattori di scala lungo *l'asse z.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glScaled** produce un ridimensionamento generale lungo gli *assi x*, *y* *e z.* I tre argomenti indicano i fattori di scala desiderati lungo ognuno dei tre assi. La matrice risultante è

![Diagramma che mostra la matrice di fattori di scala lungo gli assi x, y e z.](images/scale01.png)

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per questa matrice di scala, con il prodotto che sostituisce la matrice corrente. Ciò significa che se M è la matrice corrente e S è la matrice di scala, M viene sostituito con M S.

Se la modalità matrice è GL MODELVIEW o GL PROJECTION, tutti gli oggetti disegnati dopo \_ \_ la chiamata di **glScaled** vengono ridimensionati. Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non ridimensionato.

Se alla matrice della visualizzazione del modello vengono applicati fattori di scala diversi da 1.0 e l'illuminazione è abilitata, è probabile che sia abilitata anche la normalizzazione automatica delle normali ([**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'argomento GL \_ NORMALIZE).

Le funzioni seguenti recuperano informazioni correlate **a glScaled**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MODELVIEW \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ PROJECTION \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ TEXTURE \_ MATRIX

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

 

 





