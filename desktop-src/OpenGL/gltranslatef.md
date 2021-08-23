---
title: Funzione glTranslatef (Gl.h)
description: La funzione glTranslatef moltiplica la matrice corrente per una matrice di traslazione.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- Funzione glTranslatef OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12975095aa78d143aaaf096e8b0141f37d45a56286e7d607a9253e59e27ba5bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489846"
---
# <a name="gltranslatef-function"></a>Funzione glTranslatef

La [**funzione glTranslatef**](gltranslate.md) moltiplica la matrice corrente per una matrice di traslazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata *x* di un vettore di traslazione.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata *y* di un vettore di traslazione.

</dd> <dt>

*z* 
</dt> <dd>

Coordinata *z* di un vettore di traslazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glTranslatef** produce la traduzione specificata da (*x*, *y*, *z*). Il vettore di traslazione viene usato per calcolare una matrice di traslazione 4x4:

![Diagramma che mostra la matrice di traslazione 4x4 specificata da x, y, z.](images/trans01.png)

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per questa matrice di traslazione, con il prodotto che sostituisce la matrice corrente. Ciò significa che se M è la matrice corrente e T è la matrice di traslazione, M viene sostituito con M T.

Se la modalità matrice è GL MODELVIEW o GL PROJECTION, vengono convertiti tutti gli oggetti disegnati dopo la chiamata di \_ \_ **glTranslatef.** Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare il sistema di coordinate non tradotto.

Le funzioni seguenti recuperano informazioni correlate [**a glTranslated**](gltranslate.md) **e glTranslatef:**

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

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





