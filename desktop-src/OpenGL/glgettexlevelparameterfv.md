---
title: Funzione glGetTexLevelParameterfv (Gl.h)
description: Le funzioni glGetTexLevelParameterfv e glGetTexLevelParameteriv restituiscono i valori dei parametri di trama per un livello di dettaglio specifico. | Funzione glGetTexLevelParameterfv (Gl.h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- Funzione glGetTexLevelParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4068b6544c334c4ca1c8e6640ccb4752669240cdde16d0522a4e13d06ebc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359777"
---
# <a name="glgettexlevelparameterfv-function"></a>Funzione glGetTexLevelParameterfv

Le **funzioni glGetTexLevelParameterfv** [**e glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) restituiscono i valori dei parametri di trama per un livello di dettaglio specifico.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Nome simbolico della trama di destinazione: GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE 1D o GL PROXY TEXTURE \_ \_ \_ \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio dell'immagine desiderata. Il livello 0 è il livello dell'immagine di base. Il *livello n* è *l'esima* immagine di riduzione mipmap.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico di un parametro di trama. Vengono accettati i nomi di parametro seguenti.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**LARGHEZZA TRAMA GL \_ \_**</dt> </dl>                                | Il *parametro params* restituisce un singolo valore contenente la larghezza dell'immagine della trama. Questo valore include il bordo dell'immagine della trama.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**ALTEZZA TRAMA GL \_ \_**</dt> </dl>                             | Il *parametro params* restituisce un singolo valore contenente l'altezza dell'immagine della trama. Questo valore include il bordo dell'immagine della trama.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**FORMATO \_ INTERNO DELLA \_ TRAMA GL \_**</dt> </dl> | Il *parametro params* restituisce un singolo valore che descrive il formato texel della trama.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**BORDO DELLA TRAMA GL \_ \_**</dt> </dl>                             | Il *parametro params* restituisce un singolo valore, la larghezza in pixel del bordo dell'immagine della trama.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**GL \_ TEXTURE \_ RED \_ SIZE**</dt> </dl>                      | Risoluzione di archiviazione interna del componente rosso di un texel. La risoluzione scelta da OpenGL sarà una corrispondenza vicina per la risoluzione richiesta dall'utente con l'argomento componente [**di glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**DIMENSIONE \_ VERDE \_ TRAMA GL \_**</dt> </dl>                | Risoluzione di archiviazione interna del componente verde di un texel. La risoluzione scelta da OpenGL sarà una corrispondenza vicina per la risoluzione richiesta dall'utente con l'argomento componente [**di glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**DIMENSIONI BLU TRAMA GL \_ \_ \_**</dt> </dl>                   | Risoluzione di archiviazione interna del componente blu di un texel. La risoluzione scelta da OpenGL sarà una corrispondenza vicina per la risoluzione richiesta dall'utente con l'argomento componente [**di glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**GL \_ TEXTURE ALPHA SIZE \_ (DIMENSIONI ALFA TRAMA \_ GL)**</dt> </dl>                | Risoluzione di archiviazione interna del componente alfa di un texel. La risoluzione scelta da OpenGL sarà una corrispondenza vicina per la risoluzione richiesta dall'utente con l'argomento componente [**di glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**DIMENSIONI \_ DELLA \_ LUMINANCE DELLA \_ TRAMA GL**</dt> </dl>    | Risoluzione di archiviazione interna del componente luminance di un texel. La risoluzione scelta da OpenGL sarà una corrispondenza vicina per la risoluzione richiesta dall'utente con l'argomento componente [**di glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**DIMENSIONI \_ \_ INTENSITÀ TRAMA GL \_**</dt> </dl>    | Risoluzione di archiviazione interna del componente di intensità di un texel. La risoluzione scelta da OpenGL sarà una corrispondenza vicina per la risoluzione richiesta dall'utente con l'argomento componente [**di glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**COMPONENTI DELLA TRAMA GL \_ \_**</dt> </dl>                 | Il *parametro params* restituisce un singolo valore: il numero di componenti nell'immagine della trama.<br/>                                                                                                                                                                                          |



 

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
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *target* o *pname non* è un valore accettato.<br/>                                                                             |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o maggiore del *log* 2 *(max)*, dove *max* è il valore restituito di GL \_ MAX TEXTURE \_ \_ SIZE.<br/>      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetTexLevelParameter** restituisce nei valori dei parametri della trama *params* per un valore specifico del livello di dettaglio, specificato come *livello*. Il  parametro target definisce la trama di destinazione, GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE 1D o GL PROXY TEXTURE 2D \_ \_ \_ \_ per \_ specificare la trama unidimensionale o bidimensionale. Il *parametro pname* specifica il parametro texture di cui verranno restituiti i valori.

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

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





