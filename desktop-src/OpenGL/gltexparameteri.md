---
title: funzione glTexParameteri (GL. h)
description: Imposta i parametri della trama. | funzione glTexParameteri (GL. h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- funzione glTexParameteri OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207ac902047c5a2b6a5266d08e71f8e47f7ccb97
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352721"
---
# <a name="gltexparameteri-function"></a>glTexParameteri (funzione)

Imposta i parametri della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione, che deve essere di tipo GL \_ trama \_ 1D o GL \_ trama \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Nome simbolico di un parametro di trama a valore singolo. I simboli seguenti sono accettati in *pname*.



| Valore                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_ \_ Filtro minimo trama \_ GL**</dt> </dl> | La funzione minimizzazione di trama viene utilizzata ogni volta che il pixel con trama viene mappato a un'area maggiore di un elemento texture. Sono disponibili sei funzioni minimizzazione definite. Due di essi utilizzano i quattro elementi di trama più vicini o più vicini per calcolare il valore di trama. Gli altri quattro usano mipmap. <br/> Un mipmap è un set ordinato di matrici che rappresentano la stessa immagine in risoluzioni progressivamente inferiori. Se la trama ha dimensioni 2nx2<sup>m</sup> sono disponibili max (n, m) + 1 mipmap. Il primo mipmap è la trama originale, con dimensioni 2nx2<sup>m</sup>. Ogni mipmap successiva ha dimensioni 2<sup>k</sup>1x2<sup>l</sup>1 dove 2<sup>k</sup>X2<sup>l</sup> sono le dimensioni del mipmap precedente, fino a k = 0 o l = 0. A questo punto, mipmap successivi hanno la dimensione 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 fino alla mipmap finale, che ha la dimensione 1x1. Mipmap vengono definiti usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con l'argomento del livello di dettaglio che indica l'ordine del mipmap. Il livello 0 è la trama originale; il livello max Bold (n, m) è il mipmap 1x1 finale.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_ \_ filtro mag trama di contabilità \_**</dt> </dl> | La funzione di ingrandimento della trama viene utilizzata quando il pixel con trama viene mappato a un'area minore o uguale a un elemento texture. Imposta la funzione di ingrandimento della trama su GL \_ più vicino o su GL \_ lineare.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_wrapping di trama GL \_ \_**</dt> </dl>             | Imposta il parametro Wrap per le coordinate di trama su GL \_ clamp o GL \_ Repeat. \_Il morsetto GL causa il fissaggio delle coordinate a nell'intervallo \[ 0, 1 \] ed è utile per impedire l'inserimento di elementi quando si esegue il mapping di una singola immagine in un oggetto. \_La ripetizione GL fa sì che la parte intera della coordinata s venga ignorata. OpenGL usa solo la parte frazionaria, creando così un modello ripetuto. Gli elementi di trama del bordo sono accessibili solo se il wrapping è impostato sul \_ morsetto GL. Inizialmente, GL \_ texture \_ Wrap \_ S è impostato su GL \_ Repeat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_wrapping trama \_ GL \_ T**</dt> </dl>             | Imposta il parametro Wrap per la coordinata di trama t su un \_ morsetto GL o una \_ ripetizione GL. Vedere la discussione in GL \_ trama \_ Wrap \_ S. Inizialmente, GL \_ texture \_ Wrap \_ T è impostato su GL \_ Repeat<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore di *pname*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ \_enumerazione non valida**</dt> </dl>     | *target* o *pname* non è uno dei valori definiti accettati oppure quando *param* deve avere un valore costante definito (in base al valore di *pname*) e no.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Commenti

Il mapping di trama è una tecnica che applica un'immagine alla superficie di un oggetto come se l'immagine fosse una decalcomania o una compattazione di cellophane. L'immagine viene creata nello spazio di trama con un sistema di coordinate (*s*, *t*). Una trama è un'immagine a una o due dimensioni e un set di parametri che determinano la modalità di derivazione degli esempi dall'immagine.

La funzione **glTexParameter** assegna il valore o i valori in params al parametro texture specificato come pname. Il parametro target definisce la trama di destinazione, ovvero GL \_ texture \_ 1D o GL \_ texture \_ 2D.

Poiché nel processo minification vengono campionati più elementi di trama, saranno evidenti meno artefatti di aliasing. Sebbene le \_ funzioni GL più vicine e GL \_ Linear minification possano essere più veloci delle altre quattro, campionano solo uno o quattro elementi di trama per determinare il valore di trama del pixel di cui viene eseguito il rendering e possono produrre modelli moiré o transizioni incomplete. Il valore predefinito del \_ filtro di trama \_ min è GL \_ \_ più vicino \_ MIPMAP \_ lineare.

Si supponga che la funzionalità di texturing sia abilitata (chiamando [**glEnable**](glenable.md) con argomento GL \_ texture \_ 1D o GL \_ texture \_ 2D) e \_ \_ \_ il filtro di trama GL min sia impostato su una delle funzioni che richiedono un mipmap. Se le dimensioni delle immagini di trama attualmente definite (con chiamate precedenti a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md)) non seguono la sequenza corretta per mipmap o se sono presenti meno immagini di trama definite rispetto a quelle necessarie o se il set di immagini di trama presenta numeri diversi di componenti di trama, è come se il mapping della trama fosse disabilitato. Il filtro lineare accede ai quattro elementi di trama più vicini solo nelle trame 2D. Nelle trame da 1 a, il filtro lineare accede ai due elementi di trama più vicini. La funzione seguente recupera le informazioni relative a **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** e **glTexParameteriv**:

[**glGetTexParameter**](glgettexparameter.md)

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





