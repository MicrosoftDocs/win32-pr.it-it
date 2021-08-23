---
title: Funzione glFeedbackBuffer (Gl.h)
description: La funzione glFeedbackBuffer controlla la modalità feedback.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- Funzione glFeedbackBuffer OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e51a08dac2bbf55509d4964218fc4b844581c797220294464b84c05de5e05b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580201"
---
# <a name="glfeedbackbuffer-function"></a>Funzione glFeedbackBuffer

La **funzione glFeedbackBuffer** controlla la modalità feedback.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*size* 
</dt> <dd>

Numero massimo di valori che possono essere scritti nel *buffer*.

</dd> <dt>

*type* 
</dt> <dd>

Costante simbolica che descrive le informazioni che verranno restituite per ogni vertice. Sono accettate le costanti simboliche seguenti: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ COLOR, GL \_ 3D \_ COLOR TEXTURE e GL \_ \_ 4D \_ COLOR \_ TEXTURE.

</dd> <dt>

*Buffer* 
</dt> <dd>

Restituisce i dati di feedback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *il* tipo non è un valore accettato.<br/>                                                                                                                                                                           |
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *size* è negativo.<br/>                                                                                                                                                                                        |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | **GlFeedbackBuffer** è stato chiamato mentre la modalità di rendering era GL FEEDBACK oppure glRenderMode è stato chiamato con l'argomento GL FEEDBACK prima \_ [](glrendermode.md) \_ che **glFeedbackBuffer** fosse chiamato almeno una volta.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                  |



## <a name="remarks"></a>Commenti

La **funzione glFeedbackBuffer** controlla i commenti e suggerimenti. Il feedback, ad esempio la selezione, è una modalità OpenGL. La modalità viene selezionata chiamando [**glRenderMode**](glrendermode.md) con GL \_ FEEDBACK. Quando OpenGL è in modalità feedback, la rasterizzazione non produce pixel. Le informazioni sulle primitive che sarebbero state rasterizzate vengono invece riportate all'applicazione usando OpenGL.

La **funzione glFeedbackBuffer** ha tre argomenti:

-   *buffer* è un puntatore a una matrice di valori a virgola mobile in cui vengono inserite le informazioni di feedback.
-   *size* indica le dimensioni della matrice.
-   *type* è una costante simbolica che descrive le informazioni restituite per ogni vertice.

