---
title: funzione glTranslated (GL. h)
description: La funzione glTranslated moltiplica la matrice corrente in base a una matrice di traslazione.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- funzione glTranslated OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320424"
---
# <a name="gltranslated-function"></a>glTranslated (funzione)

La funzione **glTranslated** moltiplica la matrice corrente in base a una matrice di traslazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
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

La funzione **glTranslated** produce la traduzione specificata da (*x*, *y*, *z*). Il vettore di traduzione viene usato per calcolare una matrice di traslazione 4x4:

![Diagramma che mostra la matrice di conversione 4x4 specificata da x, y, z.](images/trans01.png)

La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per la matrice di traslazione, con il prodotto che sostituisce la matrice corrente. Ovvero, se M è la matrice corrente e T è la matrice di traslazione, M viene sostituito con M T.

Se la modalità matrice è la \_ proiezione GL MODELVIEW o GL \_ , verranno tradotti tutti gli oggetti disegnati dopo **glTranslated** . Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare il sistema di coordinate non convertito.

Le funzioni seguenti consentono di recuperare informazioni correlate a [**glTranslated**](gltranslate.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_

**glGet** con argomento GL \_ MODELVIEW \_ Matrix

**glGet** con matrice di \_ proiezione GL argomento \_

**glGet** con argomento della \_ matrice di trama GL \_

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

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





