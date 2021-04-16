---
title: funzione glLoadIdentity (GL. h)
description: La funzione glLoadIdentity sostituisce la matrice corrente con la matrice di identità.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- funzione glLoadIdentity OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104553644"
---
# <a name="glloadidentity-function"></a>glLoadIdentity (funzione)

La funzione **glLoadIdentity** sostituisce la matrice corrente con la matrice di identità.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glLoadIdentity** sostituisce la matrice corrente con la matrice di identità. È semanticamente equivalente alla chiamata di [**glLoadMatrix**](glloadmatrix.md) con la matrice di identità seguente.

![Diagramma che mostra la matrice di identità che glLoadIdentity chiama.](images/load01.png)

Tuttavia, in alcuni casi, è più efficiente.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glLoadIdentity**:

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

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





