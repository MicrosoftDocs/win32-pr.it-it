---
title: funzione glRotatef (GL. h)
description: La funzione glRotatef moltiplica la matrice corrente in base a una matrice di rotazione.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- funzione glRotatef OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479330"
---
# <a name="glrotatef-function"></a>glRotatef (funzione)

La funzione **glRotatef** moltiplica la matrice corrente in base a una matrice di rotazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*angolo* 
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

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glRotatef** calcola una matrice che esegue una rotazione in senso antiorario dei gradi *angolari* sul vettore dall'origine al punto (*x*, *y*, *z*).

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per la matrice di rotazione, con il prodotto che sostituisce la matrice corrente. Ovvero, se M è la matrice corrente e R è la matrice di traslazione, M viene sostituito con M R.

Se la modalità matrice è la \_ proiezione GL MODELVIEW o GL \_ , vengono ruotati tutti gli oggetti disegnati dopo **glRotatef** . Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non ruotato.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glRotatef**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_

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

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





