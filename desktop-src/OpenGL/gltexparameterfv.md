---
title: Funzione glTexParameterfv (Gl.h)
description: Imposta i parametri di trama. | Funzione glTexParameterfv (Gl.h)
ms.assetid: 29aa2823-5c73-48f1-891f-018dd7a93323
keywords:
- Funzione glTexParameterfv OpenGL
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
ms.openlocfilehash: 433a886ac7094a28e7c936eb02dd55743bf1abe6a94b128fb98b42bb1bad8335
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490061"
---
# <a name="gltexparameterfv-function"></a>Funzione glTexParameterfv

Imposta i parametri di trama.

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

Trama di destinazione, che deve essere GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico di un singolo parametro di trama con valori. I simboli seguenti vengono accettati in *pname*.



| Valore                                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN \_ \_ TRAME GL \_**</dt> </dl>       | La funzione di minificazione della trama viene usata ogni volta che il pixel di cui viene eseguito il mapping a un'area maggiore di un elemento di trama. Sono disponibili sei funzioni di minificazione definite. Due di essi usano uno o quattro elementi di trama più vicini per calcolare il valore della trama. Gli altri quattro usano mipmap. <br/> Un mipmap è un set ordinato di matrici che rappresenta la stessa immagine a risoluzioni progressivamente inferiori. Se la trama ha dimensioni 2nx2<sup>m,</sup> sono presenti max(n, m) + 1 mipmap. La prima mipmap è la trama originale, con dimensioni 2nx2<sup>m.</sup> Ogni mipmap successiva ha dimensioni 2<sup>k</sup>1x2<sup>l</sup>1, dove 2<sup>k</sup>x2<sup>l</sup> sono le dimensioni della mipmap precedente, fino a k = 0 o l = 0. A questo punto, le mipmap successive hanno la dimensione 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 fino alla mipmap finale, che ha dimensione 1x1. Le mipmap vengono definite usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con l'argomento level-of-detail che indica l'ordine delle mipmap. Il livello 0 è la trama originale. level bold max(n, m) è l'ultimo mipmap 1x1.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO MAG \_ \_ TRAMA \_ GL**</dt> </dl>       | La funzione di ingrandimento della trama viene usata quando il pixel di cui viene eseguito il mapping a un'area minore o uguale a un elemento di trama. Imposta la funzione di ingrandimento della trama su GL \_ NEAREST o GL \_ LINEAR.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_AVVOLGI \_ TRAMA GL \_ S**</dt> </dl>                   | Imposta il parametro wrap per le coordinate della trama su GL \_ CLAMP o GL \_ REPEAT. GL CLAMP fa sì che le coordinate s siano ancorate all'intervallo \_ 0,1 ed è utile per impedire il wrapping degli elementi quando si esegue il mapping di una singola immagine \[ \] su un oggetto. GL \_ REPEAT fa in modo che la parte intera della coordinata s sia ignorata. OpenGL usa solo la parte frazionaria, creando così un modello ripetuto. Gli elementi della trama del bordo sono accessibili solo se il ritorno a capo è impostato su GL \_ CLAMP. Inizialmente, GL \_ TEXTURE WRAP S è impostato su GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Imposta il parametro wrap per la coordinata di trama t su GL \_ CLAMP o GL \_ REPEAT. Vedere la discussione in GL \_ TEXTURE \_ WRAP \_ S. Inizialmente, GL \_ TEXTURE WRAP T è impostato su GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**COLORE \_ BORDO \_ TRAMA \_ GL**</dt> </dl> | Imposta un colore del bordo. Il *parametro params* contiene quattro valori che costituiscono il colore RGBA del bordo della trama. I componenti di colore integer vengono interpretati in modo lineare in modo che il numero intero più positivo venga mappato a 1,0 e il numero intero più negativo venga mappato a 1,0. I valori vengono ancorati all'intervallo \[ 0,1 \] quando vengono specificati. Inizialmente, il colore del bordo è (0, 0, 0, 0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**PRIORITÀ \_ TRAME GL \_**</dt> </dl>              | Specifica la priorità di trame della trama attualmente associata. I valori consentiti sono nell'intervallo \[ 0, 1 \] . Per [**altre informazioni, vedere glPrioritizeTextures**](glprioritizetextures.md) e [**glBindTexture.**](glbindtexture.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*params* 
</dt> <dd>

Puntatore a una matrice in cui sono archiviati il valore o i valori di pname. Il parametro params fornisce una funzione per minimizzarne la trama come una delle seguenti.



| Valore                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**Gl \_ PIÙ VICINO**</dt> </dl>                                             | Restituisce il valore dell'elemento di trama più vicino (in distanza a New York) al centro del pixel da trame. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ LINEAR**</dt> </dl>                                                   | Restituisce la media ponderata dei quattro elementi di trama più vicini al centro del pixel da trame. Possono includere elementi di trama del bordo, a seconda dei valori di GL \_ TEXTURE \_ WRAP \_ S, GL TEXTURE WRAP \_ T e del mapping \_ \_ esatto. GL NEAREST è in genere più veloce di GL LINEAR, ma può produrre immagini trame con bordi più netti perché la transizione tra gli elementi della trama \_ \_ non è uniforme. Il valore predefinito di GL \_ TEXTURE MAG FILTER è GL \_ \_ \_ LINEAR.<br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <dt>**GL \_ PIÙ \_ VICINO MIPMAP \_**</dt> </dl> | Sceglie la mappa mipmap più vicina alle dimensioni del pixel da trame e usa il criterio GL NEAREST (l'elemento di trama più vicino al centro del pixel) per produrre un valore di \_ trama. <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <dt>**GL \_ LINEAR \_ MIPMAP \_ PIÙ VICINO**</dt> </dl>    | Sceglie la mappa mipmap più vicina alle dimensioni del pixel da trame e usa il criterio GL LINEAR (media ponderata dei quattro elementi di trama più vicini al centro del pixel) per produrre un valore di \_ trama. <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <dt>**LINEARE \_ \_ MIPMAP PIÙ \_ VICINA GL**</dt> </dl>    | Sceglie le due mipmap più vicine alle dimensioni del pixel da trame e usa il criterio GL NEAREST (l'elemento di trama più vicino al centro del pixel) per produrre un valore di trama da \_ ogni mipmap. Il valore finale della trama è una media ponderata di questi due valori. <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <dt>**GL \_ LINEAR \_ MIPMAP \_ LINEAR**</dt> </dl>       | Sceglie le due mipmap più vicine alle dimensioni del pixel da trame e usa il criterio GL LINEAR (media ponderata dei quattro elementi di trama più vicini al centro del pixel) per produrre un valore di trama da ogni \_ mipmap. Il valore finale della trama è una media ponderata di questi due valori.<br/>                                                                                                                                                                    |



 

Il *parametro params* fornisce una funzione per ingrandire la trama come una delle seguenti.



| Valore                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**Gl \_ PIÙ VICINO**</dt> </dl> | Restituisce il valore dell'elemento di trama più vicino (in distanza a New York) al centro del pixel da trame. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ LINEAR**</dt> </dl>       | Restituisce la media ponderata dei quattro elementi di trama più vicini al centro del pixel da trame. Possono includere elementi di trama del bordo, a seconda dei valori di GL \_ TEXTURE \_ WRAP \_ S, GL TEXTURE WRAP \_ T e del mapping \_ \_ esatto. GL NEAREST è in genere più veloce di GL LINEAR, ma può produrre immagini trame con bordi più netti perché la transizione tra gli elementi della trama \_ \_ non è uniforme. Il valore predefinito di GL \_ TEXTURE MAG FILTER è GL \_ \_ \_ LINEAR.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Gl \_ ENUMERAZIONE \_ NON VALIDA**</dt> </dl>     | *target* o *pname* non è uno dei valori definiti accettati o quando *param* deve avere un valore costante definito (in base al valore *di pname*) e non lo ha fatto.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Commenti

La mappatura trame è una tecnica che applica un'immagine sulla superficie di un oggetto come se l'immagine fosse una decal o cellophane shrink-wrap. L'immagine viene creata nello spazio trame, con un sistema di coordinate (*s*, *t*). Una trama è un'immagine unidimensionale o bidimensionale e un set di parametri che determinano la modalità di derivazione dei campioni dall'immagine.

La **funzione glTexParameter** assegna il valore o i valori in params al parametro texture specificato come pname. Il parametro di destinazione definisce la trama di destinazione, GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

Quando vengono campionati più elementi di trama nel processo di minificazione, sarà evidente un minor numero di artefatti di aliasing. Anche se le funzioni di minificazione GL NEAREST e GL LINEAR possono essere più veloci delle altre quattro, campionano solo uno o quattro elementi di trama per determinare il valore della trama del pixel sottoposto a rendering e possono produrre motivi di \_ \_ moire o transizioni instabili. Il valore predefinito di GL \_ TEXTURE MIN FILTER è GL NEAREST \_ \_ \_ \_ MIPMAP \_ LINEAR.

Si supponga che la texturing sia abilitata (chiamando [**glEnable**](glenable.md) con l'argomento GL TEXTURE 1D o GL TEXTURE 2D) e GL TEXTURE MIN FILTER sia impostato su una delle funzioni che richiedono \_ \_ un \_ \_ \_ \_ \_ mipmap. Se le dimensioni delle immagini di trama attualmente definite (con le chiamate precedenti a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D)**](glteximage2d.md)non seguono la sequenza corretta per le mipmap o sono definite meno immagini di trama di quelle necessarie o il set di immagini di trama ha un numero diverso di componenti della trama, è come se il mapping trame fosse disabilitato. Il filtro lineare accede ai quattro elementi di trama più vicini solo nelle trame 2D. Nelle trame 1D, il filtro lineare accede ai due elementi di trama più vicini. La funzione seguente recupera informazioni correlate a **glTexParameterf,** **glTexParameteri,** **glTexParameterfv** e **glTexParameteriv**:

[**glGetTexParameter**](glgettexparameter.md)

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

[**glEnd**](glend.md)
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

 

 





