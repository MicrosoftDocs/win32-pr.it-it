---
title: funzione glMatrixMode (GL. h)
description: La funzione glMatrixMode specifica quale matrice è la matrice corrente.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- funzione glMatrixMode OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120438"
---
# <a name="glmatrixmode-function"></a>glMatrixMode (funzione)

La funzione **glMatrixMode** specifica quale matrice è la matrice corrente.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Stack matrice che rappresenta la destinazione per le successive operazioni di matrice. Il parametro *mode* può assumere uno dei tre valori.



| Valore                                                                                                                                                         | Significato                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <dt>**\_MODELVIEW GL**</dt> </dl>    | Applica le successive operazioni della matrice allo stack della matrice Modelview.<br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <dt>**\_proiezione GL**</dt> </dl> | Applica le successive operazioni della matrice allo stack della matrice di proiezione.<br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <dt>**\_trama GL**</dt> </dl>          | Applica le successive operazioni della matrice allo stack della matrice di trame.<br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glMatrixMode** imposta la modalità della matrice corrente.

La funzione seguente recupera le informazioni correlate a **glMatrixMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_

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

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





