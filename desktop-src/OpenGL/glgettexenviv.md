---
title: funzione glGetTexEnviv (GL. h)
description: Le funzioni glGetTexEnvfv e glGetTexEnviv restituiscono parametri di ambiente di trama. | funzione glGetTexEnviv (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- funzione glGetTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321409"
---
# <a name="glgettexenviv-function"></a>glGetTexEnviv (funzione)

Le funzioni [**glGetTexEnvfv**](glgettexenvfv.md) e **glGetTexEnviv** restituiscono parametri di ambiente di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Ambiente di trama. Deve essere una \_ trama GL \_ env.

</dd> <dt>

*pname* 
</dt> <dd>

Nome simbolico di un parametro dell'ambiente di trama. Vengono accettati i valori seguenti.



| Valore                                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <dt>**\_ \_ modalità ENV trama \_ GL**</dt> </dl>    | Il parametro *params* restituisce la modalità dell'ambiente di trama a valore singolo, una costante simbolica.<br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <dt>**\_ \_ colore ENV trama \_ GL**</dt> </dl> | Il parametro *params* restituisce quattro valori integer o a virgola mobile che corrispondono al colore dell'ambiente di trama. I valori integer, se richiesti, vengono mappati linearmente dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al numero intero rappresentabile più positivo e-1,0 sia mappato al numero intero rappresentabile più negativo.<br/> |



 

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
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* o *pname* non è un valore accettato.<br/>                                                                             |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetTexEnv** restituisce i valori selezionati dei *params* di un ambiente di trama specificato con [**glTexEnv**](gltexenv-functions.md). Il parametro *target* specifica un ambiente di trama. Attualmente, viene definito e supportato un solo ambiente di trama: GL \_ texture \_ env.

Il parametro *pname* assegna un nome a un parametro di ambiente di trama specifico.

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

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





