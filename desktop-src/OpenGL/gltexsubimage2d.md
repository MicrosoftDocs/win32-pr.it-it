---
title: funzione glTexSubImage2D (GL. h)
description: La funzione glTexSubImage2D specifica una parte di un'immagine di trama unidimensionale esistente. Non è possibile definire una nuova trama con glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- funzione glTexSubImage2D OpenGL
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
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300953"
---
# <a name="gltexsubimage2d-function"></a>glTexSubImage2D (funzione)

La funzione **glTexSubImage2D** specifica una parte di un'immagine di trama unidimensionale esistente. Non è possibile definire una nuova trama con **glTexSubImage2D**.

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

Trama di destinazione. Deve essere di \_ trama GL \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

Numero del livello di dettaglio. Il livello 0 è l'immagine di base. Il livello *n* è l'immagine di riduzione del mipmap *n*.

</dd> <dt>

*xoffset* 
</dt> <dd>

Offset di Texel nella direzione *x* all'interno della matrice di trame.

</dd> <dt>

*yoffset* 
</dt> <dd>

Offset di Texel nella direzione *y* all'interno della matrice di trame.

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

Formato dei dati pixel. Può assumere uno dei seguenti valori simbolici.



| Valore                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_indice colori \_ GL**</dt> </dl>             | Ogni elemento è un singolo valore, ovvero un indice colori. Viene convertito in un formato a virgola fissa (con un numero non specificato di 0 bit a destra del punto binario), spostato a sinistra o a destra, a seconda del valore e del segno dello \_ spostamento di indice GL \_ e aggiunto all' \_ offset dell'indice GL \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)). L'indice risultante viene convertito in un set di componenti colore usando il \_ mapping GL pixel i \_ \_ \_ a \_ R, GL \_ pixel \_ Map \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ mappa \_ i \_ a \_ una tabella e l'intervallo viene premuto nell'intervallo \[ 0, 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**\_rosso GL**</dt> </dl>                                      | Ogni elemento è un singolo componente rosso. Viene convertita in formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per verde e blu e 1,0 per alfa. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**\_verde GL**</dt> </dl>                                | Ogni elemento è un singolo componente verde. Viene convertita in formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Blue e 1,0 per Alpha. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_blu GL**</dt> </dl>                                   | Ogni elemento è un singolo componente blu. Viene convertita nel formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per il rosso e il verde e 1,0 per Alpha. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**\_alfa GL**</dt> </dl>                                | Ogni elemento è un singolo componente alfa. Viene convertita in formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per rosso, verde e blu. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Ogni elemento è una tripla RGB. Viene convertita nel formato a virgola mobile e assemblata in un elemento RGBA collegando 1,0 per Alpha. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**\_RGBA GL**</dt> </dl>                                   | Ogni elemento è un elemento RGBA completo. Viene convertito in virgola mobile. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**\_luminanza GL**</dt> </dl>                    | Ogni elemento è un singolo valore di luminosità. Viene convertita in formato a virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu e collegando 1,0 per alfa. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**\_alfa luminanza GL \_**</dt> </dl> | Ogni elemento è una coppia di luminanza/alfa. Viene convertita in formato a virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati dei dati pixel. Sono accettati i valori simbolici seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.

</dd> <dt>

*pixel* 
</dt> <dd>

Puntatore ai dati dell'immagine in memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *destinazione* non è la \_ trama GL \_ 2D.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Format* non è una costante accettata.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* non è una costante accettata.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* è una \_ bitmap GL e *Format* non è un indice di \_ colore GL \_ .<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *xoffset* è minore di-*b*; la   +  *larghezza* xoffset è maggiore di *w*  -  *b* oppure *yoffset* è minore di-*b* oppure l'   +  *altezza* di yoffset è maggiore di *h*  -  *b*, dove *w* è la \_ larghezza della trama GL \_ , *h* è l' \_ altezza della trama GL \_ e *b* è la larghezza del bordo della \_ trama GL \_ dell'immagine della trama da modificare. <br/> Si noti che *w* e *h* includono due volte lo spessore del bordo.<br/> |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *Width* era minore di *b*, dove *b* è lo spessore del bordo della matrice di trame.<br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *bordo* non è zero o 1.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La matrice di trama non è stata definita da un'operazione **glTexImage2D** precedente.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a>Commenti

Il texturing bidimensionale per una primitiva viene abilitato con [**glEnable**](glenable.md) e **glDisable** con l'argomento di \_ trama GL \_ 2D. Durante la texturing, una parte di un'immagine di trama specificata viene mappata in ogni primitiva abilitata. Usare la funzione **glTexSubImage2D** per specificare un'immagine secondaria contigua di un'immagine di trama bidimensionale esistente per la texturing.

I Texel a cui fanno riferimento i *pixel* sostituiscono un'area della matrice di trama esistente con gli indici *x* di *xoffset* e *xoffset* + (*Width* 1) inclusivi e gli indici *y* di *yoffset* e *yoffset* + (*Height* 1) inclusi. Questa area non può includere Texel non compresi nell'intervallo della matrice di trama originariamente specificata.

La specifica di un'immagine secondaria con una *larghezza* pari a zero non ha alcun effetto e non genera un errore.

La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.

In generale, le immagini di trama possono essere rappresentate dagli stessi formati di dati dei pixel in un comando [**glDrawPixels**](gldrawpixels.md) , ad eccezione del fatto che \_ \_ \_ \_ non è possibile usare l'indice degli stencil GL e il componente profondità GL. Le modalità [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su **glDrawPixels**.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexSubImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) con argomento di \_ trama GL \_ 2D

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

 

 





