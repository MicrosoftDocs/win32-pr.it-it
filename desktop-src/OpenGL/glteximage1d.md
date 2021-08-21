---
title: Funzione glTexImage1D (Gl.h)
description: La funzione glTexImage1D specifica un'immagine di trama unidimensionale.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- Funzione glTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd443389439b6d012533d3184739dfa849d672d76a8eced0e8ea244601d4122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490251"
---
# <a name="glteximage1d-function"></a>Funzione glTexImage1D

La **funzione glTexImage1D** specifica un'immagine di trama unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione. Deve essere GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio. Il livello 0 è il livello dell'immagine di base. Il *livello n* è *l'immagine n* Th mipmap reduction.

</dd> <dt>

*internalformat* 
</dt> <dd>

Specifica il numero di componenti di colore nella trama. Deve essere 1, 2, 3 o 4 oppure una delle costanti simboliche seguenti: GL \_ ALPHA, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ LUMINANCE, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, \_ GL LUMINANCE16, \_ GL LUMINANCE \_ ALPHA, GL \_ LUMINANCE4 \_ \_ ALPHA4, GL \_ LUMINANCE6 ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ INTENSITY, GL INTENSITY, GL INTENSITY GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ \_ RGB, GL \_ R3 G3 \_ B2, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ A1, GL \_ RGBA8, GL \_ RGB10 \_ A2, GL \_ RGBA12 o GL \_ RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine della trama. Deve essere 2 *n* + 2( *border* ) per un numero intero *n*. L'altezza dell'immagine della trama è 1.

</dd> <dt>

*confine* 
</dt> <dd>

Larghezza del bordo. Deve essere 0 o 1.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Può presupporre uno dei nove valori simbolici.



| Valore                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**INDICE COLORI \_ GL \_**</dt> </dl>             | Ogni elemento è un singolo valore, un indice di colore. Viene convertito in punto fisso (con un numero non specificato di 0 bit a destra del punto binario), spostato a sinistra o a destra, a seconda del valore e del segno di GL INDEX SHIFT e aggiunto a \_ \_ GL INDEX OFFSET \_ \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)). L'indice risultante viene convertito in un set di componenti di colore usando le tabelle GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B e GL PIXEL MAP I TO A e con un intervallo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ di \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1. \]<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Ogni elemento è un singolo componente rosso. Viene convertito in virgola mobile e assemblato in un elemento RGBA associando 0,0 per verde e blu e 1,0 per alfa. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ VERDE**</dt> </dl>                                | Ogni elemento è un singolo componente verde. Viene convertito in virgola mobile e assemblato in un elemento RGBA associando 0,0 per il rosso e il blu e 1,0 per alfa. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLU**</dt> </dl>                                   | Ogni elemento è un singolo componente blu. Viene convertito in virgola mobile e assemblato in un elemento RGBA associando 0,0 per il rosso e il verde e 1,0 per alfa. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Ogni elemento è un singolo componente rosso. Viene convertito in virgola mobile e assemblato in un elemento RGBA associando 0,0 per rosso, verde e blu. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Ogni elemento è una tripla RGB. Viene convertito in virgola mobile e assemblato in un elemento RGBA associando 1.0 per alpha. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Ogni elemento è un elemento RGBA completo. Viene convertito in virgola mobile. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ EXT**</dt> </dl>                         | Ogni pixel è un gruppo di tre componenti nell'ordine seguente: blu, verde, rosso.<br/> GL BGR EXT offre un formato che corrisponde al layout di memoria Windows bitmap indipendenti \_ \_ dal dispositivo (DIB). Le applicazioni possono quindi usare gli stessi dati con Windows di funzione e chiamate di funzione pixel OpenGL.<br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ EXT**</dt> </dl>                      | Ogni pixel è un gruppo di quattro componenti nell'ordine seguente: blu, verde, rosso, alfa.<br/> GL BGRA EXT offre un formato che corrisponde al layout di memoria \_ Windows bitmap indipendenti dal dispositivo \_ (DIB). Le applicazioni possono quindi usare gli stessi dati con Windows di funzione e chiamate di funzione pixel OpenGL.<br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Ogni elemento è un singolo valore di luminance. Viene convertito in virgola mobile e quindi assemblato in un elemento RGBA replicando il valore di luminance tre volte per il rosso, il verde e il blu e collegando 1,0 per alpha. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Ogni elemento è una coppia luminance/alpha. Viene convertito in virgola mobile e quindi assemblato in un elemento RGBA replicando il valore di luminance tre volte per rosso, verde e blu. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati dei dati pixel. Vengono accettati i valori simbolici seguenti: GL \_ UNSIGNED \_ BYTE, GL \_ BYTE, GL \_ BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT e GL \_ FLOAT.

