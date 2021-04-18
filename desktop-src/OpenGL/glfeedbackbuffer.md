---
title: funzione glFeedbackBuffer (GL. h)
description: La funzione glFeedbackBuffer controlla la modalità di feedback.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- funzione glFeedbackBuffer OpenGL
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
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301920"
---
# <a name="glfeedbackbuffer-function"></a>glFeedbackBuffer (funzione)

La funzione **glFeedbackBuffer** controlla la modalità di feedback.

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

Costante simbolica che descrive le informazioni che verranno restituite per ogni vertice. Sono accettate le costanti simboliche seguenti: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ color, GL \_ 3D \_ Color \_ texture e GL \_ 4D \_ Color \_ texture.

</dd> <dt>

*buffer* 
</dt> <dd>

Restituisce i dati di feedback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* non è un valore accettato.<br/>                                                                                                                                                                           |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *dimensione* è negativa.<br/>                                                                                                                                                                                        |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | **glFeedbackBuffer** è stato chiamato mentre la modalità di rendering è il \_ feedback GL oppure [**glRenderMode**](glrendermode.md) è stato chiamato con l'argomento GL \_ feedback prima che **glFeedbackBuffer** venisse chiamato almeno una volta.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                  |



## <a name="remarks"></a>Commenti

La funzione **glFeedbackBuffer** controlla il feedback. Il feedback, ad esempio la selezione, è una modalità OpenGL. La modalità viene selezionata chiamando [**glRenderMode**](glrendermode.md) con feedback GL \_ . Quando OpenGL è in modalità di feedback, nessun pixel viene prodotto dalla rasterizzazione. Al contrario, le informazioni sulle primitive che sarebbero state rasterizzate vengono riportate all'applicazione con OpenGL.

La funzione **glFeedbackBuffer** presenta tre argomenti:

-   *buffer* è un puntatore a una matrice di valori a virgola mobile in cui vengono inserite le informazioni sul feedback.
-   *size* indica la dimensione della matrice.
-   il *tipo* è una costante simbolica che descrive le informazioni restituite per ogni vertice.

È necessario eseguire **glFeedbackBuffer** prima che la modalità di feedback sia abilitata (chiamando **glRenderMode** con l'argomento GL \_ feedback). L'impostazione \_ del feedback GL senza stabilire il buffer di feedback o la chiamata di **GlFeedbackBuffer** mentre OpenGL è in modalità di feedback, è un errore.

Estrarre la modalità di feedback di OpenGL chiamando [**glRenderMode**](glrendermode.md) con un valore di parametro diverso da \_ feedback GL. Quando si esegue questa operazione mentre OpenGL è in modalità di feedback, **glRenderMode** restituisce il numero di voci inserite nella matrice di commenti. Il valore restituito non supera mai le *dimensioni*. Se i dati di feedback richiedevano più spazio rispetto a quello disponibile nel *buffer*, **glRenderMode** restituisce un valore negativo.

In modalità feedback, ogni primitiva che verrebbe rasterizzata genera un blocco di valori che vengono copiati nella matrice di commenti. In caso affermativo, il numero di voci supera il limite massimo, **glFeedbackBuffer** scrive parzialmente il blocco in modo da riempire la matrice (se è presente una stanza a sinistra) e imposta un flag di overflow. Ogni blocco inizia con un codice che indica il tipo primitivo, seguito da valori che descrivono i vertici primitivi e i dati associati. La funzione **glFeedbackBuffer** scrive anche le voci per le bitmap e i rettangoli pixel. Il feedback si verifica dopo che l'eliminazione del poligono e l'interpretazione [**glPolygonMode**](glpolygonmode.md) dei poligoni è stata eseguita, quindi i poligoni che vengono abbattuti non vengono restituiti nel buffer di feedback. Può verificarsi anche dopo che i poligoni con più di tre bordi vengono suddivisi in triangoli, se l'implementazione di OpenGL esegue il rendering dei poligoni eseguendo questa scomposizione.

È possibile inserire un marcatore nel buffer di feedback con [**glPassThrough**](glpassthrough.md).

Di seguito è riportata la grammatica per i blocchi di valori scritti nel buffer di feedback. Ogni primitiva è indicata con un valore di identificazione univoco seguito da un certo numero di vertici. Le voci poligono includono un valore integer che indica il numero di vertici seguiti. Un vertice viene alimentato come un certo numero di valori a virgola mobile, come determinato dal *tipo*. I colori vengono reinseriti come quattro valori in modalità RGBA e un valore in modalità di indice dei colori.

textfeedback < feedbackItem feedback \| feedbackItem

feedbackItem < Point \| LineSegment \| Polygon \| bitmap \| pixelRectangle \| PassThru

punto < vertice del token del \_ punto GL \_

lineSegment < GL riga token Vertex Vertex vertice del vertice del \_ \_ \| token di \_ \_ reimpostazione della riga \_

Polygon < \_ token poligono GL \_ n Polispec

Polispec < vertice del vertice del vertice di Polispec \|

bitmap < \_ vertice del \_ token bitmap GL

pixelRectangle < GL creare il vertice del token di pixel per il vertice del \_ \_ \_ token pixel \| \_ \_ \_

passThru < GL \_ pass- \_ through del valore del \_ token

Vertex < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture

valore di < 2D

valore valore < 3D

3dColor < valore valore valore valore

3dColorTexture < valore valore valore valore Tex

4dColorTexture < valore valore valore valore valore Tex

Color < \| Indice RGBA

RGBA valore valore valore valore <

valore < indice

valore valore valore valore di < Tex

Il parametro *value* è un numero a virgola mobile e *n* è un Integer a virgola mobile che fornisce il numero di vertici nel poligono. Di seguito sono riportate le costanti a virgola mobile simboliche: \_ token del punto GL \_ , token di riga GL, token di reimpostazione della riga GL, token del poligono GL, token della \_ \_ \_ \_ \_ \_ \_ \_ bitmap GL \_ , token del \_ \_ pixel di estrazione GL \_ , token del \_ \_ pixel di copia GL \_ e \_ token di pass- \_ through \_ . \_ \_ \_ Il token di reimpostazione della riga GL viene restituito ogni volta che viene reimpostato il modello line stipple. I dati restituiti come vertice dipendono dal *tipo* di feedback.

La tabella seguente fornisce la corrispondenza tra il *tipo* e il numero di valori per vertice. *k* è 1 nella modalità di indice colore e 4 in modalità RGBA.



| Tipo                   | Coordinate        | Colore | Trama | Numero totale di valori |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| \_Colore GL 3D \_          | *x*, *y*, *z*      | *k*   |         | 3 + *k*                |
| \_ \_ Trama colori GL \_ 3D | *x*, *y*, *z*,     | *k*   | 4       | 7 + *k*                |
| \_ \_ Trama colori GL \_ 4D | *x*, *y*, *z*, *w* | *k*   | 4       | 8 + *k*                |



 

Le coordinate dei vertici dei commenti sono nelle coordinate della finestra, eccetto *w*, che è nelle coordinate di ritaglio. Se l'illuminazione è abilitata, vengono illuminati i colori di feedback. Se la generazione delle coordinate di trama è abilitata, vengono generate le coordinate della trama di feedback. Vengono sempre trasformati dalla matrice di trame.

La funzione **glFeedbackBuffer** , se utilizzata in un elenco di visualizzazione, non viene compilata nell'elenco di visualizzazione, bensì viene eseguita immediatamente.

La funzione seguente recupera le informazioni correlate a **glFeedbackBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_

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

[**Remo**](glend.md)
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

 

 





