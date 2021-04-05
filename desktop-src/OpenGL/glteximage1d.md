---
title: funzione glTexImage1D (GL. h)
description: La funzione glTexImage1D specifica un'immagine di trama unidimensionale.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- funzione glTexImage1D OpenGL
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
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048233"
---
# <a name="glteximage1d-function"></a>glTexImage1D (funzione)

La funzione **glTexImage1D** specifica un'immagine di trama unidimensionale.

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

Trama di destinazione. Deve essere una \_ trama GL \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

Numero del livello di dettaglio. Il livello 0 è il livello dell'immagine di base. Il livello *n* è l'immagine di riduzione del mipmap *n*.

</dd> <dt>

*internalformat* 
</dt> <dd>

Specifica il numero di componenti di colore nella trama. Deve essere 1, 2, 3 o 4 o una delle costanti simboliche seguenti: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL ALPHA12, GL ALPHA16, GL Luminance, GL LUMINANCE4, GL LUMINANCE8, GL LUMINANCE12, GL LUMINANCE16, GL \_ \_ \_ \_ \_ \_ \_ \_ Luminance \_ Alpha, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ alfa2, GL LUMINANCE8 \_ \_ ALPHA8, GL \_ LUMINANCE12 ALPHA4, \_ GL \_ LUMINANCE12 \_ ALPHA12, GL LUMINANCE16 ALPHA16, GL Intensity, GL INTENSITY4, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ INTENSITY8, GL INTENSITY12, GL INTENSITY16, GL RGB, GL RGB4, GL RGB5, GL RGB8, GL RGB10, GL RGB12, GL RGB16, GL RGBA, GL RGBA2, GL RGBA4, GL RGB5, GL Rgba8, GL RGB10 a1, GL RGBA12, GL RGBA16 a2, GL o GL.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'immagine della trama. Deve essere 2 *n* + 2 ( *bordo* ) per alcuni numeri interi *n*. L'altezza dell'immagine della trama è 1.

</dd> <dt>

*bordo* 
</dt> <dd>

Larghezza del bordo. Deve essere 0 o 1.

</dd> <dt>

*format* 
</dt> <dd>

Formato dei dati pixel. Può assumere uno dei nove valori simbolici.



| Valore                                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_indice colori \_ GL**</dt> </dl>             | Ogni elemento è un singolo valore, ovvero un indice colori. Viene convertito in un punto fisso (con un numero non specificato di 0 bit a destra del punto binario), spostato a sinistra o a destra, a seconda del valore e del segno dello spostamento di \_ indice GL \_ e aggiunto all'offset dell' \_ indice GL \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)). L'indice risultante viene convertito in un set di componenti colore usando il \_ mapping GL pixel i \_ \_ \_ a \_ R, GL \_ pixel \_ Map \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ mappa \_ i \_ a \_ una tabella e l'intervallo viene premuto nell'intervallo \[ 0, 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**\_rosso GL**</dt> </dl>                                      | Ogni elemento è un singolo componente rosso. Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per verde e blu e 1,0 per alfa. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**\_verde GL**</dt> </dl>                                | Ogni elemento è un singolo componente verde. Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Blue e 1,0 per Alpha. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_blu GL**</dt> </dl>                                   | Ogni elemento è un singolo componente blu. Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Green e 1,0 per Alpha. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**\_alfa GL**</dt> </dl>                                | Ogni elemento è un singolo componente rosso. Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per rosso, verde e blu. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Ogni elemento è una tripla RGB. Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 1,0 per Alpha. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**\_RGBA GL**</dt> </dl>                                   | Ogni elemento è un elemento RGBA completo. Viene convertito in virgola mobile. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ ext**</dt> </dl>                         | Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.<br/> GL \_ BGR \_ ext fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows. In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ ext**</dt> </dl>                      | Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.<br/> GL \_ BGRA \_ ext fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows. In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.<br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**\_luminanza GL**</dt> </dl>                    | Ogni elemento è un singolo valore di luminosità. Viene convertita in virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu e collegando 1,0 per alfa. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**\_alfa luminanza GL \_**</dt> </dl> | Ogni elemento è una coppia di luminanza/alfa. Viene convertita in virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu. Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

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



| Nome                                                                                                  | Significato                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *destinazione* non è una \_ trama GL.<br/>                                                                                                                                                                                    |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Format* non è una costante di *formato* accettata. Vengono accettate solo le costanti di formato diverse da GL \_ stencil \_ index e GL \_ Depth \_ Component. Vedere la descrizione del parametro *Format* per un elenco di valori possibili.<br/> |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* non è una costante di *tipo* .<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* è una \_ bitmap GL e *Format* non è un indice di \_ colore GL \_ .<br/>                                                                                                                                                        |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .<br/>                                                                                                 |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *internalformat* è diverso da 1, 2, 3 o 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *Width* è minore di zero o maggiore di 2 + GL \_ \_ dimensione della trama massima \_ oppure non può essere rappresentata come 2 *n* + 2 (bordo) per un valore integer pari a *n*.<br/>                                                            |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | il *bordo* non è 0 o 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                          |



## <a name="remarks"></a>Commenti

La funzione **glTexImage1D** specifica un'immagine di trama unidimensionale. Il texturing esegue il mapping di una parte di un' *immagine di trama* specificata a ogni primitiva grafica per cui è abilitata la funzionalità di texturing. Il texturing unidimensionale viene abilitato e disabilitato usando [**glEnable**](glenable.md) e **GLDISABLE** con argument GL \_ texture \_ 1D.

Le immagini di trama sono definite con **glTexImage1D**. Gli argomenti descrivono i parametri dell'immagine di trama, ad esempio larghezza, larghezza del bordo, numero del livello di dettaglio (vedere [**glTexParameter**](gltexparameter-functions.md)) e numero di componenti colore specificati. Gli ultimi tre argomenti descrivono il modo in cui l'immagine viene rappresentata in memoria. Questi argomenti sono identici ai formati pixel utilizzati per [**glDrawPixels**](gldrawpixels.md).

I dati vengono letti da *pixel* come una sequenza di byte firmati o non firmati, Shorts o Long o valori a virgola mobile a precisione singola, a seconda del *tipo*. Questi valori sono raggruppati in set di uno, due, tre o quattro valori, a seconda del *formato*, per formare elementi. Se *Type* è \_ una bitmap GL, i dati vengono considerati come una stringa di byte senza segno (e *Format* deve essere un \_ Indice dei colori GL \_ ). Ogni byte di dati viene considerato come elementi a 8 1 bit, con l'ordinamento dei bit determinato da GL \_ depack \_ LSB \_ First (vedere [**glPixelStore**](glpixelstore-functions.md)).

Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama, a seconda dei *componenti*. Un'immagine di trama a un componente usa solo il componente rosso del colore RGBA Estratto da *pixel*. Un'immagine a due componenti usa i valori R e. Un'immagine A tre componenti usa i valori R, G e B. Un'immagine a quattro componenti utilizza tutti i componenti di RGBA.

La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.

L'immagine di trama può essere rappresentata dagli stessi formati di dati dei pixel in un comando [**glDrawPixels**](gldrawpixels.md) , ad eccezione del fatto che \_ \_ \_ \_ non è possibile usare l'indice degli stencil GL e il componente di profondità GL. Le modalità [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su **glDrawPixels**.

Un'immagine di trama con larghezza zero indica la trama null. Se la trama null è specificata per il livello di dettaglio 0, è come se la texturing fosse disabilitata.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexImageID**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ 1D

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

[**Remo**](glend.md)
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

 

 





