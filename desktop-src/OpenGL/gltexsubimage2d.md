---
title: Funzione glTexSubImage2D (Gl.h)
description: La funzione glTexSubImage2D specifica una parte di un'immagine di trama unidimensionale esistente. Non è possibile definire una nuova trama con glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- Funzione glTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c568afbe63ab01bd2866f180f968ea80101fec2ff22062707f4929d662ea47ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519701"
---
# <a name="gltexsubimage2d-function"></a>Funzione glTexSubImage2D

La **funzione glTexSubImage2D** specifica una parte di un'immagine di trama unidimensionale esistente. Non è possibile definire una nuova trama **con glTexSubImage2D.**

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione. Deve essere GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numero di livello di dettaglio. Il livello 0 è l'immagine di base. Il *livello n* è *l'esima* immagine di riduzione mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Offset texel nella direzione *x* all'interno della matrice di trame.

</dd> <dt>

*yoffset* 
</dt> <dd>

Offset texel nella direzione *y* all'interno della matrice di trame.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine secondaria della trama.

</dd> <dt>

*height* 
</dt> <dd>

Altezza dell'immagine secondaria della trama.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Può presupporre uno dei valori simbolici seguenti.



| Valore                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**INDICE COLORI GL \_ \_**</dt> </dl>             | Ogni elemento è un singolo valore, un indice di colore. Viene convertito in formato a virgola fissa (con un numero non specificato di 0 bit a destra del punto binario), spostato a sinistra o a destra, a seconda del valore e del segno di GL INDEX SHIFT e aggiunto a \_ \_ GL INDEX OFFSET \_ \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)). L'indice risultante viene convertito in un set di componenti di colore usando le tabelle GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B e GL PIXEL MAP I TO A e con un intervallo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ di \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1. \]<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Ogni elemento è un singolo componente rosso. Viene convertito in formato a virgola mobile e assemblato in un elemento RGBA associando 0,0 per il verde e il blu e 1,0 per alfa. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ VERDE**</dt> </dl>                                | Ogni elemento è un singolo componente verde. Viene convertito in formato a virgola mobile e assemblato in un elemento RGBA associando 0,0 per il rosso e il blu e 1,0 per alfa. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLU**</dt> </dl>                                   | Ogni elemento è un singolo componente blu. Viene convertito in formato a virgola mobile e assemblato in un elemento RGBA associando 0,0 per il rosso e il verde e 1,0 per alfa. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Ogni elemento è un singolo componente alfa. Viene convertito in formato a virgola mobile e assemblato in un elemento RGBA associando 0,0 per il rosso, il verde e il blu. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Ogni elemento è una tripla RGB. Viene convertito in formato a virgola mobile e assemblato in un elemento RGBA associando 1.0 per alpha. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Ogni elemento è un elemento RGBA completo. Viene convertito in virgola mobile. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Ogni elemento è un singolo valore di luminance. Viene convertito in formato a virgola mobile e quindi assemblato in un elemento RGBA replicando il valore di luminance tre volte per il rosso, il verde e il blu e collegando 1,0 per alpha. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Ogni elemento è una coppia luminance/alpha. Viene convertito in formato a virgola mobile e quindi assemblato in un elemento RGBA replicando il valore di luminance tre volte per rosso, verde e blu. Ogni componente viene quindi moltiplicato per il fattore di scala con segno GL c SCALE, aggiunto alla distorsione con segno GL c BIAS e viene aggiunto all'intervallo \_ \_ \_ \_ \[ 0,1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

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



| Nome                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *la destinazione* non era GL \_ TEXTURE \_ 2D.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *format* non è una costante accettata.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *il tipo* non è una costante accettata.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *il tipo* era GL \_ BITMAP e il *formato* non era GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *level* è minore di zero o maggiore di log2 *max*, dove *max* è il valore restituito di GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *xoffset* è minore di -*b*; o *xoffset* width è maggiore di w b ; o yoffset è minore di - b ; o  +     -    *yoffset* height è maggiore di h b , dove w è GL TEXTURE WIDTH, h è GL TEXTURE HEIGHT e b è la larghezza di GL TEXTURE BORDER dell'immagine trama da  +     -    \_ \_  \_ \_  \_ \_ modificare. <br/> Si noti *che w* e *h* includono il doppio dello spessore del bordo.<br/> |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* era minore di *b*, dove *b* è la larghezza del bordo della matrice di trame.<br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *border* non è zero o 1.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La matrice di trame non è stata definita da **un'operazione glTexImage2D** precedente.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a>Commenti

La texturing bidimensionale per una primitiva è abilitata usando [**glEnable**](glenable.md) **e glDisable con** l'argomento GL \_ TEXTURE \_ 2D. Durante la trama, parte di un'immagine di trama specificata viene mappata a ogni primitiva abilitata. Usare la funzione **glTexSubImage2D** per specificare un'immagine secondaria contigua di un'immagine di trama bidimensionale esistente per la trama.

I texel a  cui fanno riferimento i pixel sostituiscono un'area della matrice di trame esistente con indici *x* di *xoffset* e *xoffset* + (*larghezza* 1) inclusi e indici *y* di *yoffset* e *yoffset* + (*altezza* 1) inclusi. Questa area non può includere texel non inclusi nell'intervallo della matrice di trame specificata in origine.

La specifica di un'immagine secondaria con *larghezza* pari a zero non ha alcun effetto e non genera un errore.

La colorazione non ha alcun effetto in modalità color-index.

In generale, le immagini di trama possono essere rappresentate dagli stessi formati di dati dei pixel in un [**comando glDrawPixels,**](gldrawpixels.md) ad eccezione del fatto che non è possibile usare GL STENCIL INDEX e \_ GL DEPTH \_ \_ \_ COMPONENT. Le [**modalità glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono esattamente sulle immagini di trama nel modo in cui influiscono **su glDrawPixels.**

Le funzioni seguenti recuperano informazioni correlate **a glTexSubImage2D:**

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ TEXTURE \_ 2D

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

[**glEnable**](glenable.md)
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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





