---
title: Funzione glTexParameterf (Gl.h)
description: Imposta i parametri della trama. | Funzione glTexParameterf (Gl.h)
ms.assetid: 20b9f2d5-66e1-41cd-9571-8caa38ef033d
keywords:
- Funzione glTexParameterf OpenGL
topic_type:
- apiref
api_name:
- glTexParameterf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1258eee2f9fa706fb4a855ef31b283a0449ad891bc9995a98acc9b3c4f49abd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490111"
---
# <a name="gltexparameterf-function"></a>Funzione glTexParameterf

Imposta i parametri della trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexParameterf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
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

Nome simbolico di un singolo parametro di trama con valore. I simboli seguenti sono accettati in *pname*.



| Valore                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN TRAMA GL \_ \_ \_**</dt> </dl> | La funzione di minimizzazione della trama viene usata ogni volta che il pixel di cui viene eseguito il mapping viene mappato a un'area maggiore di un elemento della trama. Sono disponibili sei funzioni di minimizzazione definite. Due di essi usano l'uno o quattro elementi di trama più vicini per calcolare il valore della trama. Le altre quattro usano mipmap.<br/> Un mipmap è un set ordinato di matrici che rappresenta la stessa immagine a risoluzioni progressivamente inferiori. Se la trama ha dimensioni 2nx2<sup>m,</sup> sono presenti max(n, m) + 1 mipmap. Il primo mipmap è la trama originale, con dimensioni 2nx2<sup>m</sup>. Ogni mipmap successivo ha dimensioni 2<sup>k</sup>1x2<sup>l</sup>1 dove 2<sup>k</sup>x2<sup>l</sup> sono le dimensioni del mipmap precedente, fino a k = 0 o l = 0. A questo punto, le mipmap successive hanno dimensione 1x2<sup>l</sup>1 o 2<sup>k</sup>1x1 fino alla mipmap finale, con dimensione 1x1. Le mipmap vengono definite usando [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md) con l'argomento level-of-detail che indica l'ordine delle mipmap. Il livello 0 è la trama originale. level bold max(n, m) è l'ultimo mipmap 1x1.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO \_ MAG \_ TRAMA GL \_**</dt> </dl> | La funzione di ingrandimento della trama viene usata quando il pixel di cui viene eseguito il mapping viene mappato a un'area minore o uguale a un elemento della trama. Imposta la funzione di ingrandimento della trama su GL \_ NEAREST o GL \_ LINEAR.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>             | Imposta il parametro wrap per le coordinate della trama su GL \_ CLAMP o GL \_ REPEAT. GL CLAMP fa sì che le coordinate s siano ancorate all'intervallo \_ 0,1 ed è utile per impedire il wrapping degli elementi quando si esegue il mapping di una singola immagine in \[ \] un oggetto. GL \_ REPEAT fa sì che la parte intera della coordinata s sia ignorata. OpenGL usa solo la parte frazionaria, creando così un modello ripetuto. Gli elementi della trama del bordo sono accessibili solo se il ritorno a capo è impostato su GL \_ CLAMP. Inizialmente, GL \_ TEXTURE WRAP S è impostato su GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>             | Imposta il parametro wrap per la coordinata della trama t su GL \_ CLAMP o GL \_ REPEAT. Vedere la discussione in GL \_ TEXTURE \_ WRAP \_ S. Inizialmente, GL \_ TEXTURE WRAP T è impostato su GL \_ \_ \_ REPEAT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*param* 
</dt> <dd>

Valore di *pname*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ENUMERAZIONE \_ NON VALIDA**</dt> </dl>     | *target* o *pname* non è uno dei valori definiti accettati oppure quando *param* deve avere un valore costante definito (in base al valore *di pname*) e non lo ha fatto.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Commenti

Il mapping delle trame è una tecnica che applica un'immagine alla superficie di un oggetto come se l'immagine fosse una decalcola o un ritorno a capo automatico della cellophane. L'immagine viene creata nello spazio della trama, con un sistema di coordinate (*s*, *t*). Una trama è un'immagine unidimensionale o bidimensionale e un set di parametri che determinano la modalità di derivazione dei campioni dall'immagine.

La **funzione glTexParameter** assegna il valore o i valori nei parametri al parametro texture specificato come pname. Il parametro target definisce la trama di destinazione, GL \_ TEXTURE \_ 1D o GL \_ TEXTURE \_ 2D.

Quando più elementi di trama vengono campionati nel processo di minimicazione, sarà evidente un minor numero di artefatti di aliasing. Anche se le funzioni di minimizzare GL NEAREST e GL LINEAR possono essere più veloci delle altre quattro, campionano solo uno o quattro elementi della trama per determinare il valore della trama del pixel sottoposto a rendering e possono produrre modelli di moire o transizioni \_ \_ instabili. Il valore predefinito di GL \_ TEXTURE MIN FILTER è GL NEAREST \_ \_ \_ \_ MIPMAP \_ LINEAR.

Si supponga che la trama sia abilitata (chiamando [**glEnable**](glenable.md) con l'argomento GL TEXTURE 1D o GL TEXTURE 2D) e GL TEXTURE MIN FILTER sia impostata su una delle funzioni che richiedono un \_ \_ \_ \_ \_ \_ \_ mipmap. Se le dimensioni delle immagini di trama attualmente definite (con le chiamate precedenti a [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D)**](glteximage2d.md)non seguono la sequenza corretta per le mipmap oppure se sono definite meno immagini di trama di quelle necessarie o se il set di immagini di trama ha un numero diverso di componenti della trama, è come se il mapping delle trame fosse disabilitato. Il filtro lineare accede ai quattro elementi di trama più vicini solo nelle trame 2D. Nelle trame 1D, il filtro lineare accede ai due elementi di trama più vicini. La funzione seguente recupera informazioni correlate a **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** e **glTexParameteriv**.

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

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





