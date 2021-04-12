---
title: funzione glBindTexture (GL. h)
description: La funzione glBindTexture consente la creazione di una trama denominata associata a una destinazione di trama.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- funzione glBindTexture OpenGL
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
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400709"
---
# <a name="glbindtexture-function"></a>glBindTexture (funzione)

La funzione **glBindTexture** consente la creazione di una trama denominata associata a una destinazione di trama.

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

Destinazione a cui è associata la trama. È necessario che il valore di GL \_ trama \_ 1D o GL \_ trama \_ 2D sia.

</dd> <dt>

*trama* 
</dt> <dd>

Nome di una trama; il nome della trama non può essere attualmente in uso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | La *destinazione* del parametro non è un valore accettato.<br/>                                                                                                                                                       |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La *trama* del parametro non ha la stessa dimensionalità della *destinazione* oppure è stata chiamata la funzione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glBindTexture** consente di creare una trama denominata. La chiamata di **glBindTexture** con la *destinazione* impostata su GL \_ texture \_ 1D o GL \_ trama \_ 2D e la *trama* impostata sul nome della nuova trama creata associa il nome della trama alla destinazione di trama appropriata. Quando una trama è associata a una destinazione, l'associazione precedente per tale destinazione non è più attiva.

I nomi di trama sono interi senza segno il cui valore è zero riservato per rappresentare la trama predefinita per ogni destinazione di trama. I nomi di trama e il contenuto della trama corrispondente sono locali nello spazio di visualizzazione condiviso del contesto di rendering OpenGL corrente. due contesti di rendering condividono nomi di trama solo se condividono anche elenchi di visualizzazione. È possibile generare un set di nuovi nomi di trama usando [**glGenTextures**](glgentextures.md).

Quando una trama viene associata per la prima volta, presuppone la dimensionalità della relativa destinazione di trama; una trama associata alla \_ trama GL \_ 1D diventa unidimensionale e una trama associata alla trama GL \_ \_ 2D diventa bidimensionale. Le operazioni eseguite su una destinazione di trama influiscono anche su una trama associata alla destinazione. Quando si esegue una query su una destinazione di trama, il valore restituito è lo stato della trama a esso associata. Le destinazioni di trama diventano alias per le trame attualmente vincolate.

Quando si associa una trama a **glBindTexture**, l'associazione rimane attiva fino a quando una trama diversa viene associata alla stessa destinazione o si elimina la trama associata con la funzione [**glDeleteTextures**](gldeletetextures.md) . Dopo aver creato una trama denominata, è possibile associarla a una destinazione di trama con la stessa dimensionalità della frequenza necessaria.

In genere è molto più veloce usare **glBindTexture** per associare una trama denominata esistente a una delle destinazioni di trama anziché ricaricare l'immagine di trama usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md). Per un maggiore controllo sulle prestazioni di texturing, usare [**glPrioritizeTextures**](glprioritizetextures.md).

È possibile includere chiamate a **glBindTexture** negli elenchi di visualizzazione.

> [!Note]  
> La funzione **glBindTexture** è disponibile solo in OpenGL versione 1,1 o successiva.

 

Le funzioni seguenti consentono di recuperare informazioni correlate a **glBindTexture**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ texture \_ 1D \_ binding

**glGet** con argomento GL \_ trama \_ 2D \_ binding

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

 

 





