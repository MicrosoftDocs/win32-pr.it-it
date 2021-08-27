---
title: Funzione glStencilMask (Gl.h)
description: La funzione glStencilMask controlla la scrittura di singoli bit nei piani di stencil.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- Funzione glStencilMask OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb2e0af89bf2c66e7fa73cf6e4ace8bc8272e8ea581e17bab17754164d3f068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036521"
---
# <a name="glstencilmask-function"></a>Funzione glStencilMask

La **funzione glStencilMask** controlla la scrittura di singoli bit nei piani di stencil.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera* 
</dt> <dd>

Maschera di bit per abilitare e disabilitare la scrittura di singoli bit nei piani di stencil. Inizialmente, la maschera è tutta uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glStencilMask** controlla la scrittura di singoli bit nei piani di stencil. Gli n bit *meno* significativi della *maschera*, dove *n* è il numero di bit nel buffer dello stencil, specificano una maschera. Ogni volta che viene visualizzato un oggetto nella maschera, il bit corrispondente nel buffer dello stencil viene reso scrivibile. Se viene visualizzato uno zero, il bit è protetto da scrittura. Inizialmente, tutti i bit sono abilitati per la scrittura.

Le funzioni seguenti recuperano informazioni correlate **a glStencilMask**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ STENCIL \_ WRITEMASK

glGet con argomento GL \_ STENCIL \_ BITS

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





