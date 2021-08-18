---
title: Funzione glRotatef (Gl.h)
description: La funzione glRotatef moltiplica la matrice corrente per una matrice di rotazione.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- Funzione glRotatef OpenGL
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
ms.openlocfilehash: 98f466ca73a826d9a12f97093c90c41cd1c753b01f25853096dd3f3219628654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937931"
---
# <a name="glrotatef-function"></a>Funzione glRotatef

La **funzione glRotatef** moltiplica la matrice corrente per una matrice di rotazione.

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

La **funzione glRotatef** calcola una matrice che esegue  una rotazione in senso antiorario dei gradi angolari intorno al vettore dall'origine al punto (*x*, *y*, *z*).

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per questa matrice di rotazione, con il prodotto che sostituisce la matrice corrente. In altri punti, se M è la matrice corrente e R è la matrice di traslazione, M viene sostituito con M R.

Se la modalità matrice è GL MODELVIEW o GL PROJECTION, tutti gli oggetti disegnati dopo la chiamata \_ \_ a **glRotatef** vengono ruotati. Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non tortuoso.

Le funzioni seguenti recuperano informazioni correlate a **glRotatef**:

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

 

 





