---
title: Funzione glGetTexParameteriv (Gl.h)
description: Le funzioni glGetTexParameterfv e glGetTexParameteriv restituiscono i valori dei parametri di trama. | Funzione glGetTexParameteriv (Gl.h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- Funzione glGetTexParameteriv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1226f4096088d20851b0eab9789acf19cb84ecfac5202ff9e992c8c07ded4bb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493671"
---
# <a name="glgettexparameteriv-function"></a>Funzione glGetTexParameteriv

Le [**funzioni glGetTexParameterfv**](glgettexparameterfv.md) **e glGetTexParameteriv** restituiscono i valori dei parametri di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Nome simbolico della trama di destinazione. Sono \_ accettati GL TEXTURE \_ 1D e GL \_ TEXTURE \_ 2D.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico di un parametro di trama. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO \_ MAG \_ TRAMA GL \_**</dt> </dl>       | Restituisce il filtro di ingrandimento della trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN TRAMA GL \_ \_ \_**</dt> </dl>       | Restituisce il filtro di minificazione della trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>                   | Restituisce la funzione di wrapping a valore singolo per le coordinate *di trama,* una costante simbolica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Restituisce la funzione di wrapping a valore singolo per la *coordinata* di trama t , una costante simbolica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**COLORE BORDO TRAMA GL \_ \_ \_**</dt> </dl> | Restituisce quattro numeri interi o a virgola mobile che costituiscono il colore RGBA del bordo della trama. I valori a virgola mobile vengono restituiti nell'intervallo \[ 0,1. \] I valori interi vengono restituiti come mapping lineare della rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato all'intero rappresentabile più positivo e -1.0 sia mappato all'intero rappresentabile più negativo.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**PRIORITÀ TRAMA GL \_ \_**</dt> </dl>              | Restituisce la priorità di priorità della trama di destinazione (o della trama denominata associata). Il valore iniziale è 1. Vedere [**glPrioritizeTextures.**](glprioritizetextures.md)<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**GL \_ TEXTURE \_ RESIDENT**</dt> </dl>              | Restituisce lo stato di rilascio della trama di destinazione. Se il valore restituito in params è GL \_ TRUE, la trama si trova nella memoria della trama. Vedere [**glAreTexturesResident.**](glaretexturesresident.md)<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i parametri della trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *target* o *name* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetTexParameter** restituisce in *params* il valore o i valori del parametro texture specificato come *pname*. Il *parametro target* definisce la trama di destinazione, GL TEXTURE 1D o GL TEXTURE 2D, per specificare la \_ \_ texturing unidimensionale o \_ \_ bidimensionale. Il *parametro pname* accetta gli stessi simboli di [**glTexParameter**](gltexparameter-functions.md), con le stesse interpretazioni.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.

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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





