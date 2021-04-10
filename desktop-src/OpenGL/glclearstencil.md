---
title: funzione glClearStencil (GL. h)
description: La funzione glClearStencil specifica il valore Clear per il buffer dello stencil.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- funzione glClearStencil OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964356"
---
# <a name="glclearstencil-function"></a>glClearStencil (funzione)

La funzione **glClearStencil** specifica il valore Clear per il buffer dello stencil.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*s* 
</dt> <dd>

Indice utilizzato quando il buffer dello stencil viene cancellato. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glClearStencil** specifica l'indice utilizzato da [**glClear**](glclear.md) per cancellare il buffer dello stencil. Il parametro *s* è mascherato da 2 <sup>m</sup>  -1, dove *m* è il numero di bit nel buffer dello stencil.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glClearStencil** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con il \_ \_ valore Clear dello stencil GL degli argomenti \_

**glGet** con \_ bit stencil GL \_ argomento

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

[**glClear**](glclear.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





