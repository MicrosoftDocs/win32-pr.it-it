---
title: funzione glTexParameterfv (GL. h)
description: Imposta i parametri della trama. | funzione glTexParameterfv (GL. h)
ms.assetid: 29aa2823-5c73-48f1-891f-018dd7a93323
keywords:
- funzione glTexParameterfv OpenGL
topic_type:
- apiref
api_name:
- glTexParameterfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74c9ee0a9a1c75c50d96c90f1612b891eed282
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321510"
---
# <a name="gltexparameterfv-function"></a>glTexParameterfv (funzione)

Imposta i parametri della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexParameterfv(
         GLenum  target,
         GLenum  pname,
   const GLfloat *params
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



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_ \_ Filtro minimo trama \_ GL**</dt> </dl>       | La funzione minimizzazione di trama viene utilizzata ogni volta che il pixel con trama viene mappato a un'area maggiore di un elemento texture. Sono disponibili sei funzioni minimizzazione definite. Due di essi utilizzano i quattro elementi di trama più vicini o più vicini per calcolare il valore di trama. Gli altri quattro usano mipmap. <br/> Un mipmap è un set ordinato di matrici che rappresentano la stessa immagine in risoluzioni progressivamente inferiori. Se la trama ha dimensioni 2nx2<sup>m</sup> sono disponibili max (n, m) + 1 mipmap. Il primo mipmap è la trama originale, con dimensioni 2nx2<sup>m</sup>. Ogni mipmap successiva ha dimensioni 2<sup>k</sup>1x2<sup>l</sup>1 dove 2<sup>k</sup>X2<sup>l</sup> sono le dimensioni del mipmap precedente, fino a k = 0 o l = 0. A questo punto, mipmap successivi hanno la dimensione 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 fino alla mipmap finale, che ha la dimensione 1x1. Mipmap vengono definiti usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con l'argomento del livello di dettaglio che indica l'ordine del mipmap. Il livello 0 è la trama originale; il livello max Bold (n, m) è il mipmap 1x1 finale.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_ \_ filtro mag trama di contabilità \_**</dt> </dl>       | La funzione di ingrandimento della trama viene utilizzata quando il pixel con trama viene mappato a un'area minore o uguale a un elemento texture. Imposta la funzione di ingrandimento della trama su GL \_ più vicino o su GL \_ lineare.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_wrapping di trama GL \_ \_**</dt> </dl>                   | Imposta il parametro Wrap per le coordinate di trama su GL \_ clamp o GL \_ Repeat. \_Il morsetto GL causa il fissaggio delle coordinate a nell'intervallo \[ 0, 1 \] ed è utile per impedire l'inserimento di elementi quando si esegue il mapping di una singola immagine in un oggetto. \_La ripetizione GL fa sì che la parte intera della coordinata s venga ignorata. OpenGL usa solo la parte frazionaria, creando così un modello ripetuto. Gli elementi di trama del bordo sono accessibili solo se il wrapping è impostato sul \_ morsetto GL. Inizialmente, GL \_ texture \_ Wrap \_ S è impostato su GL \_ Repeat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_wrapping trama \_ GL \_ T**</dt> </dl>                   | Imposta il parametro Wrap per la coordinata di trama t su un \_ morsetto GL o una \_ ripetizione GL. Vedere la discussione in GL \_ trama \_ Wrap \_ S. Inizialmente, GL \_ texture \_ Wrap \_ T viene impostato su GL \_ Repeat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**\_ \_ colore bordo trama \_ GL**</dt> </dl> | Imposta il colore del bordo. Il parametro *params* contiene quattro valori che comprendono il colore RGBA del bordo della trama. I componenti dei colori integer vengono interpretati in modo lineare, in modo che il numero intero positivo sia mappato a 1,0 e l'intero più negativo sia mappato a 1,0. I valori vengono fissati nell'intervallo compreso tra \[ 0 e 1 \] quando vengono specificati. Inizialmente, il colore del bordo è (0, 0, 0, 0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_priorità trama \_ GL**</dt> </dl>              | Specifica la priorità di residenza della trama della trama attualmente associata. I valori consentiti sono compresi nell'intervallo compreso tra \[ 0 e 1 \] . Per ulteriori informazioni, vedere [**glPrioritizeTextures**](glprioritizetextures.md) e [**glBindTexture**](glbindtexture.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*params* 
</dt> <dd>

Puntatore a una matrice in cui vengono archiviati il valore o i valori di pname. Il parametro params fornisce una funzione per minimizzazione la trama come uno dei seguenti.



| Valore                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ PIÙ vicino**</dt> </dl>                                             | Restituisce il valore dell'elemento texture più vicino (a Manhattan distance) al centro del pixel che si sta tramando. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**\_linea GL**</dt> </dl>                                                   | Restituisce la media ponderata dei quattro elementi di trama più vicini al centro del pixel che si sta tramando. Possono includere elementi di trama del bordo, a seconda dei valori della \_ trama GL \_ Wrap \_ S, della \_ trama GL \_ Wrap \_ T e del mapping esatto. GL \_ più vicino è in genere più veloce rispetto a GL \_ lineare, ma può produrre immagini con trama con spigoli più nitidi perché la transizione tra gli elementi della trama non è uniforme. Il valore predefinito di GL \_ texture \_ mag \_ Filter è GL \_ Linear.<br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <dt>**GL \_ più vicino \_ MIPMAP \_ più vicino**</dt> </dl> | Sceglie il mipmap che corrisponde maggiormente alla dimensione del pixel che si sta tramando e usa il \_ criterio di stima più vicino (l'elemento di trama più vicino al centro del pixel) per produrre un valore di trama. <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <dt>**\_MIPMAP lineare \_ \_ più vicino**</dt> </dl>    | Consente di scegliere il mipmap che corrisponde maggiormente alla dimensione del pixel che si sta tramando e usa il \_ criterio lineare GL, ovvero una media ponderata dei quattro elementi di trama più vicini al centro del pixel, per produrre un valore di trama. <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <dt>**GL \_ più vicino \_ MIPMAP \_ lineare**</dt> </dl>    | Sceglie le due mipmap che corrispondono maggiormente alla dimensione del pixel che si sta tramando e usa il criterio di ricerca \_ più vicino (l'elemento di trama più vicino al centro del pixel) per produrre un valore di trama da ogni mipmap. Il valore di trama finale è una media ponderata dei due valori. <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <dt>**\_MIPMAP lineare \_ lineare \_**</dt> </dl>       | Sceglie le due mipmap che corrispondono maggiormente alla dimensione del pixel che si sta tramando e usa il \_ criterio linea GL (una media ponderata dei quattro elementi di trama più vicini al centro del pixel) per produrre un valore di trama da ogni mipmap. Il valore di trama finale è una media ponderata dei due valori.<br/>                                                                                                                                                                    |



 

Il parametro *params* fornisce una funzione per ingrandire la trama come uno dei seguenti.



| Valore                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ PIÙ vicino**</dt> </dl> | Restituisce il valore dell'elemento texture più vicino (a Manhattan distance) al centro del pixel che si sta tramando. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**\_linea GL**</dt> </dl>       | Restituisce la media ponderata dei quattro elementi di trama più vicini al centro del pixel che si sta tramando. Possono includere elementi di trama del bordo, a seconda dei valori della \_ trama GL \_ Wrap \_ S, della \_ trama GL \_ Wrap \_ T e del mapping esatto. GL \_ più vicino è in genere più veloce rispetto a GL \_ lineare, ma può produrre immagini con trama con spigoli più nitidi perché la transizione tra gli elementi della trama non è uniforme. Il valore predefinito di GL \_ texture \_ mag \_ Filter è GL \_ Linear.<br/> |



 

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

 

 





