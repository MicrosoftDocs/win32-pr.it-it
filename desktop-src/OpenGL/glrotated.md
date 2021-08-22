---
title: Funzione glRotated (Gl.h)
description: La funzione glRotated moltiplica la matrice corrente per una matrice di rotazione.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- Funzione glRotated OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32216eab9a7c7613f082470360d3f938bbdeaf8ae38cd875d84cd0338dfa78c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491771"
---
# <a name="glrotated-function"></a>Funzione glRotated

La **funzione glRotated** moltiplica la matrice corrente per una matrice di rotazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Angolo* 
</dt> <dd>

Angolo di rotazione, in gradi.

</dd> <dt>

*x* 
</dt> <dd>

Coordinata *x* di un vettore.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata *y* di un vettore.

</dd> <dt>

*z* 
</dt> <dd>

Coordinata *z* di un vettore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glRotated** calcola una matrice che esegue  una rotazione in senso antiorario dei gradi angolari intorno al vettore dall'origine al punto (*x*, *y*, *z*).

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per questa matrice di rotazione, con il prodotto che sostituisce la matrice corrente. In altri punti, se M è la matrice corrente e R è la matrice di traslazione, M viene sostituito con M R.

Se la modalità matrice è GL MODELVIEW o GL PROJECTION, tutti gli oggetti disegnati dopo la chiamata \_ \_ a **glRotated** vengono ruotati. Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non tortuoso.

Le funzioni seguenti recuperano informazioni correlate **a glRotated**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ RENDER \_ MODE

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MATRIX \_ MODE

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MODELVIEW \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ PROJECTION \_ MATRIX

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ TEXTURE \_ MATRIX

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

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