È necessario rilasciare **glFeedbackBuffer prima** che sia abilitata la modalità feedback (chiamando **glRenderMode** con l'argomento GL \_ FEEDBACK). L'impostazione di GL FEEDBACK senza stabilire il buffer di feedback o chiamare \_ **glFeedbackBuffer** mentre OpenGL è in modalità feedback è un errore.

Per uscire dalla modalità feedback, OpenGL chiama [**glRenderMode**](glrendermode.md) con un valore di parametro diverso da GL \_ FEEDBACK. Quando si esegue questa operazione mentre OpenGL è in modalità feedback, **glRenderMode** restituisce il numero di voci inserite nella matrice feedback. Il valore restituito non supera mai *le dimensioni .* Se i dati di feedback richiedeva più spazio di quello disponibile nel *buffer*, **glRenderMode** restituisce un valore negativo.

In modalità feedback, ogni primitiva che verrebbe rasterizzata genera un blocco di valori che viene copiato nella matrice feedback. In questo caso, il numero di voci supererebbe il valore massimo, **glFeedbackBuffer** scrive parzialmente il blocco in modo da riempire la matrice (se rimane spazio) e imposta un flag di overflow. Ogni blocco inizia con un codice che indica il tipo primitivo, seguito da valori che descrivono i vertici della primitiva e i dati associati. La **funzione glFeedbackBuffer** scrive anche voci per bitmap e rettangoli di pixel. Il feedback si verifica dopo l'culling dei poligoni e l'interpretazione [**glPolygonMode**](glpolygonmode.md) dei poligoni, quindi i poligoni che vengono culled non vengono restituiti nel buffer di feedback. Può verificarsi anche dopo che i poligoni con più di tre bordi sono suddivisi in triangoli, se l'implementazione OpenGL esegue il rendering dei poligoni eseguendo questa scomposizione.

È possibile inserire un marcatore nel buffer di feedback [**con glPassThrough.**](glpassthrough.md)

Di seguito è riportata la grammatica per i blocchi di valori scritti nel buffer di feedback. Ogni primitiva è indicata con un valore di identificazione univoco seguito da un numero di vertici. Le voci poligono includono un valore intero che indica quanti vertici seguono. Un vertice viene restituito come numero di valori a virgola mobile, come determinato dal *tipo*. I colori vengono restituiti come quattro valori in modalità RGBA e un valore in modalità color-index.

feedbackList < feedbackItem feedbackList \| feedbackItem

feedbackItem < point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru

vertice point < GL \_ POINT \_ TOKEN

LineSegment < vertice del vertice GL \_ LINE TOKEN GL LINE RESET TOKEN \_ \| \_ \_ \_ vertex

polygon < GL \_ POLYGON \_ TOKEN n polySpec

polySpec < vertice del vertice polySpec \|

Bitmap < vertice GL \_ BITMAP \_ TOKEN

pixelRectangle < vertice GL \_ DRAW PIXEL TOKEN GL COPY PIXEL TOKEN \_ \_ \| \_ \_ \_ vertex

passThru < VALORE \_ TOKEN \_ PASS-THROUGH GL \_

vertex < 2d \| \| 3d 3dColor \| 3dColorTexture \| 4dColorTexture

2d < valore

Valore 3d < valore

Colore 3dColor < valore valore di colore

3dColorTexture < valore valore tex

4dColorTexture < valore valore valore color tex

color < rgba \| index

rgba < valore valore

index < value

tex < valore value value

Il *parametro* value è un numero a virgola mobile e *n* è un intero a virgola mobile che specifica il numero di vertici nel poligono. Di seguito sono riportate le costanti a virgola mobile simboliche: GL \_ POINT \_ TOKEN, GL \_ LINE \_ TOKEN, GL LINE RESET \_ \_ \_ TOKEN, GL POLYGON \_ \_ TOKEN, GL BITMAP \_ \_ TOKEN, GL DRAW PIXEL \_ TOKEN, GL COPY PIXEL TOKEN e \_ \_ GL PASS THROUGH \_ \_ \_ \_ \_ \_ TOKEN. GL \_ LINE RESET TOKEN viene \_ \_ restituito ogni volta che viene reimpostato il modello di stipple di riga. I dati restituiti come vertice dipendono dal tipo *di* feedback .

La tabella seguente fornisce la corrispondenza tra *il tipo* e il numero di valori per vertice; *k* è 1 in modalità color-index e 4 in modalità RGBA.



| Tipo                   | Coordinate        | Color | Trama | Numero totale di valori |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| COLORE \_ 3D GL \_          | *x*, *y*, *z*      | *K*   |         | 3 + *k*                |
| TRAMA \_ COLORE 3D GL \_ \_ | *x*, *y*, *z*,     | *K*   | 4       | 7 + *k*                |
| TRAMA \_ COLORI GL 4D \_ \_ | *x*, *y*, *z*, *w* | *K*   | 4       | 8 + *k*                |



 

Le coordinate dei vertici di feedback sono in coordinate della finestra, ad eccezione *di w*, che si trova nelle coordinate del clip. I colori del feedback sono illuminati, se l'illuminazione è abilitata. Se la generazione delle coordinate di trama è abilitata, vengono generate coordinate di trama di feedback. Vengono sempre trasformati dalla matrice di trame.

La **funzione glFeedbackBuffer,** se usata in un elenco di visualizzazione, non viene compilata nell'elenco di visualizzazione, ma viene eseguita immediatamente.

La funzione seguente recupera informazioni correlate a **glFeedbackBuffer**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ RENDER \_ MODE

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





