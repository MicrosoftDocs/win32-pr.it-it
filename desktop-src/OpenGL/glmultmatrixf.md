---
title: funzione glMultMatrixf (GL. h)
description: La funzione glMultMatrixf moltiplica la matrice corrente in base a una matrice arbitraria. | funzione glMultMatrixf (GL. h)
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- funzione glMultMatrixf OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f981b78dc2d9f152a4a7d1f40c4a2d1f120944b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104557598"
---
# <a name="glmultmatrixf-function"></a>glMultMatrixf (funzione)

Le funzioni [**glMultMatrixd**](glmultmatrixd.md) e **glMultMatrixf** moltiplicano la matrice corrente in base a una matrice arbitraria.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*m* 
</dt> <dd>

Puntatore a una matrice 4x4 archiviato nell'ordine colonna-Major come 16 valori consecutivi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glMultMatrix** moltiplica la matrice corrente in base a quella specificata in *m*. Ovvero, se M è la matrice corrente e T è la matrice passata a **glMultMatrix**, m viene sostituito con m T.

La matrice corrente è la matrice di proiezione, la matrice Modelview o la matrice di trama, determinata dalla modalità matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)).

Il parametro *m* punta a una matrice 4x4 di valori a virgola mobile a precisione singola o a precisione doppia archiviati in ordine colonna-principale. Ovvero la matrice viene archiviata come illustrato nella figura seguente.

![! [Diagramma che mostra la matrice 4x4 a cui punta il parametro m.]](images/multi01.png)

Le funzioni seguenti consentono di recuperare informazioni correlate a **glMultMatrix**:

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





