---
title: Funzione glGetTexGenfv (Gl.h)
description: Le funzioni glGetTexGendv, glGetTexGenfv e glGetTexGeniv restituiscono parametri di generazione delle coordinate di trama. | Funzione glGetTexGenfv (Gl.h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- Funzione glGetTexGenfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40e916f98270c163ed8f299a8466ae66fc2775e466efaeb76a36b0953056eb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493791"
---
# <a name="glgettexgenfv-function"></a>Funzione glGetTexGenfv

Le [**funzioni glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv** e [**glGetTexGeniv**](glgettexgeniv.md) restituiscono parametri di generazione delle coordinate di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Coord* 
</dt> <dd>

Coordinata di trama. Deve essere GL \_ S, GL \_ T, GL \_ R o GL \_ Q.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico dei valori da restituire. Deve essere GL TEXTURE GEN MODE o il nome di una delle equazioni del piano di generazione della \_ \_ \_ trama: GL \_ OBJECT PLANE o GL EYE \_ \_ \_ PLANE. Questi valori sono i seguenti.



| Valore                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**MODALITÀ GEN TRAMA GL \_ \_ \_**</dt> </dl> | Il *parametro params* restituisce la funzione di generazione di trame a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**PIANO OGGETTI GL \_ \_**</dt> </dl>              | Il *parametro params* restituisce i quattro coefficienti dell'equazione del piano che specificano la generazione di coordinate lineari dell'oggetto. I valori interi, se richiesti, vengono mappati direttamente dalla rappresentazione a virgola mobile interna.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**GL \_ EYE \_ PLANE**</dt> </dl>                       | Il *parametro params* restituisce i quattro coefficienti dell'equazione del piano che specificano la generazione di coordinate lineari dell'occhio. I valori interi, se richiesti, vengono mappati direttamente dalla rappresentazione a virgola mobile interna. I valori restituiti sono quelli mantenuti in coordinate oculare. Non sono uguali ai valori specificati tramite [**glTexGen**](gltexgen-functions.md), a meno che la matrice modelview non sia stata identificata al momento della chiamata **a glTexGen.**<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *coord* o *pname* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetTexGen** restituisce nei *parametri selezionati dei parametri* di una funzione di generazione delle coordinate di trama specificata con **glTexGen**. Il *parametro coord* fa nome a una delle coordinate della trama (*s*, *t*, *r*, *q*), usando la costante simbolica GL \_ S, GL \_ T, GL R o GL \_ \_ Q.

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





