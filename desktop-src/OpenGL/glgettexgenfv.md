---
title: funzione glGetTexGenfv (GL. h)
description: Le funzioni glGetTexGendv, glGetTexGenfv e glGetTexGeniv restituiscono parametri di generazione delle coordinate di trama. | funzione glGetTexGenfv (GL. h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- funzione glGetTexGenfv OpenGL
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
ms.openlocfilehash: e527d0388b8aca7239ba1c51dccdce15de3cd8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352851"
---
# <a name="glgettexgenfv-function"></a>glGetTexGenfv (funzione)

Le funzioni [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv** e [**glGetTexGeniv**](glgettexgeniv.md) restituiscono parametri di generazione delle coordinate di trama.

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

*pname* 
</dt> <dd>

Nome simbolico del valore o dei valori da restituire. Deve essere \_ \_ \_ la modalità gen della trama GL o il nome di una delle equazioni del piano di generazione della trama, ovvero il \_ piano dell'oggetto GL o il \_ \_ piano GL Eye \_ . Questi valori sono i seguenti.



| Valore                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <dt>**\_modalità di \_ generazione \_ trama GL**</dt> </dl> | Il parametro *params* restituisce la funzione di generazione della trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <dt>**\_piano oggetto \_ GL**</dt> </dl>              | Il parametro *params* restituisce i quattro coefficienti di equazione del piano che specificano la generazione della coordinata lineare dell'oggetto. Per i valori integer, quando richiesto, viene eseguito il mapping direttamente dalla rappresentazione a virgola mobile interna.<br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <dt>**\_piano d'occhio GL \_**</dt> </dl>                       | Il parametro *params* restituisce i quattro coefficienti di equazione del piano che specificano la generazione della coordinata lineare degli occhi. Per i valori integer, quando richiesto, viene eseguito il mapping direttamente dalla rappresentazione a virgola mobile interna. I valori restituiti sono quelli mantenuti in coordinate oculari. Non sono uguali ai valori specificati tramite [**glTexGen**](gltexgen-functions.md), a meno che non sia stata identificata la matrice Modelview al momento della chiamata di **glTexGen** .<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Coord* o *pname* non è un valore accettato.<br/>                                                                              |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetTexGen** restituisce parametri selezionati in *params* di una funzione di generazione della coordinata di trama specificata con **glTexGen**. Il parametro *Coord* denomina una delle coordinate di trama (*s*, *t*, *r*, *q*), usando la costante simbolica GL \_ s, GL \_ t, GL \_ r o GL \_ q.

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

[**glTexGen**](gltexgen-functions.md)
</dt> </dl>

 

 





