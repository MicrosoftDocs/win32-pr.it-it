---
title: funzione glStencilMask (GL. h)
description: La funzione glStencilMask controlla la scrittura di singoli bit nei piani dello stencil.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- funzione glStencilMask OpenGL
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
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121583"
---
# <a name="glstencilmask-function"></a>glStencilMask (funzione)

La funzione **glStencilMask** controlla la scrittura di singoli bit nei piani dello stencil.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maschera* 
</dt> <dd>

Maschera di bit per abilitare e disabilitare la scrittura di singoli bit nei piani dello stencil. Inizialmente, la maschera corrisponde a tutti gli altri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glStencilMask** controlla la scrittura di singoli bit nei piani dello stencil. I *n* bit meno significativi della *maschera*, dove *n* è il numero di bit nel buffer dello stencil, specificare una maschera. Ogni volta che viene visualizzato un oggetto nella maschera, il bit corrispondente nel buffer dello stencil viene reso scrivibile. Quando viene visualizzato uno zero, il bit è protetto da scrittura. Inizialmente, tutti i bit sono abilitati per la scrittura.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glStencilMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento GL \_ stencil \_ WRITEMASK

glGet con \_ bit stencil GL \_ argomento

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

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





