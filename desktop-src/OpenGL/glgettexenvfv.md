---
title: Funzione glGetTexEnvfv (Gl.h)
description: Le funzioni glGetTexEnvfv e glGetTexEnviv restituiscono parametri di ambiente della trama. | Funzione glGetTexEnvfv (Gl.h)
ms.assetid: aa037494-e227-48f1-8d5e-9f82073dc2ea
keywords:
- Funzione glGetTexEnvfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnvfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b9b294879711662c67f9ab581e89eaadfa620363e1d19e93f7ea686ba7453a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493871"
---
# <a name="glgettexenvfv-function"></a>Funzione glGetTexEnvfv

Le **funzioni glGetTexEnvfv** [**e glGetTexEnviv**](glgettexenviv.md) restituiscono parametri di ambiente della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexEnvfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Ambiente di trama. Deve essere GL \_ TEXTURE \_ ENV.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico di un parametro dell'ambiente di trama. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**MODALITÀ DI \_ ENV \_ TRAME GL \_**</dt> </dl>    | Il *parametro params* restituisce la modalità ambiente trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**COLORE \_ \_ DELL'AMBIENTE DI TRAMA GL \_**</dt> </dl> | Il *parametro params* restituisce quattro valori integer o a virgola mobile che sono il colore dell'ambiente di trama. I valori integer, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 sia mappato all'intero rappresentabile più positivo e -1.0 sia associato all'intero rappresentabile più negativo.<br/> |



 

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
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* o *pname* non è un valore accettato.<br/>                                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetTexEnv** restituisce nei *parametri* i valori selezionati di un ambiente di trama specificato con [**glTexEnv**](gltexenv-functions.md). Il *parametro di* destinazione specifica un ambiente di trama. Attualmente è definito e supportato un solo ambiente di trama: GL \_ TEXTURE \_ ENV.

Il *parametro pname* nomi di un parametro di ambiente di trama specifico.

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

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





