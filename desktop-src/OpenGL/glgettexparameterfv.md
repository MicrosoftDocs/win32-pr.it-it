---
title: Funzione glGetTexParameterfv (Gl.h)
description: Le funzioni glGetTexParameterfv e glGetTexParameteriv restituiscono i valori dei parametri di trama. | Funzione glGetTexParameterfv (Gl.h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- Funzione glGetTexParameterfv OpenGL
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
ms.openlocfilehash: 7925ae070a3e35f6c9b3a9ba65ff506f775b77e625dc852b49cc305c76003428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359711"
---
# <a name="glgettexparameterfv-function"></a>Funzione glGetTexParameterfv

Le **funzioni glGetTexParameterfv** e [**glGetTexParameteriv**](glgettexparameteriv.md) restituiscono i valori dei parametri di trama.

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

Nome simbolico della trama di destinazione. Gl \_ TEXTURE \_ 1D e GL \_ TEXTURE \_ 2D sono accettate.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico di un parametro di trama. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO MAG \_ \_ TRAMA \_ GL**</dt> </dl>       | Restituisce il filtro di ingrandimento della trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN \_ \_ TRAME GL \_**</dt> </dl>       | Restituisce il filtro di minificazione della trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_AVVOLGI \_ TRAMA GL \_ S**</dt> </dl>                   | Restituisce la funzione di wrapping a valore singolo per le coordinate della *trama,* una costante simbolica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Restituisce la funzione di wrapping a valore singolo per la coordinata di trama *t*, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**COLORE \_ BORDO \_ TRAMA \_ GL**</dt> </dl> | Restituisce quattro numeri interi o a virgola mobile che costituiscono il colore RGBA del bordo della trama. I valori a virgola mobile vengono restituiti nell'intervallo \[ 0,1. \] I valori integer vengono restituiti come mapping lineare della rappresentazione a virgola mobile interna in modo che 1.0 sia mappato all'intero rappresentabile più positivo e -1.0 sia associato all'intero rappresentabile più negativo.<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**PRIORITÀ \_ TRAME GL \_**</dt> </dl>              | Restituisce la priorità di residenza della trama di destinazione (o della trama denominata associata). Il valore iniziale è 1. Vedere [**glPrioritizeTextures**](glprioritizetextures.md).<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**RESIDENTE \_ TRAME GL \_**</dt> </dl>              | Restituisce lo stato di residenza della trama di destinazione. Se il valore restituito in params è GL \_ TRUE, la trama è residente nella memoria della trama. Vedere [**glAreTexturesResident**](glaretexturesresident.md).<br/>                                                                                                                                                                           |



 

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
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* o *name* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetTexParameter** restituisce in *params* il valore o i valori del parametro texture specificato come *pname*. Il *parametro di* destinazione definisce la trama di destinazione, GL TEXTURE 1D o GL TEXTURE 2D, per specificare la texturing unidimensionale o \_ \_ \_ \_ bidimensionale. Il *parametro pname* accetta gli stessi simboli di [**glTexParameter**](gltexparameter-functions.md), con le stesse interpretazioni.

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

 

 





