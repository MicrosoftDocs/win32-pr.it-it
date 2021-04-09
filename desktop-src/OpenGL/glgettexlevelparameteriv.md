---
title: funzione glGetTexLevelParameteriv (GL. h)
description: Le funzioni glGetTexLevelParameterfv e glGetTexLevelParameteriv restituiscono i valori dei parametri di trama per un livello di dettaglio specifico. | funzione glGetTexLevelParameteriv (GL. h)
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- funzione glGetTexLevelParameteriv OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0fa167eae842784e967538ff1539e0b43a6a2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969082"
---
# <a name="glgettexlevelparameteriv-function"></a>glGetTexLevelParameteriv (funzione)

Le funzioni [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) e **glGetTexLevelParameteriv** restituiscono i valori dei parametri di trama per un livello di dettaglio specifico.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexLevelParameteriv(
   GLenum target,
   GLint  level,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Il nome simbolico della trama di destinazione: GL \_ texture \_ 1D, GL \_ texture \_ 2D, GL \_ proxy \_ texture \_ 1D o GL \_ proxy \_ texture \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Il numero del livello di dettaglio dell'immagine desiderata. Il livello 0 è il livello dell'immagine di base. Il livello *n* è l'immagine di riduzione del mipmap *n*.

</dd> <dt>

*pname* 
</dt> <dd>

Nome simbolico di un parametro di trama. I nomi di parametro seguenti sono accettati.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**\_spessore trama \_ GL**</dt> </dl>                                | Il parametro *params* restituisce un singolo valore contenente la larghezza dell'immagine della trama. Questo valore include il bordo dell'immagine della trama.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**\_altezza trama \_ GL**</dt> </dl>                             | Il parametro *params* restituisce un singolo valore contenente l'altezza dell'immagine della trama. Questo valore include il bordo dell'immagine della trama.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**\_ \_ formato interno trama \_ GL**</dt> </dl> | Il parametro *params* restituisce un singolo valore che descrive il formato di Texel della trama.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**\_bordo trama \_ GL**</dt> </dl>                             | Il parametro *params* restituisce un singolo valore, ovvero la larghezza, in pixel, del bordo dell'immagine della trama.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**\_ \_ dimensioni rosse trama \_ GL**</dt> </dl>                      | Risoluzione dell'archiviazione interna del componente rosso di un Texel. La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**\_ \_ dimensioni verdi trama \_ GL**</dt> </dl>                | Risoluzione dell'archiviazione interna del componente verde di un Texel. La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**\_ \_ dimensioni blu trama \_ GL**</dt> </dl>                   | Risoluzione dell'archiviazione interna del componente blu di un Texel. La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**\_ \_ dimensioni alfa trama \_ GL**</dt> </dl>                | Risoluzione dell'archiviazione interna del componente alfa di un Texel. La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**\_ \_ dimensioni luminanza trama GL \_**</dt> </dl>    | Risoluzione dell'archiviazione interna del componente luminanza di un Texel. La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**\_dimensioni dell' \_ intensità della trama GL \_**</dt> </dl>    | Risoluzione dell'archiviazione interna del componente Intensity di un Texel. La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**\_componenti di trama GL \_**</dt> </dl>                 | Il parametro *params* restituisce un singolo valore, ovvero il numero di componenti nell'immagine della trama.<br/>                                                                                                                                                                                          |



 

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
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *livello* è minore di zero o maggiore di *log* 2 *(max)*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .<br/>      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetTexLevelParameter** restituisce i valori dei parametri di trama di *params* per un valore specifico del livello di dettaglio, specificato come *Level*. Il parametro *target* definisce la trama di destinazione, ovvero GL \_ texture \_ 1D, GL \_ texture \_ 2D, GL \_ proxy \_ texture \_ 1D o GL \_ proxy \_ texture \_ 2D per specificare il texturing unidimensionale o bidimensionale. Il parametro *pname* specifica il parametro della trama il cui valore o i valori verranno restituiti.

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

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





