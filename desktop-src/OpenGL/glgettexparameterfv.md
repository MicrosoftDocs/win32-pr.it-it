---
title: funzione glGetTexParameterfv (GL. h)
description: Le funzioni glGetTexParameterfv e glGetTexParameteriv restituiscono i valori dei parametri della trama. | funzione glGetTexParameterfv (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- funzione glGetTexParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321814"
---
# <a name="glgettexparameterfv-function"></a>glGetTexParameterfv (funzione)

Le funzioni **glGetTexParameterfv** e [**glGetTexParameteriv**](glgettexparameteriv.md) restituiscono i valori dei parametri della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Nome simbolico della trama di destinazione. \_ \_ Viene accettata la trama GL 1D e GL \_ texture \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Nome simbolico di un parametro di trama. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_ \_ filtro mag trama di contabilità \_**</dt> </dl>       | Restituisce il filtro di ingrandimento della trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_ \_ Filtro minimo trama \_ GL**</dt> </dl>       | Restituisce il filtro minification di trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_wrapping di trama GL \_ \_**</dt> </dl>                   | Restituisce la funzione di wrapping a valore singolo per le coordinate di trama *s*, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_wrapping trama \_ GL \_ T**</dt> </dl>                   | Restituisce la funzione di wrapping a valore singolo per la coordinata di trama *t*, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**\_ \_ colore bordo trama \_ GL**</dt> </dl> | Restituisce quattro numeri interi o a virgola mobile che comprendono il colore RGBA del bordo della trama. I valori a virgola mobile vengono restituiti nell'intervallo compreso tra \[ 0 e 1 \] . I valori integer vengono restituiti come mapping lineare della rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_priorità trama \_ GL**</dt> </dl>              | Restituisce la priorità di residenza della trama di destinazione (o della trama denominata associata). Il valore iniziale è 1. Vedere [**glPrioritizeTextures**](glprioritizetextures.md).<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**\_residente trama \_ GL**</dt> </dl>              | Restituisce lo stato di residenza della trama di destinazione. Se il valore restituito in params è GL \_ true, la trama è residente nella memoria della trama. Vedere [**glAreTexturesResident**](glaretexturesresident.md).<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i parametri della trama.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *destinazione* o il *nome* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetTexParameter** restituisce in *params* il valore o i valori del parametro texture specificato come *pname*. Il parametro *target* definisce la trama di destinazione, ovvero GL \_ texture \_ 1D o GL \_ trama \_ 2D, per specificare una texturatura bidimensionale o bidimensionale. Il parametro *pname* accetta gli stessi simboli di [**glTexParameter**](gltexparameter-functions.md), con le stesse interpretazioni.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.

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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