</dd> <dt>

*Pixel* 
</dt> <dd>

Puntatore ai dati dell'immagine in memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *la destinazione* non è una TEXTURE \_ GL.<br/>                                                                                                                                                                                    |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *format* non è una costante di *formato accettata.* Vengono accettate solo costanti di formato diverse da GL \_ STENCIL INDEX e GL DEPTH \_ \_ \_ COMPONENT. Per un elenco dei valori *possibili, vedere* la descrizione del parametro format.<br/> |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *type* non è una *costante di* tipo.<br/>                                                                                                                                                                                   |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *il tipo* era GL \_ BITMAP e il *formato* non era GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                        |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o maggiore di log2 *max,* dove *max* è il valore restituito di GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                                 |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *internalformat* non era 1, 2, 3 o 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* è minore di zero o maggiore di 2 + GL MAX TEXTURE SIZE oppure non può essere rappresentato come \_ \_ \_ 2 *n* + 2(border) per un valore intero di n .<br/>                                                            |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *border* non è 0 o 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                          |



## <a name="remarks"></a>Commenti

La **funzione glTexImage1D** specifica un'immagine di trama unidimensionale. La trama esegue il mapping di una parte di un'immagine *di trama specificata* a ogni primitiva grafica per cui è abilitata la trama. La texturing unidimensionale è abilitata e disabilitata usando [**glEnable**](glenable.md) **e glDisable con** l'argomento GL \_ TEXTURE \_ 1D.

Le immagini di trama sono definite **con glTexImage1D.** Gli argomenti descrivono i parametri dell'immagine della trama, ad esempio larghezza, larghezza del bordo, numero di livello di dettaglio (vedere [**glTexParameter)**](gltexparameter-functions.md)e numero di componenti di colore forniti. Gli ultimi tre argomenti descrivono il modo in cui l'immagine viene rappresentata in memoria. Questi argomenti sono identici ai formati pixel usati per [**glDrawPixels.**](gldrawpixels.md)

I dati vengono letti dai *pixel* come sequenza di byte con o senza segno, short o long o valori a virgola mobile e precisione singola, a seconda *del tipo*. Questi valori sono raggruppati in set di uno, due, tre o quattro valori, a seconda del *formato*, per formare gli elementi. Se *type* è GL BITMAP, i dati vengono considerati come una stringa di byte senza segno \_ (e il *formato* deve essere GL \_ COLOR \_ INDEX). Ogni byte di dati viene considerato come otto elementi a 1 bit, con ordinamento dei bit determinato da GL \_ UNPACK \_ LSB \_ FIRST (vedere [**glPixelStore).**](glpixelstore-functions.md)

Un'immagine di trama può avere fino a quattro componenti per ogni elemento della trama, a seconda dei *componenti*. Un'immagine di trama a un componente usa solo il componente rosso del colore RGBA estratto dai *pixel*. Un'immagine a due componenti usa i valori R e A. Un'immagine a tre componenti usa i valori R, G e B. Un'immagine a quattro componenti usa tutti i componenti RGBA.

La colorazione non ha alcun effetto in modalità color-index.

L'immagine della trama può essere rappresentata dagli stessi formati di dati dei pixel in un [**comando glDrawPixels,**](gldrawpixels.md) ad eccezione del fatto che non è possibile usare GL STENCIL INDEX e \_ GL DEPTH \_ \_ \_ COMPONENT. Le [**modalità glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono esattamente sulle immagini di trama nel modo in cui influiscono **su glDrawPixels.**

Un'immagine di trama con larghezza zero indica la trama Null. Se la trama Null viene specificata per il livello di dettaglio 0, è come se la trama fosse disabilitata.

Le funzioni seguenti recuperano informazioni correlate **a glTexImageID:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE \_ 1D

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





