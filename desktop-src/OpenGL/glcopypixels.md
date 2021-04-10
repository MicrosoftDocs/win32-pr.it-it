---
title: funzione glCopyPixels (GL. h)
description: La funzione glCopyPixels copia i pixel nel framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- funzione glCopyPixels OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964354"
---
# <a name="glcopypixels-function"></a>glCopyPixels (funzione)

La funzione **glCopyPixels** copia i pixel nel framebuffer.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata del piano x della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata del piano y della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.

</dd> <dt>

*width* 
</dt> <dd>

Dimensione della larghezza dell'area rettangolare dei pixel da copiare. Deve essere non negativo.

</dd> <dt>

*height* 
</dt> <dd>

Dimensione dell'altezza dell'area rettangolare dei pixel da copiare. Deve essere non negativo.

</dd> <dt>

*type* 
</dt> <dd>

Specifica se **glCopyPixels** consiste nel copiare i valori dei colori, i valori di profondità o i valori dello stencil. Le costanti simboliche accettabili sono.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <dt><strong>GL_COLOR</strong></dt> </dl></td>
<td>La funzione <strong>glCopyPixels</strong> legge gli indici o i colori RGBA dal buffer attualmente specificato come buffer di origine di lettura (vedere <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>). <br/> Se OpenGL è in modalità di indice a colori:<br/>
<ol>
<li>Ogni indice letto da questo buffer viene convertito in un formato a virgola fissa con un numero di bit non specificato a destra del punto binario.</li>
<li>Ogni indice viene spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto al GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, i bit a zero riempiono i percorsi di bit non specificati nel risultato.<br/></li>
<li>Se GL_MAP_COLOR è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di ricerca GL_PIXEL_MAP_I_TO_I.</li>
<li>Se la sostituzione della ricerca dell'indice viene eseguita o meno, la parte intera dell'indice è quindi <strong>e</strong>ed è con 2<em><sup>b</sup></em> 1, dove <em>b</em> è il numero di bit in un buffer di indice dei colori.</li>
</ol>
Se OpenGL è in modalità RGBA:<br/>
<ol>
<li>I componenti rosso, verde, blu e alfa di ogni pixel letti vengono convertiti in un formato a virgola mobile interno con precisione non specificata.</li>
<li>La conversione esegue il mapping del valore del componente rappresentabile più grande a 1,0 e il valore del componente zero a 0,0.</li>
<li>I valori dei colori a virgola mobile risultanti vengono moltiplicati per GL_c_SCALE e aggiunti a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti colore.</li>
<li>I risultati vengono fissati nell'intervallo [0, 1].</li>
<li>Se GL_MAP_COLOR è true, ogni componente colore viene ridimensionato in base alle dimensioni della tabella di ricerca GL_PIXEL_MAP_c_TO_c e quindi sostituito dal valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A. Gli indici o i colori RGBA risultanti vengono quindi convertiti in frammenti associando <em>la posizione raster</em>corrente e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente e il pixel è il pixel nella posizione <em>i</em> nella riga <em>j</em> . Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. Il mapping di trama, la nebbia e tutte le operazioni di frammento vengono applicati prima che i frammenti vengano scritti nel framebuffer.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <dt><strong>GL_DEPTH</strong></dt> </dl></td>
<td>I valori di profondità vengono letti dal buffer di profondità e vengono convertiti direttamente in un formato a virgola mobile interno con precisione non specificata. Il valore di profondità a virgola mobile risultante viene moltiplicato per GL_DEPTH_SCALE e aggiunto al GL_DEPTH_BIAS. Il risultato viene bloccato nell'intervallo [0, 1]. <br/> I componenti di profondità risultanti vengono quindi convertiti in frammenti associando il colore della posizione raster corrente o l'indice dei colori e le coordinate di trama a ogni pixel, assegnando quindi le coordinate della finestra (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente e il pixel è il pixel nella posizione <em>i</em> nella riga <em>j</em> . Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni. Il mapping di trama, la nebbia e tutte le operazioni di frammento vengono applicati prima che i frammenti vengano scritti nel framebuffer.<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <dt><strong>GL_STENCIL</strong></dt> </dl></td>
<td>Gli indici degli stencil vengono letti dal buffer dello stencil e convertiti in un formato a virgola fissa interno con un numero di bit non specificato a destra del punto binario. Ogni indice a virgola fissa viene quindi spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto al GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra. In entrambi i casi, i bit a zero riempiono i percorsi di bit non specificati nel risultato. Se GL_MAP_STENCIL è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di ricerca GL_PIXEL_MAP_S_TO_S. Se la sostituzione della ricerca dell'indice viene eseguita o meno, la parte integer dell'indice è quindi <strong>e</strong>ed è con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit nel buffer dello stencil. Gli indici stencil risultanti vengono quindi scritti nel buffer dello stencil in modo tale che l'indice letto dalla posizione <em>i</em> della riga <em>j</em> venga scritto in location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente. Solo il test di proprietà dei pixel, il test a forbice e lo stencil writemask influiscono su queste Scritture.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | La *larghezza* o l'altezza è negativa.<br/>                                                                                     |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | il *tipo* è la \_ profondità GL e non è presente alcun buffer di profondità.<br/>                                                                        |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | il *tipo* è lo \_ stencil GL e non è presente alcun buffer dello stencil.<br/>                                                                    |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glCopyPixels** copia un rettangolo di pixel allineato a schermo dalla posizione del framebuffer specificata in un'area relativa alla posizione raster corrente. L'operazione è definita correttamente solo se l'intera area di origine pixel si trova all'interno della parte esposta della finestra. I risultati delle copie dall'esterno della finestra o dalle aree della finestra che non sono esposte sono dipendenti dall'hardware e non definiti.

I parametri *x* e *y* specificano le coordinate della finestra dell'angolo inferiore sinistro dell'area rettangolare da copiare. I parametri *Width* e *Height* specificano le dimensioni dell'area rettangolare da copiare. La *larghezza* e l' *altezza* non devono essere negative.

Diversi parametri controllano l'elaborazione dei dati pixel durante la copia. Questi parametri vengono impostati con tre funzioni: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md). In questo argomento vengono descritti gli effetti sui **glCopyPixels** della maggior parte, ma non tutti, dei parametri specificati da queste tre funzioni.

La funzione **glCopyPixels** copia i valori da ogni pixel con l'angolo inferiore sinistro in corrispondenza di (*x*  +  *i*, *y*  +  *j*) per 0 = *i*  <  *larghezza* e 0 = *j*  <  *altezza*. Questo pixel viene *definito il pixel i nella* riga *j* . I pixel vengono copiati nell'ordine delle righe dalla riga più bassa alla riga più alta, da sinistra a destra in ogni riga.

Il parametro di *tipo* specifica se i dati relativi al colore, alla profondità o allo stencil devono essere copiati.

La rasterizzazione descritta fino a questo punto presuppone i fattori di zoom pixel di 1,0. Se si usa [**glPixelZoom**](glpixelzoom.md) per modificare i fattori di zoom *x* e *y* pixel, i pixel vengono convertiti in frammenti come indicato di seguito. Se (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster corrente e un pixel specificato si trova nella posizione *i* nella riga *j* del rettangolo pixel di origine, vengono generati frammenti per i pixel i cui centri si trovano nel rettangolo con gli angoli

(*x*<sub>r</sub>  +  *Zoom*? i, y <sub>r</sub>  +  *Zoom*<sub>y</sub> *j*)

e

(*x*<sub>r</sub>  +  *Zoom*? (*i* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))

dove *Zoom*? è il valore di GL \_ Zoom \_ X e *Zoom*<sub>y</sub> è il valore di GL \_ Zoom \_ y.

Le modalità specificate da [**glPixelStore**](glpixelstore-functions.md) non hanno effetto sull'operazione di **glCopyPixels**.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glCopyPixels**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position

**glGet** con argomento GL \_ Current \_ raster \_ position \_ valido

Per copiare il pixel di colore nell'angolo inferiore sinistro della finestra nella posizione raster corrente, usare

**glCopyPixels**(0, 0, 1, 1, \_ colore GL);

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





