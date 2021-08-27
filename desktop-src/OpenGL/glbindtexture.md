---
title: Funzione glBindTexture (Gl.h)
description: La funzione glBindTexture consente la creazione di una trama denominata associata a una destinazione di trama.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- Funzione glBindTexture OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f7f108a0ce4fbc60aba6dc0430227eab15218fe17f80800678fc16b54bbc39f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082221"
---
# <a name="glbindtexture-function"></a>Funzione glBindTexture

La **funzione glBindTexture** consente la creazione di una trama denominata associata a una destinazione di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Destinazione a cui è associata la trama. Deve avere il valore GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

</dd> <dt>

*Texture* 
</dt> <dd>

Nome di una trama. Il nome della trama non può essere attualmente in uso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | La destinazione *del parametro* non è un valore accettato.<br/>                                                                                                                                                       |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La trama *del* parametro non aveva la stessa dimensionalità della destinazione *o* la funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glBindTexture** consente di creare una trama denominata. Chiamando **glBindTexture** con *target* impostato su GL \_ TEXTURE 1D o GL TEXTURE \_ \_ \_ 2D e *texture* impostata sul nome della nuova trama creata, il nome della trama viene associato alla destinazione di trama appropriata. Quando una trama è associata a una destinazione, l'associazione precedente per tale destinazione non è più in vigore.

I nomi delle trame sono interi senza segno con valore zero riservato per rappresentare la trama predefinita per ogni destinazione di trama. I nomi delle trame e il contenuto della trama corrispondente sono locali allo spazio dell'elenco di visualizzazione condiviso del contesto di rendering OpenGL corrente. Due contesti di rendering condividono i nomi delle trame solo se condividono anche elenchi di visualizzazione. È possibile generare un set di nuovi nomi di trama [**usando glGenTextures**](glgentextures.md).

Quando una trama viene associata per la prima volta, presuppone la dimensionalità della destinazione della trama; una trama associata a GL \_ TEXTURE \_ 1D diventa unidimensionale e una trama associata a GL \_ TEXTURE \_ 2D diventa bidimensionale. Le operazioni eseguite su una destinazione di trama influiscono anche su una trama associata alla destinazione. Quando si esegue una query su una destinazione di trama, il valore restituito è lo stato della trama associata. Le destinazioni trame diventano alias per le trame attualmente associate.

Quando si associa una trama con **glBindTexture**, l'associazione rimane attiva fino a quando una trama diversa non viene associata alla stessa destinazione o non si elimina la trama associata con la funzione [**glDeleteTextures.**](gldeletetextures.md) Dopo aver creato una trama denominata, è possibile associarla a una destinazione di trama con la stessa dimensionalità necessaria.

In genere è molto più veloce usare **glBindTexture** per associare una trama denominata esistente a una delle destinazioni di trama anziché ricaricare l'immagine della trama usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D.**](glteximage2d.md) Per un controllo aggiuntivo delle prestazioni di texturing, [**usare glPrioritizeTextures**](glprioritizetextures.md).

È possibile includere chiamate a **glBindTexture** negli elenchi di visualizzazione.

> [!Note]  
> La **funzione glBindTexture** è disponibile solo in OpenGL versione 1.1 o successiva.

 

Le funzioni seguenti recuperano informazioni correlate **a glBindTexture**:

-   [**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ TEXTURE \_ 1D \_ BINDING

**glGet con** argomento GL \_ TEXTURE \_ 2D \_ BINDING

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





